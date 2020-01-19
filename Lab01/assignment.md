# Lab 1
The purpose of this lab is to familiarize yourself with the lab space we will be using  
for the remainder of the labs.  You should have received an email regarding your AWS  
Educate account for this class.  We will be using AWS to create virtual environments  
for you to use to complete the tasks given.

## Objectives
1. Get Started with AWS Educate
2. Start building your git(hub) toolbox
3. Use some linux commands in your AWS environment
5. Submit your answers to Pilot

**Important Note:**  This AWS environment only allows inbound access from following ports:
* 22

### Setup for Windows Users
* Open Powershell as Administrator
* Enter the following line  
  `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`
* You will need to reboot your system to finish installing the package
* Install Ubuntu 18.04 LTS from the Windows store
* Launch Ubuntu 18.04 LTS Bash to finish configuring your account
  (username/password)  
  Note: the password prompt cursor does not move.  Type your password and hit Enter to continue  
  If it does anything else, you may need to repeat this process starting with Powershell
* [Download MobaXterm Home Edition](https://download.mobatek.net/1242019111120613/MobaXterm_Installer_v12.4.zip)
* Extract the Installer file to your Desktop.
* Double-click to run the installer
* Once installed, run the program one time - this finishes the installation
* You can now delete the installation files

## Lab Procedure
Perform the following tasks.  Document your progress in a plain text file named `Lab01-LastName.txt`  
where LastName is your last name

At the top of the file please enter your personal details as follows:
```
Name: Your name
Email: Your email

```
For each part give a summary of steps taken and document any challenges you faced.   
Be sure to answer all questions asked.

## Register for AWS Educate
You should have an email from AWS Educate to guide you through account creation.  
Note: The email was sent to your wright.edu email account

Once you have filled in the information and verified your email address, you will get an account  
approval email.  For reference, mine took 2-3 minutes to arrive.

## Part 1 - Provision the lab environment in AWS.  
Assuming you have registered for AWS Educate and have access to this class, perform the following:

* [Sign in to AWS educate](https://www.awseducate.com/signin/SiteLogin)
  * Click the `My Classrooms` Button
  * Click the blue `Go to classroom` button for *Operating Systems Concepts and Usage*
  * Click the blue `AWS Console` button  
  
  This will launch the AWS console  
  Note: If you were already logged in with your personal account, click the log out prompt and  
  log back in with your university account
  
  Your username in the top right should look something like this  
  `vocstartsoft/user236529=lastname.number@wright.edu`.

Now we need to create an SSH key pair to get to your virtual machine.

* Click the Services menu, then select EC2 under Compute  
  [EC2 service from the AWS console](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Home:)  
  In the center area you should see a list of all Resources you have available.  
  Right now they should all be 0.
* Click on [Key Pairs](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#KeyPairs:sort=keyName) 
* Click on the `Create Key Pair` blue button.  
  Choose the name for your key.  I used `ceg2350-aws-vm`  
  This creates a public/private key pair, stores the public key in AWS, and  
  downloads the private key to your local machine.
* **Do not lose this private key.**  
  If you do lose it, log in to AWS Educate, delete the lost key, and generate a new one.  
  If you are using a lab machine, save your key by emailing it to yourself to saving it to a USB drive
* Once you have created your SSH key, [click here to provision your virtual environment](https://console.aws.amazon.com/cloudformation/home?region=us-east-1#/stacks/new?stackName=CEG-2350&templateURL=https:%2F%2Fwsu-cecs-cf-templates.s3.us-east-2.amazonaws.com%2Fceg2350.yml)  
  This link autofills many fields for creating our virtual machine.
  * On the first menu, click Next
  * On the second menu, under Parameters, type the name of the key pair you made in the  
  step above.  If you don't remember, you can [open your key list here](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#KeyPairs:sort=keyName).  Click Next
  * On the third menu, select Next
  * Scroll to the bottom and select Create Stack
  * You will be redirected to a status page that says CREATE_IN_PROGRESS

* Once you have created the AWS Cloud formation stack you can [return to the EC2 service](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Home:).  
  Here you should see additional resources have been created (not everything says 0 anymore) 
* Click on [Running Instances](https://console.aws.amazon.com/ec2/v2/home?region=us-east-1#Instances:sort=instanceState)
* Our machine should now be created (or almost ready).
* We need to know the Elastic IP address.  This IP address is what we will use to SSH into our
  virtual environment.

*Note: There are no questions to answer in Part 1.  Please just document your
experience creating the lab environment.*

## Part 3 - Connecting to the AWS environment
**You are now ready to make an SSH connection to your AWS server.**  
Using MobaXterm perform the following actions:
* Copy the AWS private SSH key to your home directory
* Make a file with the name of your AWS Educate key
    * For example, `ceg2350-aws-vm.pem`
* Open a text editor (`vim` or `nano`) for your file
    * Copy the contents of the file that was downloaded from AWS Educate into the file
* Make the key only readable by your user (`chmod`)
* SSH into your AWS server with the following (replace */path/to/private/key*
  and *ElasticIP* with your information):  
  `ssh -i /path/to/private/key ubuntu@ElasticIP`

### Acknowledgement
Credit to Matt Kijowski's GitHub Repo - [Lab 1 for Cyber Security Analysis](https://github.com/mkijowski/cyber-security-analysis-applied/blob/master/labs/lab1.md)
