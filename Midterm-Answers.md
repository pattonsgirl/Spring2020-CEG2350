1. What is the point of pathnames / environment variables?
In Linux pathnames (specificed by $PATH) tell the system where to look for binaries / programs / scripts and in which order.  It is similar for Windows environment variables.

2. In a git repository, I create a new file called hello.txt  Write the steps to get it into my repository.
Minimum correct answer:
git add hello.txt
git commit
git push

3. ROM is what type of memory?  List some examples.
Full answer:
Read only memory.  It is non-volatile.  This means that data is not deleted when the device is powered down.
Examples: flash drives, CD drives, HDD, SSD, floppy disks

4. What is the difference between a hard link and a copy of a file?
Essentials of correct answer:
Copy has a different inode than the original file, and data is stored independent of the original (a change I make in one is not in the other).  Hard links have the same inode (a change in one is also done on the other)

5. Explain hard link vs. soft links.
Thorough answer:
Hard links have the same inode as the original file, meaning that they use the same spots in memory.  Editing either will change the content that both reference.  Soft links have their own inode number and point to the hard link / original file.  If a hard link / original file used by the soft link is deleted the soft link can no longer be used to access the file.  Soft links can be deleted and not affect the hard link / original file.

6. Name a difference between binaries in sbin and binaries in bin.
sbin holds system level binaries (associates more with root & sudo), bin holds essential binaries (associates more with regular users).  
Examples of sbin: mkfs & gdisk.  Examples of bin: mkdir & chown

7. How is data stored on a computer?  What would be the benefit of defragmenting your disk?
Data is stored in available block space, not necessarily sequentially.  Defragmenting will order data so that it is in sequential order.  This is more necessary for hard drives than SSDs due to the difference in how the read / write operations work.  Defragmenting does not delete files.

8. The .bashrc file in my home directory and any aliases in it are unique to my user.
It is true.  Other users cannot use my .bashrc file unless they copying it to their home folder or is added to the default .bashrc configuration for all users

9. I have a local directory that I would like to make a local git repository.  What command(s) do I need to use?
git init

10. What information does an inode keep track of?  What command can show me this information for a given file / folder?
Inodes keep track of meta data about a file / folder such as creation date, date modified, and which disk blocks it is stored on.
'stat' shows me the indoe information about a given file / folder
'ls -li' will show me the inode, but not the meta information

11. Craft the necessary command(s) to change the permissions on this file so that bob is the owner and can read and write, the group can read and write, and others can only read.

-rwxr-x--x sue sue file.txt

One way to do it:
chown bob file.txt - this changes owner
chmod -x file.txt - removes execute for all
chmod g+w file.txt - adds write privileges for group
chmod o+r file.txt - adds read only privileges to others

final form:
-rw-rw-r-- bob sue file.txt

12. Provide all information you can based on the following:

dr-x-w-w-- bob sue test - SHOULD BE
dr-x-w-r-- bob sue test

d is for directory.  User is bob, bob can read and execute.  Group is sue, sue can write.  Other can only read.  Name of the directory is test.

13. What are some ways I can see file / folder permissions in Windows?
You could use WSL Ubuntu (making ls -l and stat valid).  I was aiming for cmd (dir /Q) / File Properties.

14. What is the difference between Linux, Ubuntu, and 4.15.0-55-generic?  (which is the kernel, which is the operating system, and which is a distribution / flavor)
Linux is the operating system, Ubuntu is the flavor / distribution, 4.15.0.55-generic is the kernel.

15. What is a disk partition?  What does a partition need for me to store data on it?
A disk partition is a defined space on a disk where information is stored.  To store data on a disk partition, in must have a filesystem.  The disk itself needs a partition table (such as MBR or GPT)

16. I am creating a script that relies on a specific file existing in a specific directory, but the program can be run by any user.  Should I use an absolute or relative path to reference the file in my script?
Absolute

17. What does the bootloader do?  What is a common bootloader for Linux?
bootloader loads the kernel (would accept OS) into memory to start the kernel.  A common bootloader in Linux is GRUB (Grand Unified Bootloader)

18. The operating system is the first thing that runs when I push the power button on my computer.
False.  The BIOS is first.

19. What does 'ps l' show?
Processes being run in any shell owned by my user.  It also shows parent ids of processes being run by me.

20. List some differences between MBR and GPT.
MBR was the original partitioning table creating for DOS / BIOS. GPT came about for newer BIOS / UEFI.  GPT has duplication of the bootloader and can repair corrupted files on its own.  GPT also supports larger drives by default, whereas MBR requires some manipulation to support large drives.  Modern systems require the BIOS to have Legacy mode enabled to use MBR partition tables.

21. The kernel / CPU follows the fetch-decode-discard cycle from startup to shutdown.
False.  The kernel / CPU follows the fetch-decode-EXECUTE cycle from startup to shutdown.

22. In a Makefile, how would I run the following target?  What would the target do?
go: code.c
     gcc -Wall -o runme code.c

To run the target, use 'make go' in the terminal.  The target compiles a c program called 'runme' from a source code called 'code.c'

23. If a child process is orphaned, how is it terminated?
If parent dies first, child is orphaned and needs to be killed.  Kernel takes over and super parent ('init') uses system calls to terminate child processes.  You can use kill manually, BUT init should be taking over so fast that the manual process isn't doable.

24. I start running a process in the foreground in my terminal.  How can I pause / suspend it?  How can I send it to the background?  To save myself future pain, how could I have started the process in the background in the first place?
Suspend with Ctrl + Z.  Send it to background with 'bg'.  If I have multiple suspended jobs, I can use bg job_num to send them to the background.  Should have ran it with 'command_name stuff &'

25. What Linux command can help me find information about most commands, not just the built-in ones?
man
help does built-ins only

