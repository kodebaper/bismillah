+++
title = 'Solved Enforce HTTPS Unavailable for Your Site on Github'
date = 2024-06-25T22:06:26+07:00
description = "Two days after the custom domain process for my blog was on the github page, after waiting for the DNS propagation"
tags = [
    "tips&tricks",
    "programming",
    "static-website",
    "hugo-static",
]
categories = [
    "programming",
    "hugo-static",
    "bloging",
    "solved",
]
series = ["Themes Guide"]
aliases = ["static-website"]
image = "httpsgithub.jpg"
+++


### main topic
Two days after the custom domain process for my blog was on the github page, after waiting for the DNS propagation process which does take quite some time usually up to 1x24 hours and doing some configuration related to DNS on cloudflare, I encountered a new problem where my blog for SSL from the setting side on GitHub could not be activated as a result I could only activate the blog's SSL from the features on cloudflare but not for the GitHub Page settings , then what are the impacts if it's like this?
 
As for the impact you get from problems like what I'm experiencing, for example, the domain is still known as HTTP, not HTTPS when opened using a browser, where in the GitHub Page settings feature it is still stated that  `Your site is published at http://santricyber. com/` not  `Your site is published at https://santricyber.com/`. Then when I opened my blog using an internet connection at the office, I had to go through verification which stated that the page being opened was not secure. I also don't understand the Fortigate firewall device in the office where I work, doing verification like this on my blog.

### problem 
As for problem solvers to overcome this problem as follows:
 
1. **First delete the domain on the GitHub Page**
 
   I first delete the domain name that I entered in the GitHub Page settings, delete it then save it, just leave it blank first. In the example in the image below, I deleted the domain `santricyber.com ---> then SAVE` "adjust to your domain name to delete first okay"
 
Up here it's finished for matters of setting up domains on the GitHub Page.
 
2.  **Resetting the Management DNS on CloudFlare**
 
   after that I went to the settings on Management **DNS on CloudFlare** because from some of the references I read it was not the same as the settings from the DNS side that I did, then I made changes to **DNS on CloudFlare** 
 
The configuration is at least as described below.
 
 
 
       <<Settings while still wrong>>
       ------------------------------
       <Type>   <Name>         <Content>            <TTL>  <Proxy Status>
       A        www            185.199.108.153      Auto    Proxied
       CNAME    santricyber.com  santricyber.github.io  Auto    Proxied
       TXT      santricyber.com  google-site......    Auto    DNS Only
 
   From the settings for DNS on CloudFlare like this, of course it's not quite right, and results in the **HTTPS** activated in the *custom domain settings on the github page* for that it returns me study the documentation that is widely scattered on the internet in the arrangement between custom domains on GitHub and DNS Management on CloudFlare. Okay until here it's done,
 
3. **Return to custom domain settings on GitHub Page**
 
   After the second point above is finished, now what I do is fill in the domain name that previously did not want to 'checklist' the `Enforce HTTPS`, after filling it in then save it, after that we have to wait for the change to HTTPS and this feature cannot be checked yet because it takes time. After waiting about 20 minutes, I refreshed the custom domain page on GitHub and `Enforce HTTPS` can be activated by placing a check in the `Enforce HTTPS` section and changing the description on the custom domain GitHub Page to `Your site is published at https http://santricyber.com/`.
 
Until these three processes are completed, and problems like this are not always faced. Because in some cases custom domains on GitHub Pages can run smoothly without going through a process like this. Hopefully useful and eager to learn!