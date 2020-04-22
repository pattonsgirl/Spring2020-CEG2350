# Topic Overview of Final Exam
It may be useful to fork / clone this to your github.  This will make you feel really cool.

### also important
* ssh keys
    * private vs public (and where to put which)
* sftp
* compression
* tar
* checksums

### bash
* bash scripting
    * if statements:  
        if [CONDITION_usually_from_`test`]; then  
            stuff  
        elif [Other_conditions]; then  
            stuff  
        else  
            stuff  
        fi
    * loops
        * for loops:  
        for i in LIST  
        do  
            stuff with $i  
        done
        * while loops:
        while [CONDITION]  
        do  
            stuff  
        done
    * using `test` flags
        * conditionals in scripting
        * remember you don't need the word `test`, you can just use the the conditional provided by `test`
    * arguments and how to access arguments in scripts
        * to access individual arguments: $# where # is the argument from the command line
        * to access all arguments: $@
* regular expressions
* sed (basic format) (see quiz 3)
* various ways to input / output from a file

### git
* init
* clone
* **add**
* **commit**
* **push**
* **branch / checkout**
* **merge**
    * What step(s) should I take for a successful merge?
    * What does a merge do?
* pull (fetch + merge)
* when to use a fork vs. a branch
    * fork - mostly for a full deviation from an original project
    * branch - mostly for features

### virtualization
* virtual machines
    * what is a hypervisor? (week 11, slide 5)
    * Install a full iso (including kernel)
    * Hypervisor virtualizes host machine's hardware
    * VMWare and VirtualBox
* containers
    * built from a recipe or build file
    * can run as an "image" or as a shell
    * relies on host kernel
    * Docker and Singularity

### networking 
* application layer
    * web servers, ssh, file share
* transport / protocol layer
    * TCP - handshake protocol where the connecting system and the system being connected to
        are constantly in communcation about recieving packets
    * UDP - the connecting system is going to request information, and the system being connect to doesn't care if you got it or if was correct.  
    * Ports (and some common services on those common ports)
        * SSH or SFTP runs on port 22
        * HTTP runs on port 80 
        * HTTPS runs on port 443
* network / internet layer
    * subnets - filter what is seen as "local" traffic
    * routes
    * ip - outside of my system - assign to a system (we can base this on a MAC address for some hardware verification if wanted)
        * public ip - this would access global communcation 
        * private ip - usually behind a router that then allows communcation with the outside world
    * gateway
    * dns (hostname)
    * dhcp
* physical layer
    * network interfaces (can be found with ifconfig in linux or with ipconfig in Windows)
        * Linux list these as eth0, wifi0, lo
        * Windows 
    * MAC addresses - these are "fingerprints" for hardware interfaces (or their vitrual counterparts)
* private networks (and their virtual counterparts)
* role of a router (virtual or physical)
    * directs traffic usually from a private network to a public network / server and back again
* role of firewalls locally (iptables) and by a specific device (for a network)
* http vs https - hypertext transfer protocol
    * HTTPS - digital certificates - from a certificate authority
        * encrypted connection between connecting system and server




Final Exam Details:
Open on Monday, 4/27, from 9:00 AM to 11:59 PM
You get two (2) hours from when you start the exam
You may use an electronic or printed "cheat sheet" as well as a terminal you have access to (including your AWS instance)
If I see the same words as are on my slides, much disappointment shall occur (and grade shall reflect)
TODO: Quiz 3 visibility

Additional due dates:
Lab 08 - 4/24 (please include Lab08 extra credit with this submission)
Lab redo - 4/24
Extra Credit "Lab" - 5/1