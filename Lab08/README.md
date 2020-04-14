# Lab 08 - NOT FINALIZED

## Lab Procedure
Document your progress in a plain text file named `Lab08-LastName.txt`  
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
`ssh -i /path/to/private/key ubuntu@ElasticIP`  OR `aws-ssh` assuming sucessful completion of Lab 04

If you've lost or forgotten your key, you'll need to provision a new stack in AWS Educate and create a new key.  
See [Remaking your AWS Educate environment](../../..) for instructions.

## Part 1: Branching Out (5pts)


## Part 2: Back It Up (5pts)
1. Use `tar` to create a tar ball of your AWS home directory.
2. How large is the tarred file?
3. Use `gzip` (or a similar tool) to compress the file.  How big is it now?
4. Use an `sftp` connection OR `rysnc` to **download** the compressed home directory to your local system from AWS.
5. Check the `md5sum` values between the remote and local compressed file to verify file integrity.

## Extra Credit: Curiousity Taught the Cat (2pt)
Use your AWS portal, or just use Google.  

Find something that people are using AWS for that you would be curious about investigating.  Try to describe a project idea that comes to mind.

Note: this is for fun.  Have some fun!  Personally, I want to play with the AWS Deep Racer

## Submission
Upload your file named `Lab08-LastName.txt` to the Pilot Dropbox.