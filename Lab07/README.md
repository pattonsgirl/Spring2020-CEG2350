# Lab 07

## Lab Procedure
Document your progress in a plain text file named `Lab07-LastName.txt`  
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

## Part 1 - Look Ma, No Password! (4pts)
Put your public key in GitHub and switch your repository URL to use SSH instead of HTTPS
1. In a web browser, go to your git repository.  Click your user icon in the top left, then click Settings.  Select SSH and GPG keys.  
Q. What is the difference between SSH and GPG keys?
2. In AWS (preferred) or your system, create an SSH key pair.  (Useful command: `ssh-keygen`)  
Q. What directory did the key pair get stored in?  Which is the public and which is the private key?  What are some markers to tell the difference?
3. In GitHub, select New SSH Key.  Paste the contents of your key into GitHub.  
Q. Did you paste the public or private key?  Why?
4. In GitHub, go back to your class repository.  Click the Clone or download button, then select "Use SSH".  It should have a form such as: `git@github.com:USERNAME/REPOSITORY.git`.  Copy this URL.
5. Follow the [Switch remote URLs from HTTPS to SSH](https://help.github.com/en/github/using-git/changing-a-remotes-url) guide in the link provided.  This should be performed in AWS (prefered) or your system if that is where your git repository is.  
Q. Write the commands you used per this guide and any additional steps you needed.  
6. In your git repository, create and push a new file to check out your new connection method.  
Q. Write the commands you used and any additional steps you needed.

## Part 2: [/insert AOL noises here/](https://www.youtube.com/watch?v=D1UY7eDRXrs) (3pts)
For your local system, identify the following information regarding your network connection:
1. Network interface
2. MAC address
3. IP Address
4. Subnet mask
5. Gateway  
Q. According to the settings above and some defaults discussed in class, are you on a private network?  Based on that answer, how do you communicate to the "world" (google.com, wright.edu, etc.)?
6. Type `host` followed by the URL of your favorite website.  
Q. Copy the command and its results into your lab write up.  What can you infer?  Do the reverse, `host` followed by the IP address given by the results.  Is your favorite website likely hosted on a single system, or is a single system likely serving multiple websites?

## Part 3: (3pts)
For the following, document the commands you used and address the question in `3`.
1. Create a file on your local system (likely in WSL Ubuntu).  Call it something noticeable like `something-noticeable.txt`.  Instead of using the `ssh` command to access AWS, use `sftp`.  If you've forgotten that command by now, take a peek in your `.bashrc` file to peek at your original `ssh` command.    
2. Using `sftp` commands, create a `Lab07` file inside of your `CEG2350` repository.  Copy your local file to the newly created `Lab07` folder.  Type `help` inside of your `sftp` connection to see a list of available commands.  Once completed, type `exit` to close the connection.
3. Get the `md5sum` of both your local file and the file now copied to AWS.  Make a change to the contents of one or the other, and check the `md5sum` of both again.  Are the `md5sum`s of both files still the same?  Why or why not?


## Submission
Upload your file named `Lab07-LastName.txt` to the Pilot Dropbox.