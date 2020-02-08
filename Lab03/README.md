# Lab 3

## Lab Procedure
Document your progress in a plain text file named `Lab03-LastName.txt`  
where LastName is your last name

At the top of the file please enter your personal details as follows:
```
Name: Your name
Email: Your email

```

Where questions are presented, answer them in your lab notes.  For each step, include the command you  
used to perform the direction or answer the question posed.  If you did something "wrong" make a note  
of it in your lab.  These are learning experiences.

Unless explicity stated, assume you should perform the lab assignment in your AWS Educate environment.  
`ssh -i /path/to/private/key ubuntu@ElasticIP`  

If you've lost or forgotten your key, you'll need to provision a new stack in AWS Educate and create a new key.  
See [Remaking your AWS Educate environment](../../..) for instructions.

## Part 1 - Exploring the File System
1. Identify the bootloader and kernel for your **local** system (ie. laptop, home pc, or lab machine).
    * Note: some systems can refer to lab slides for terminology.  Don't need proof.

2. In AWS, read `/boot/grub/menu.lst`  
    * If you were to see the grub menu while booting, what are the options grub would present?  
    * What kernel is used AWS Educate?   
    * Use `df -T` to find out the file system used by this device.  
        * Hint: What is the top of the Linux directory structure?

3. In AWS, run `sudo parted -l`
    * What is the primary disk in the `/dev` folder?  
    * What type of partition table is our AWS environment using? 
        * Hint: If it looks unfamilar, use Google to find the common name
    * How many Gigabytes (GB) of storage do we have?

## Part 2 - Partitions
1. Use `df -h`
    * How much space is used and how much space is free?
2. Run `parted` on the disk (use the answer you found in Part 1-3)
    * How can you view the options for `parted`?
3. The remainder of this section will deal with theorical questions since we can't go to AWS in person.
    * There are two steps related to resizing partitions - list them.
        * Note the process to *expand* a filesystem.
        * Note the process to *shrink* a filesystem.
        * *Hint*: You can use Google, or you can look at the usage guide for `resize2fs`
    * Let's say we can go to AWS and plug in a brand new hard drive that is 8TB in size.  Assume that when the drive  
    is plugged in, the drive name is `/dev/sdb`
        * What partition table should we select?  Why?
        * What command(s) / program(s) can we use to create a partition table on our new drive? 
            * Note the command and its parameters
        * What command can we use to create a filesystem on our partition?
            * Note the command and its parameters
    * Let's assume the above went well.  Write the command to mount the drive to `/mnt/Lab03`
        * If we wanted to make this permanent, what file would we need to edit?

## Submission
Upload your file named `Lab03-LastName.txt` to the Pilot Dropbox.