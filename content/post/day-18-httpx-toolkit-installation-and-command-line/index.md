+++
title = 'Day 18 Httpx Toolkit Installation and Command Line'
date = 2025-01-23T15:15:24+07:00
description = "How to install the httpx toolkit and how to use it"
tags = [
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
image = "pentest1.png"
+++

``````
sudo apt install httpx-toolkit

or

go install -v github.com/projectdiscovery/httpx/cmd/httpx@latest

after done, for this installation you can following this step bellow

┌──(kali㉿kali)-[~]
└─$ ls
Desktop    Documents  go                Music     Public   Templates
dirsearch  Downloads  hostingerBBP.txt  Pictures  reports  Videos
                                                                                                              
┌──(kali㉿kali)-[~]
└─$ cd go       
                                                                                                         
┌──(kali㉿kali)-[~/go]
└─$ ls 
bin  pkg
                                                                                                        
┌──(kali㉿kali)-[~/go]
└─$ cd bin 
                                                                                                        
┌──(kali㉿kali)-[~/go/bin]
└─$ ls
httpx
                                                                                                    
┌──(kali㉿kali)-[~/go/bin]
└─$ sudo cp httpx /usr/local/bin 

``````

this is a command line to search active subdomain, after scanning with subfinder tool

```````
httpx-toolkit -l logreport.txt -o active-logreport.txt -mc 200
```````