# Lab 06

## Lab Procedure
Document your progress in a plain text file named `Lab06-LastName.txt`  
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

## Part 1 - More Git Practice (1 pt)
1. Go to your AWS Educate environment.
2. In your CEG2350 git repository, create a new folder called `Lab06`.
3. Add the folder for tracking, and commit and push the folder to your GitHub repository.

## Part 2 - Intro to Scripts & Regular Expressions (9 pts)
1. Create a file in `Lab06` called `sortme.txt`.  It should have the contents below:
```
9.1
43.7
2.2
62.1
2.1
9.3
43.5
4.6
44.6
4.7
42.7
47.4
46.6
4.5
55.6
4
9.2
66.6
2
2.3
```
2. Create a bash script called `sorting-party.sh`.  The script should have the following features:
* Takes in an *input* file name as a first argument.
* Takes in an *output* file name as a second argument.
* Uses regular expressions to verify that the file names end in `.txt`  [This guide](https://www.poftut.com/how-to-use-regular-expression-regex-in-bash-linux/) should help you out.
* Sorts the data using the `sort` command.
* Outputs the sorted data to a file called `sorted.txt`

Therefore, `sorted.txt` should have these contents:
```
66.6
62.1
55.6
47.4
46.6
44.6
43.7
43.5
42.7
9.3
9.2
9.1
4.7
4.6
4.5
4
2.3
2.2
2.1
2
```
3. Copy the contents of your script into your lab write up.
4. Create a file called `README.md`.
* What does the `.md` extension mean in a git repository?
* Using [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet), create a usage guide for how your script works and explaining the contents of the `Lab06` folder.  Copy its content into your lab write up.
5. Commit and push your files to your github repository.  Write the command(s) you used.

## Submission
Upload your file named `Lab06-LastName.txt` to the Pilot Dropbox.

Check permission post sftp
Use md5sum to check validity of a file
gpg encrytpion?

Scripting & git
