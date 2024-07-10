+++
title = 'Day 2 Penetration Testing Challenge "cyber security basics practice"'
date = 2024-06-29T22:39:59+07:00
description = "At this stage I will explain what I did on day 2 of learning ethical hacking as a pentester. What I explain here is large-scale in the scope of practice, so to deepen it requires exploration from each of us to dig deeper in learning. "
tags = [
    "hacking",
    "information-gathering",
    "ethical-hacking",
    "Pentester-SERIES",
]
categories = [
    "cyber-security",
    "redteam",
    "Pentester-SERIES",
]
series = ["Themes Guide"]
aliases = ["hacking-series"]
image = "day2.png"
+++

### Main Topic
At this stage I will explain what I did on day 2 of learning ethical hacking as a pentester. What I explain here is large-scale in the scope of practice, so to deepen it requires exploration from each of us to dig deeper in learning. Especially in terms of flying hours to try often and consistently.

In the previous series of articles, I have explained how I already have about 12 years of experience in the use of the Linux operating system, but I need to keep repeating in terms of learning and recording it in the learning documentation through this article on my personal blog.

At this stage I will show the basic skills that must be understood, then you must learn more deeply outside this article according to your needs and abilities in mastering the operating system for hacking, Kali Linux of course.

### Basic skills
1. understand the Kali Linux operating system in outline and thoroughly

    This operating system is not the same as the operating system you may be using right now, for example if you are using the Windows operating system or even Mac OS. Then in Kali Linux you will find different things like
    - How to install an application in the OS using commands in the terminal
    - Perform an OS update
    - Delete certain applications and 
    - Some document processing applications, audio and video players that will be different.

2. Using the TERMINAL application

    This application is very important in my opinion, because this application is very powerful to execute a job in the operating system using only certain command lines, for example to install an application using only this command

    ```
    ~$ sudo apt install 'application-name'
    ``` 
    
    Or if you want to upgrade the Kali Linux operating system, you only need to type this command line
    
    ```
     ~$ sudo apt update 
    ```

     Below is an example of using the terminal command line in Kali Linux and operating systems derived from DEBIAN, this is a small example that I included for more complete you can search for additional knowledge about the command line that is more complete in other learning resources.
     

    #### Command Line in Terminal

    ```
    ~$ cd <directory>
        This command is used to move directories

    ~$ pwd
        This command is used to display the current directory path

    ~$ mkdir
        This command is used to create a new directory

    ~$ cp
        This command is used to copy a file and directory including its contents

    ~$ touch
        This command is used to create an empty file

    ~$ mv
        This command is used to move from one directory to another directory

    ~$ grep
        This command is used to search for strings in files

    ~$ sudo apt update
        This command is used to update the operating system

    ~$ sudo
        This command is used to execute commands as the superuser

    ~$ sudo su
       This command is used to switch from being a normal user to being a super user

    ~$ nano file.txt
        This command is used to open a file in .txt format.

    ~$ chmod
        This command is used to change the read, write and execute permissions of a file.

    ~$ uname
        This command is used to display information about the device's kernel, name, and hardware.

    ~$ history
        This command displays previously executed commands.

    ~$ ifconfig
        This command displays the system network interface and its configuration.

    ~$ echo 
        This command displays the contents of a message as standard output.

    ~$ nslookup
        This command is used to look up domain IP information and vice versa

    ~$ hostname
        This command displays the system hostname.

    ~$ nano, vi, jed
    This command is used to edit with a text editor.

    ~$ kill
        This command is used to kill a process running on the operating system.
    ```

3. Don't expect more from the graphical interface

    This is no less important, if you start using Kali Linux for learning purposes in the world of hacking, you will intersect a lot with the command line to perform an action, most of the penetration testing will be done with the command line. For that, enjoy the command line.

### Hacking Tips

is about hard work, consistency, and persistence.
Although this is a start, this is an important note to remind myself how to have knowledge. We have to work hard to learn continuously with consistency and perseverance.