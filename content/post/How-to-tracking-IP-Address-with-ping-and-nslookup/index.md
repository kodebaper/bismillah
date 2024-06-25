+++
title = 'How to Tracking IP Address With Ping and Nslookup'
date = 2024-06-25T22:22:38+07:00
description = "Like the part that I previously explained in hacking activities is information gathering, while in information gathering things that are usually collected include"
tags = [
    "hacking",
    "information-gathering",
    "ethical-hacking",
    "pentester",
]
categories = [
    "cyber-security",
    "redteam",
    "recon",
]
series = ["Themes Guide"]
aliases = ["hacking-series"]
image = "recon2.jpg"
+++


### main topic
Like the part that I previously explained in hacking activities is information gathering, while in information gathering things that are usually collected include
IP Address
username
email address
operating system
if what we are targeting is a website, of course, we also have to know what technology is used on our target website, both the programming language used, the database used.
there are at least two types in the process of gathering information, 


### **1. active information gathering**

active information gathering is when we collect the information we need and then do packet exchange with the target, an example here is, for example, doing social engineering


### **2. passive information gathering**

We collect target information through third parties, this source can be obtained through search engines to collect target data.
there is nothing that has to be done from the two points above, which is using any method as long as we can get the data from the target we need.
the tools we can use include ping, whois, nslookup, whatweb, theHarvester, Hunter.io, sharelock. we will start with the simplest tool, namely PING through the terminal. the way this tool works is that PING will send ICMP (INTERNET CONTROL MESSAGE PROTOCOL) to a website for diagnostics. This activity is legal and does not break the law.

`````````
~$ ping kominfo.go.id 
PING kominfo.go.id (45.60.36.49) 56(84) bytes of data.
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=1 ttl=57 time=6.42 ms
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=2 ttl=57 time=5.91 ms
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=4 ttl=57 time=14.3 ms
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=5 ttl=57 time=4.08 ms
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=6 ttl=57 time=5.23 ms
64 bytes from 45.60.36.49 (45.60.36.49): icmp_seq=7 ttl=57 time=4.27 ms
^C
--- kominfo.go.id ping statistics ---
7 packets transmitted, 6 received, 14.2857% packet loss, time 6019ms
rtt min/avg/max/mdev = 4.080/6.708/14.344/3.513 ms

`````````

we found the website kominfo.go.id this is 45.60.36.49, this is important for us to do vulnerability analysis or exploitation.

Another tool that we will try to use nslookup, how to use just type it back in the terminal, and the result will be like below

````````````````
~$ nslookup kominfo.go.id
 Server:		127.0.0.53 Address:	127.0.0.53#53
Non-authoritative answer: 
Name:	kominfo.go.id Address: 45.60.36.49 
Name:	kominfo.go.id Address: 45.60.34.49 
Name:	kominfo.go.id Address: 2001:df2:a600::10
````````````````

This information will also provide a complete IP address related to the IP address using active information gathering.
for the next method, we can do passive information gathering, for example, here you can use a search engine through a site that provides services to check the IP address of a website, in this case, we can use the IP Checker website, for this stage I will not give an example. please check via website (ip-checker.info)

We will continue this article to the next step which is **to create an ip checker tool in Python**