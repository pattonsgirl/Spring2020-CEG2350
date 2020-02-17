# Lab 5 - NOT FINALIZED

## Lab Procedure
Document your progress in a plain text file named `Lab05-LastName.txt`  
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

## Part 1 - Git Fidgetting
1. Create or sign in to your [github](https://github.com/) account.
2. Create a new Repository with a name of your choice.  I recommend `CEG2350`. 
    * Set it to Private (you can change this in the future).  
    * Check the box to Initialize this repository  with a README
    * Click Create Repository
    * You should be asked to input text into a `README.md` file.  Your text can be:
```
Course work for CEG 2350 Spring 2020
```
3. In your github repository, select Clone or Download (green button).  It should say "Clone with HTTPS".  Copy the URL to your clipboard
4. Go to your AWS Educate environment.
5. Create a folder called `git` and change into the folder.  Write the command you used.
6. Use the `git` command to `clone` your repository.  Write the command you used.

## Part 2 - Simple Makefile
1. Copy your `Lab04` folder to `git/CEG2350/Lab05`.  Write the command(s) you used.
2. Check the `status` of your git repository.  Write the command you used and any output.
3. Commit and push the folder `Lab05` and its contents to your git repo.  Write the command(s) you used.
4. In `Lab05` create a file called `Makefile`.  Write the command you used.
5. Write contents in `Makefile` so that in the shell the following commands perform the following actions:
    * `make` will compile the program and create an executable version
    * `make run` will compile and execute the program
    * `make clean` will delete the compiled program
6. Copy the contents of your `Makefile` into your lab notes.
7. Commit and push your `Makefile` into your git repo.  Write the command you used.

## Part 3 - 

## Submission
Upload your file named `Lab05-LastName.txt` to the Pilot Dropbox.