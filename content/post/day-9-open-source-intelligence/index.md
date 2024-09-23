+++
title = 'Day 9 Open Source Intelligence'
date = 2024-09-04T10:20:13+07:00
description = "This article discusses the use of tools that can help gather information about a target for exploitation or other purposes, such as finding all social media accounts belonging to the target"
tags = [
    "OSINT",
    "information-gathering",
    "ethical-hacking",
    "Pentester-SERIES",
]
categories = [
    "OSINT",
    "cyber-security",
    "redteam",
    "Pentester-SERIES",
]
series = ["Themes Guide"]
aliases = ["hacking-series"]
image = "day9.png"
+++

### Main Topics
This article discusses the use of tools that can help gather information about a target for exploitation or other purposes, such as finding all social media accounts belonging to the target. 

> The author shares the article for learning purposes only and takes no responsibility for any misuse of the information provided.

### finduser

One of the tools mentioned is "finduser," which helps find various usernames from a target's social media. The installation process involves cloning the tool from GitHub and running it in the command line. The output provides information about the target on different platforms, which can be used for further mitigation according to specific needs.

### Finduser installation

> ~$ git clone https://github.com/mishakorzik/UserFinder



### It's time for us to use this tool
> ~$ cd finduser

> ~$ bash finduser


Then this is the result

````
santricyber@santricyber:~/UserFinder$ bash UserFinder.sh 
 __   __  ______  _______  ______      _______  ___  __    _  ______   _______  ______ 
|  | |  ||      ||       ||    _ |    |       ||   ||  |  | ||      | |       ||    _ |
|  | |  ||  ____||    ___||   | ||    |    ___||   ||   |_| ||  _    ||    ___||   | ||
|  |_|  || |____ |   |___ |   |_||_   |   |___ |   ||       || | |   ||   |___ |   |_||_ 
|       ||____  ||    ___||    __  |  |    ___||   ||  _    || |_|   ||    ___||    __  |
|       | ____| ||   |___ |   |  | |  |   |    |   || | |   ||       ||   |___ |   |  | |
|_______||______||_______||___|  |_|  |___|    |___||_|  |__||______| |_______||___|  |_|

             .:.:;.. UserFinder v1.0 Developer: misha korzhik ..;:.:.

[>] Input Username: santricyber

[>] Checking username santricyber on global info-stealer: 
[+] No result found

[>] Checking username santricyber on social networks: 
[+] Instagram:  Found! https://www.instagram.com/santricyber
[+] Facebook:  Found! https://www.facebook.com/santricyber
[+] Twitter:  Found! https://www.twitter.com/santricyber
[+] YouTube: Not Found!
[+] Blogger:  Found! https://santricyber.blogspot.com
[+] GooglePlus:  Found! https://plus.google.com/+santricyber/posts
[+] Reddit:  Found! https://www.reddit.com/user/santricyber
[+] Wordpress:  Found! https://santricyber.wordpress.com
[+] Pinterest:  Found! https://www.pinterest.com/santricyber
[+] Github:  Found! https://www.github.com/santricyber
[+] Tumblr: Not Found!
[+] Flickr:  Found! https://www.flickr.com/photos/santricyber
[+] Steam: Not Found!
[+] Vimeo: Not Found!
[+] SoundCloud:  Found! https://soundcloud.com/santricyber
[+] Disqus:  Found! https://disqus.com/santricyber
[+] Medium:  Found! https://medium.com/@santricyber
[+] DeviantART: Not Found!
[+] VK:  Found! https://vk.com/santricyber
[+] About.me: Not Found!
[+] Spotify: Not Found!
[+] MixCloud: Not Found!
[+] Scribd:  Found! https://www.scribd.com/santricyber
[+] Badoo: Not Found!
[+] Patreon: Not Found!
[+] BitBucket:  Found! https://bitbucket.org/santricyber
[+] CashMe:  Found! https://cash.me/santricyber
[+] Behance:  Found! https://www.behance.net/santricyber
[+] GoodReads: Not Found!
[+] Instructables:  Found! https://www.instructables.com/member/santricyber
[+] Keybase:  Found! https://keybase.io/santricyber
[+] Kongregate: Not Found!
[+] LiveJournal: Not Found!
[+] AngelList:  Found! https://angel.co/santricyber
[+] last.fm: Not Found!
[+] Dribbble: Not Found!
[+] Codecademy: Not Found!
[+] Gravatar:  Found! https://en.gravatar.com/santricyber
[+] Pastebin:  Found! https://pastebin.com/u/santricyber
[+] Foursquare:  Found! https://foursquare.com/santricyber
[+] Roblox:  Found! https://foursquare.com/santricyber
[+] Gumroad:  Found! https://www.gumroad.com/santricyber
[+] Newgrounds: Not Found!
[+] Wattpad:  Found! https://www.wattpad.com/user/santricyber
[+] Canva:  Found! https://www.canva.com/santricyber
[+] CreativeMarket:  Found! https://creativemarket.com/santricyber
[+] Trakt: Not Found!
[+] 500px:  Found! https://500px.com/santricyber
[+] Buzzfeed: Not Found!
[+] TripAdvisor:  Found! https://tripadvisor.com/members/santricyber
[+] HubPages: Not Found!
[+] Contently:  Found! https://santricyber.contently.com
[+] Houzz:  Found! https://houzz.com/user/santricyber
[+] blip.fm:  Found! https://blip.fm/santricyber
[+] Wikipedia:  Found! https://www.wikipedia.org/wiki/User:santricyber
[+] HackerNews: Not Found!
[+] CodeMentor: Not Found!
[+] ReverbNation: Not Found!
[+] Designspiration: Not Found!
[+] Bandcamp: Not Found!
[+] ColourLovers:  Found! https://www.colourlovers.com/love/santricyber
[+] IFTTT: Not Found!
[+] Ebay:  Found! https://www.ebay.com/usr/santricyber
[+] Slack: Not Found!
[+] OkCupid: Not Found!
[+] Trip:  Found! https://www.trip.skyscanner.com/user/santricyber
[+] Ello:  Found! https://ello.co/santricyber
[+] Tracky: Not Found!
[+] Tripit:  Found! https://www.tripit.com/people/santricyber#/profile/basic-info
[+] Basecamp: Not Found!
[+] Saved: 

````

From the above results we get a lot of information about targets on several platforms which we can then do further mitigation, of course we use according to what we need from these assets.

### Bug Bounty Helper

Another tool recommended for finding information about a target is a website called "Bug Bounty Helper." This website is useful for testing website vulnerabilities. It provides a list of vulnerabilities and information that can be obtained from the target website, such as exposed configuration files, database files, login pages, SQL errors, and more. The author also shares some additional web references for doing open-source intelligence (OSINT) activities, including websites for analyzing data, checking phone number owners, Twitter engineering, social engineering, image search, and username verification.

````
https://dorks.faisalahmed.me/

````

by using this website there are several things that we can get from the target website that we will test the level of vulnerability, including:

`````

🔍 Directory listing vulnerabilities
🔍 Exposed Configuration files
🔍 Exposed Database files
🔍 Find WordPress
🔍 Exposed log files
🔍 Backup and old files
🔍 Login pages
🔍 SQL errors
🔍 Publicly exposed documents
🔍 phpinfo()
🔍 Finding Backdoors
🔍 Install / Setup files
🔍 Open Redirects
🔍 Apache STRUTS RCE
🔍 Find Pastebin entries
🔍 Employees on LINKEDIN
🔍 .htaccess sensitive files
🔍 Find Subdomains
🔍 Find Sub-Subdomains
🔍 Find WordPress #2
🔍 Find WordPress [Wayback Machine]
🔍 Search in GITHUB
🔍 Search in OpenBugBounty
🔍 Search in Reddit
🔍 Test CrossDomain
🔍 Check in ThreatCrowd
🔍 Find .SWF file (Google)
🔍 Find .SWF file (Yandex)
🔍 Search SWF in WayBack Machine
🔍 Search in WayBack Machine #2
🔍 Search in WayBack Machine #3
🔍 Search in WayBack Machine [List/All]
🔍 Check in crt.sh
🔍 Check in CENSYS [IP4] | [DOMAINS] | [CERTS]
🔍 Search in SHODAN

`````

Then for extras I have some web references for doing OSINT that are quite helpful

``````
https://inteltechniques.com/menu.html   /analisa data menggunakan website ini
https://www.truecaller.com/    cek nama pemilik nomor telepon  
https://inteltechniques.com/menu.html
https://socialbearing.com/        twitter engineering
https://codeofaninja.com/tools/            social engineering
https://www.tineye.com
https://knowem.com/
https://checkusernames.com/     cek username
OSINT https://osintframework.com/

``````


Overall, the article aims to provide readers with tools and resources that can aid in gathering information about targets for cybersecurity purposes. It offers insights into techniques like finding usernames on social media platforms and identifying website vulnerabilities. The author encourages responsible use of the information and hopes that the article will contribute to learning about cyber security.

hope this article helps us to learn cyber security!