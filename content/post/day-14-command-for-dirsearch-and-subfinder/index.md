+++
title = 'Day 14 Command for Dirsearch and Subfinder'
date = 2025-01-14T06:30:58+07:00
description = "This is a simple command that allows you to run the dirsearch and subfinder, dirsearch, HTTPX-Toolkit"
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

from another time, i'm just trying to hunting bug in website using dirsearch tool, but I sometimes forget use of the command :) 
``````

$ dirsearch https://yourtarget-domain.com/ -i

$ dirsearch https://yourtarget-domain.com/ -i 200

$ dirsearch -u http://example.com/

$ dirsearch -u http://example.com/ -w /position/wordlist.txt
[This command scans directories on the basis of your wordlis]

$ dirsearch -u http://example.com/ -w /position/wordlist.txt — include-status=200

$ dirsearch -u http://example.com/ -w /position/wordlist.txt -e php,xml,html,js
[this command to scans on the basis file with extensions you want e.g.html,js,xml]

$ subfinder -d yourtarget-domain.com -o logreport.txt

$ httpx-toolkit -l logreport.txt -o active-logreport.txt -mc 200

``````