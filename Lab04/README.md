# Lab 4

## Lab Procedure
Document your progress in a plain text file named `Lab04-LastName.txt`  
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

## Part 1 - Processes
**Log in to your AWS Edu environment:**

1. Craft a command that snapshots processes being run by and for your user, `ubuntu`
    * Note: you need to use to correct flags to see all process being run.
    * Helpful commands: `grep, ps, |`

2. `sleep` is a neat command that creates a process that does nothing for the amount of time specified.  I very  
much recommend reading through the rest of this section before performing it.
    * Run a `sleep` command that runs for 5 minutes.  Can you enter anything?  Do **not** exit the terminal or  
    press `Ctrl+C`
    * Since we have remote access to this machine, we can open *another* connection to AWS to see what is going on.  
    Open another terminal and connect to AWS.  
        * What does `ps l` show us?
    * `kill` the `sleep` command running in the other terminal using its process ID.
    * Switch to the terminal you wrote the `sleep` command in.  Is there a message there?
    * Run the command again, but this time set it to run in the background.
    * Use the job ID to bring it back to the foreground, and send a signal to terminate it with `Ctrl+C`

## Part 2 - Programs
1. On your **local** machine, create an `alias` called `aws-ssh` that contains the command and parameters you have  
been using to log on to your AWS Educate system.  Use an *absolute* path to your key file in your command.  Why use  
an absolute path instead of relative?
    * Note: you can do this in WSL-Ubuntu, Mac, or the MobaXTerm Local Terminal
    * Powershell users: `set-alias` doesn't work the same way for you (yay!).  To save you some headache, I'll tell  
    you that you need to create a `function`, *not* an `alias`

2. Run your new `alias` to test it.  Exit out of your AWS terminal.  Make your `alias` permanent for your user in the `.bashrc` file.
    * MobaXTerm users (no WSL-Ubuntu): you need to create a file called `.bash_profile` to store your aliases
    * Powershell users: You can *try* [this guide](https://www.repusic.com/powershell/2018/04/09/Powershell_permant_profile.html) to save your function.  
        * If you get this message: `... cannot be loaded because  running scripts is disabled on this system`, mark  
        the steps you followed.  If you want the scary red text to go away, edit the `$profile` and delete the text  
        you entered.

**Log back in to your AWS Edu environment for the next steps:**

3. List the version and location of `python`, `java`, and `gcc`.  Helpful commands: `whereis, which, man`
    * How can I use python 3?

4. Create a folder named `Lab04`.  Go into the folder.  Create a file named `input.txt`.  Put the following content in it:
    ```
    Hello!
    ```
    * You may choose *Java* or *C* or *C++* to do the following.  
        * Python is not a compiled language, and will **not** count for credit.
    * Create a file called `helloworld` with the appropriate extension for your language of choice (`.java` for Java  
    , `.c` for C, `.cpp` for C++).  Write the command(s) you used to create and edit your code.
    * Write a program that echos text inputted by the user.  Code integrity does not matter - you may work together  
    or use things found on the internet or textbooks.  Include your code in your lab write up.
        * Note: Assume no spaces, just a single word / string
    * Compile your code.  Write the command you used to compile it.
    * Run your program.  Write the command you used to run it.
    * Run your program by *redirecting* the input to be from your `input.txt` file.  Write the command you used.
    * Run your program by *redirecting* the input to be from your `input.txt` file **and** redirecting the output to  
    a file called `output.txt`.  Write the command you used.
    * Run your program by *redirecting* the input to be from your `input.txt` file **and** writing to both standard  
    output **and** redirecting the output to a file called `output.txt`.  Write the command you used.
    * Modify the contents of `input.txt` to only have `Cool!`.  
    * Run your program by *redirecting* the input to be from your `input.txt` file **and** *appending* the output to  
    `output.txt`.  Write the command you used.

## Submission
Upload your file named `Lab04-LastName.txt` to the Pilot Dropbox.