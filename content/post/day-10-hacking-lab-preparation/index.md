+++
title = 'Day 10 Hacking Lab Preparation'
date = 2024-09-09T21:47:11+07:00
description = "This article provides instructions on how to create an IDOR (Insecure Direct Object Reference) LAB on Kali Linux using VulnLab"
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
image = "day10.png"
+++

### Main Topics
1. This article provides instructions on how to create an IDOR (Insecure Direct Object Reference) LAB on Kali Linux using VulnLab. 

2. The necessary preparations include having Docker installed, which is needed to run the VulnLab image. 

3. The installation method is detailed in the official VulnLab page on Github. 

4. The VulnLab provides various types of vulnerabilities that can be tested, including IDOR attacks. 

### Preparation

Preparation that we must do to create an IDOR LAB on our Kali Linux operating system using VulnLab
1. docker
2. Vulnlab DockerHub

### Explanation

We need Docker to run the image of VulnLab later, here I will not explain how to install docker from scratch on the Kali Linux operating system, I assume you have installed docker. If you have not installed docker, please install it first.

I refer to the installation method on the official VulnLab page at the following link.

> [VulnLab-Github-Installation](https://github.com/Yavuzlar/VulnLab)

I explained a little on the official VulnLab page developed by Yavuzlar on Github explaining several types of vulnerabilities that can be tried using this Lab, including:

- SQL Injection
- Cross Site Scripting (XSS)
- Command Injection
- Insecure Direct Object References (IDOR)
- Cross Site Request Forgery (CSRF)
- XML External Entity (XXE)
- Insecure Deserialization
- File Upload
- File Inclusion
- Broken Authentication
- Race Condition
- Server Side Template Injection (SSTI)
- API Hacking
- Captcha Bypass
- Path Traversal


Here's how to install the Lab from VulnLab to try to simulate an IDOR attack

````
 docker run --name vulnlab -d -p 1337:80 yavuzlar/vulnlab:latest
````

then the next step

````
Go to http://localhost:1337
````

after that if we want to reuse the IDOR Lab that we have tried, we only need to run this command to use it again

````
docker run -d -p 1337:80 yavuzlar/vulnlab
````

The following is the Lab view of the VulnLab that we run

![IDOR-LABs](/post/images/idor.png)

Good luck!


Translated with DeepL.com (free version)