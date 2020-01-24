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
One uses MobaXTerm.  The other uses Powershell (assuming you have the latest version of Windows 10).  Since one is consistent (MobaXTerm) and the other is not (Powershell), I'll tell you how to use just MobaXTerm.

* Open MobaXTerm
* On the front page, before you click or open anything, you should see an option for "Start Local Terminal"
    * If you already setup WSL Ubuntu as your default:  
        In the User Sessions listing, right click and select "New Session"
        Click on "Shell".  Use the defaults, and select OK.
* The Welcome text in the shell tells us something very convenient: 
    * `Your computer drives are accessible through the /drives path`
    * Try typing `cd /drives/`
    * Use `ls` to see what is in this directory.

Now that you can see your file system, in your lab write notes write the file path to get to your key.  
Commands that may help: `pwd, ls, cd`    
*Note: not the one we copied to WSL Ubuntu, but the one that you downloaded or saved*


Log in to your AWS Educate environment:  
`ssh -i /path/to/private/key ubuntu@ElasticIP` 

## Part 2 - Files and Directories
* Create directories
* Create files
* Create a hidden file
* Play with chmod
* Explore soft links vs. hard links