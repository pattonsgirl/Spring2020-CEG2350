# Lab 3 - NOT FINALIZED

## Lab Procedure
Document your progress in a plain text file named `Lab03-LastName.txt`  
where LastName is your last name

At the top of the file please enter your personal details as follows:
```
Name: Your name
Email: Your email

```
Unless explicity stated, assume you should perform the lab assignment in your AWS Educate environment.  
`ssh -i /path/to/private/key ubuntu@ElasticIP`  

If you've lost or forgotten your key, you'll need to provision a new stack in AWS Educate and create a new key.  
See [Remaking your AWS Educate environment](../../..) for instructions.

## Part 1 - Exploring the File System:
Where questions are presented, answer them in your lab notes.  For each step, include the command you  
used to perform the direction or answer the question posed.  If you did something "wrong" make a note  
of it in your lab.  These are learning experiences.

Identify the bootloader and kernel for your local system (ie. laptop, home pc, or lab machine)

Read /boot/grub/menu.lst  What are the two options?  What is our kernel on AWS Educate?   

Use df -T to find out the file system used by this device.  Hint: what is the top of the Linux directory structure?

Run sudo parted -l.  What is the disk name in the /dev folder?  What type of partition table are we using (if it looks unfamilar, use Google to find the common name)  How many Gigabytes (GB) of storage do we have?

Let's see how much space we can play with.  df -h

Use the appropriate partitioning tool to create a 0.5 GB partition.  Make a filesystem on that partition that is compatible with Linux.  Mount the partition to /mnt/Lab03

Note: If you ruin this, DON'T PANIC.  You will just need to create a new stack by deleting yours, then clicking the provision link from Lab 1

Look at /usr/lib

## Submission
Upload your file named `Lab03-LastName.txt` to the Pilot Dropbox.