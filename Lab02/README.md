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

If you've forgotten your key, you'll need to provision a new stack in AWS Educate and create a new key.  
See [Remaking your AWS Educate environment](../../..) for instructions.

## Part 3 - Files and Directories
* Create directories
* Create files
* Create a hidden file
* Play with chmod
* Explore soft links vs. hard links

## Submission
Upload your file named Lab02-LastName.txt to the Pilot Dropbox.