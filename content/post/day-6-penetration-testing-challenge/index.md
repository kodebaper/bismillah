+++
title = 'Day 6 Penetration Testing Challenge "Reconnaissance PART 2 Dirsearch, Subfinder and HTTPX-Toolkit"'
date = 2024-06-29T22:48:46+07:00
description = ""
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
image = "day6.png"
+++

### Main Topics
In in this article, I will note some common commands when performing reconnaissance using tools **Subfinder, Dirsearch, and HTTPX-Toolkit**. Of course, there are many commands that can be used when using these tools, and I will not discuss them in their entirety or in detail. I will show some of the command lines that I often use.

But before that, in accordance with the previous article, I will give tips on how to find out which subdomains are still active from the subdomains we obtained from the scan results using **Subfinder** tools. The method is as follows.

### Find the Active 200 Server Response Directory
Finding an open directory will make it easier, because the dirsearch application will automatically provide a report on the results of scanning only response server code 200. To do this, simply use the following command on dirsearch

````
$ dirsearch https://yourtarget-domain.com/ -i 200
````

The HTTPX Toolkit application will sort out the active subdomains that we got from the scan results using the Subfinder tools

### Dirsearch command line
To use the Dirsearch tool, we can use this tool in the reconnaissance process, use this command

````
$ dirsearch https://yourtarget-domain.com/
````
The result of this will select all the directories that are linked from the target website target.

### Subfinder command line
Using the Subfinder tool to find the subdomains of the target domain that we want to scan for vulnerabilities is as follows, but before that I need to explain the function of the command below. **-o** is the output of the scan results that we will save in the **txt** file, then **logreport.txt** is the file name where we will save all the subdomains from the scan using the Subfinder tool.

````
subfinder -d yourtarget-domain.com -o logreport.txt
````

### Finding active subdomains using HTTPX-TOOLKIT

`````
httpx-toolkit -l logreport.txt -o active-logreport.txt -mc 200
`````

The explanation is as follows:
-l is a list of subdomains that we have previously obtained from the results of scanning with the subfinder tool, but we cannot be sure that all the scanned subdomains are active, so the role of the **httpx-tool** tool is used as a filter to collect only active subdomains.

- -o is the output of active subdomains, then we save it in a file called **active-logreport.txt**.

- -mc 200 is the code to run **httpx-toolkit** and find only active subdomain results that will be generated.

Thank you, we will meet in the next article.