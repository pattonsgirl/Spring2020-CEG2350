# Lab 2

## Lab Procedure
Document your progress in a plain text file named `Lab02-LastName.txt`  
where LastName is your last name

At the top of the file please enter your personal details as follows:
```
Name: Your name
Email: Your email

```
## Part 1 - Other ways to access your key
Now that we've gone the long way, let's look at the shortcut.  MobaXTerm has ssh built in by default, so you could use it instead of WSL Ubuntu to SSH to your AWS Educate environment.  The purpose of this part of the lab is to find a file using the command line.  Pick one of the two routes below to find the key you downloaded or saved to your local system, not the key we copied to `/home/your_username/`

1. Open MobaXTerm w/ Local Terminal
* On the front page, before you click or open anything, you should see an option for "Start Local Terminal"
    * If you already setup WSL Ubuntu as your default:  
        In the User Sessions listing, right click and select "New Session"
        Click on "Shell".  Use the defaults, and select OK.
* The Welcome text in the shell tells us something very convenient: 
    * `Your computer drives are accessible through the /drives path`
    * Try typing `cd /drives/`
    * Use `ls` to see what is in this directory.

2. Open MobaXTerm OR WSL Ubuntu
* Open a WSL Ubuntu terminal
* The Welcome text in the shell tells us something very convenient: 
    * `Windows drives are mounted into /mnt path`
    * Try typing `cd /mnt/`
    * Use `ls` to see what is in this directory.

Now that you can see your file system, **in your lab notes, write the file path to your key**.  
Useful Commands: `pwd, ls, cd`

Mac users:  
In your Terminal go to your root directory.  In your lab notes, write the file path to get to your key.


## Part 2 - Log in to your AWS Educate environment:  
`ssh -i /path/to/private/key ubuntu@ElasticIP`  
Use either your newly found path to your key or the key in your `/home/username` directory.

If you've forgotten your key, you'll need to provision a new stack in AWS Educate and create a new key.  
See [Remaking your AWS Educate environment](../../..) for instructions.

1. Run `sudo apt update` - in your lab notes, explain what update does
2. Run `sudo apt upgrade` - in your lab notes, explain what upgrade does
3. Run `sudo apt autoremove` - in your lab notes, explain what autoremove does
Useful commands: `man, apt, sudo`

## Part 3 - Directories, Files, and Permissions
Where questions are presented, answer them in your lab notes.  For each step, include the command you  
used to perform the direction or answer the question posed.  If you did something "wrong" make a note  
of it in your lab.  These are learning experiences.
1. Create a directory called `Lab02`
    * In `Lab02`, create one directory called `DirA` and one directory called `Directory B`
    * What happens to the path name of `Directory B`?  Which of the folders uses a better naming convention?
    * Rename `Directory B` to `DirB`  
    Useful commands: `man, mkdir, cd, ls, pwd, mv`
2. In `DirA`, create a file called `test.txt`
    * Put at least three lines of text in `test.txt` using `vim`
    Useful commands: `touch, vim`
3. Make a copy of `test.txt`
    * Rename it to `.hidden.txt`
    * Type `ls`.  Can you see both files?  Use flags for `ls` to see your file.  
    Useful commands: `cp, mv, ls`
4. What are the permission settings for user, group, and other of the files in `DirA`?  What is the current  
owner and group name?  
    * Use `sudo` to make a copy of `text.txt` called `su-test.txt`
    * What are the permission settings for user, group, and other for `su-text.txt`?  What is the current  
owner and group name?
    * Can your user read this file?  How can you read this file? 
    * Change the file permissions so you can read and write to the file without using sudo 
    Useful Commands: `chmod, chown, chgrp, ls, sudo, cp, cat`
5. By default, what does `ln` followed by a filename do?  Use `ln` to create a file named `hard.txt` from `test.txt`
    * Note the inode number of `hard.txt` and `test.txt`
    * Create a symbolic link called `sym.txt` from `hard.txt`
    * Note the inode number of `sym.txt`.  Is it the same as `hard.txt`?
    * Delete `test.txt`.  Is `hard.txt` and `sym.txt` still readable?
    * Delete `hard.txt`.  Is `sym.txt` still readable?  Why or why not?
    * Make a new file called `hard.txt` with some text in it.  Can you read `sym.txt` now?
    * Move `hard.txt` to `DirB`.  Can you read `sym.txt`?
    * Delete `sym.txt`
    * Create a symbolic link from `hard.txt` in `DirB` to `newsym.txt` in `DirA`
    Useful Commands: `ln, test, stat`


## Submission
Upload your file named Lab02-LastName.txt to the Pilot Dropbox.