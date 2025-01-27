+++
title = 'Day 16 Port Scanning With Nmap'
date = 2025-01-22T21:52:37+07:00
description = "How to use Nmap for port scanning and vulnerability assessment mitigation"
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


### How to search Open port in domain/IP Address
```````
┌──(kali㉿kali)-[~]
└─$ nmap -sV -sC 178.0.0.0
```````

### 
````````
kali㉿kali)-[~]
└─$ sudo nmap -p- -sV 104.16.65.50     
[sudo] password for kali: 
Starting Nmap 7.92 ( https://nmap.org ) at 2025-01-21 14:48 WIB
Nmap scan report for 104.16.65.50
Host is up (0.071s latency).
Not shown: 65522 filtered tcp ports (no-response)
PORT     STATE SERVICE  VERSION
80/tcp   open  http     Cloudflare http proxy
443/tcp  open  ssl/http Cloudflare http proxy
2052/tcp open  http     Cloudflare http proxy
2053/tcp open  ssl/http nginx
2082/tcp open  http     Cloudflare http proxy
2083/tcp open  ssl/http nginx
2086/tcp open  http     Cloudflare http proxy
2087/tcp open  ssl/http nginx
2095/tcp open  http     Cloudflare http proxy
2096/tcp open  ssl/http nginx
8080/tcp open  http     Cloudflare http proxy
8443/tcp open  ssl/http Cloudflare http proxy
8880/tcp open  http     Cloudflare http proxy

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 156.03 seconds.

another command,

`````
$ sudo nmap Target_IP_Address/24

$ nmap -sP -vv --packet-trace 10.10.209.108

$ nmap -A -Pn -p 443 targetdomain.com.


user this command to scan

$ $ nmap -sV -sC 116.206.232.173

after get the result, you can use this command to get deep information port

$ nmap 116.0.0.0 -Pn -p 80,443,3306 -sV -A 

`````````
Command Breakdown:
- p 80,22,443,3306: Specifies the ports to scan, focusing on those discovered earlier.
- sV: Enables version detection to identify the software and version running on open ports.
- A: Activates advanced features, including OS detection, version detection, script scanning, and traceroute.

Thank you:)