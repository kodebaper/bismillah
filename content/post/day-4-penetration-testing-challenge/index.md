+++
title = 'Day 4 Penetration Testing Challenge "Pentest-Notes"'
date = 2024-06-29T22:43:31+07:00
description = "In this article I would like to share some important notes about what I learned on day 4"
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
image = "day4.png"
+++

### Main Topic
Day 4 of learning Penetration testing I learned about the stages in the implementation of Hacking, at this stage I began to recognize the tools to do Hacking to test the vulnerability of a website. the tools I use are 2

1. Dirsearch
2. Subfinder

Of course I will not discuss the use of these two tools, but in detail I will explain in the next article according to what I have learned about the Dirsearch and Subfinder tools that I will later explain.

In this article, I would like to share some important notes about what I learned on day 4.

### Notes 1
1. Directories and Endpoints

    In the process of testing website vulnerabilities we need to test by looking for open directories from a target, but it is equally important that we also need to recognize Endpoints. 

    Endpoint is a security strategy that focuses on protecting digital devices, this endpoint is very important to gain access to the target system, so in addition to looking for loopholes through directories, we can also look for vulnerabilities through Endpoint files.

2. RESPONSE CODE

    We need to understand the response code from the server to know what it means, on another occasion in detail I will make a special article about the response code from a server, for example the 200 response code server successfully received, the 400 response code which means server client error. Of course this will be even more we will get a response code.

    More clearly this is a real example of my response code testing website vulnerabilities using the Dirsearch tool

    ```
    400 1KB http://yourtarget.com/actuator/;/prometheus
    400 1KB http://yourtarget.com/actuator/;/metrics
    403 564B http://yourtarget.com/admin/.config
    400 1KB http://yourtarget.com/admin;/
    400 1KB http://yourtarget.com/Admin;/
    403 564B http://yourtarget.com/admrev/.ftppass
    403 564B http://yourtarget.com/admpar/.ftppass
    200 3KB http://yourtarget.com/app
    200 3KB http://yourtarget.com/app/
    200 131B http://yourtarget.com/application/cache/
    200 131B http://yourtarget.com/application/logs/
    200 131B http://yourtarget.com/application/
    301 178B http://yourtarget.com/application -> REDIRECTS TO: http://yourtarget.com/application/
    301 178B http://yourtarget.com/assets -> REDIRECTS TO: http://yourtarget.com/assets/
    ```

3. Vulnerabilities are categorized into 5 types of vulnerabilities namely

    - P5 informational
    - P4 low
    - P3 medium
    - P2 high
    - P1 critical

4. zero.web

    This command can be used to search for website vulnerabilities that only use HTTP with the Dirsearch tool.

5. Server Path

    The results of vulnerability findings that contain information about the server Path and Server Address are included in the vulnerability findings, an example of a Server Path is **Target.com/info.php**

### Note 2

1. WAF

    WAF is WEB APPLICATION FIREWALL is a server to secure the main server, a system protected by WAF tends to be more difficult to test for security even though it still has many possibilities to be penetrated.

2. WAF BYPASS

    To avoid the WEB APPLICATION FIREWALL system we can bypass using Public IP access.

3. IP ORIGIN

    IP Address is an original IP Address that directly leads to the website system or website address directly.

4. SHODAN

    An alternative to hacking while using the **Shodan** application, we can use the **Hunter.how** application.

See you in the next article.