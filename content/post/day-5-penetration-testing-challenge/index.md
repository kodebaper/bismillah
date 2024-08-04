+++
title = 'Day 5 Penetration Testing Challenge "Reconnaissance PART 1"'
date = 2024-06-29T22:46:04+07:00
description = " is a reconnaissance tool or often known as Subfinder. It is a subdomain enumerator to find subdomains from the main domain of the target we are targeting."
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
image = "day5.png"
+++

### Main Topics

Discussing the Reconnaissance phase is an introductory phase to getting started with penetration testing using the Subfinder and Dirsearch tools. For this, I need to explain the understanding of these two tools

### 1. **Subfinder** 
    is a reconnaissance tool or often known as Subfinder. It is a subdomain enumerator to find subdomains from the main domain of the target we are targeting.

```
┌──(infosec㉿infosec)-[~]
└─$ subfinder -d mytarget.com -o report.txt
[INF] Detected old /home/infosec/.config/subfinder/config.yaml config file, trying to migrate providers to /home/infosec/.config/subfinder/provider-config.yaml
[INF] Migration successful from /home/infosec/.config/subfinder/config.yaml to /home/infosec/.config/subfinder/provider-config.yaml.

               __    _____           __         
   _______  __/ /_  / __(_)___  ____/ /__  _____
  / ___/ / / / __ \/ /_/ / __ \/ __  / _ \/ ___/
 (__  ) /_/ / /_/ / __/ / / / / /_/ /  __/ /    
/____/\__,_/_.___/_/ /_/_/ /_/\__,_/\___/_/

                projectdiscovery.io

[INF] Current subfinder version v2.6.0 (outdated)
[INF] Loading provider config from /home/infosec/.config/subfinder/provider-config.yaml
[INF] Enumerating subdomains for mytarget.com

```

I did not include the target domain that I tried for privacy reasons, for that I illustrated the main target domain with **mytarget.com** here we will get results where the main target domain has subdomains according to what it has. With this tool we can see how many subdomains there are.

If you look at the command that I typed there is the **-o report.txt** parameter, this means that -o is the output that will be generated so that I can save it into the **report.txt** file, we can use this to make it easier to create a scanning report for analysis at a later date.

but after we do scanning with the command **$ subfinder -d mytarget.com -o report.txt** all subdomains will be scanned by the subfinder application without us knowing whether the subdomain is active or not, for that in the next article I will write an article on how to use a tool to select which subdomains are active and inactive. The tool is called **HTTPX TOOL**

### 2. Tools for scanning directories on a target website using **DIRSEARCH**
    This tool will make it easier for us to find any directories including sensitive files or not from a target that we will test for weaknesses, besides being open source this tool is also easy to understand and use by even a beginner. And if a target is very vulnerable we can get sensitive files from the system.

```
┌──(infosec㉿infosec)-[~]
└─$ dirsearch -u mytarget.com            


  _|. _ _  _  _  _ _|_    v0.4.3                                                                                                                             
 (_||| _) (/_(_|| (_| )                                                                                                                                      
                                                                                                                                                             
Extensions: php, aspx, jsp, html, js | HTTP method: GET | Threads: 25 | Wordlist size: 11460

Output File: /home/infosec/reports/_mytarget.com/_24-07-10_15-50-14.txt

Target: https://mytarget.com/

[15:50:14] Starting:                                                                                                                                         
[15:50:15] 400 -    1KB - /!.gitignore
[15:50:16] 400 -    1KB - /!.htaccess                                       
[15:50:16] 400 -    1KB - /!.htpasswd                                       
[15:50:16] 400 -    1KB - /+CSCOT+/oem                                      
[15:50:16] 400 -    1KB - /+CSCOE+/session_password.html                    
[15:50:16] 400 -    1KB - /+CSCOE+/logon.html
[15:50:16] 400 -    1KB - /+CSCOT+/oem-customization?app=AnyConnect&type=oem&platform=..&resource-type=..&name=%2bCSCOE%2b/portal_inc.lua
[15:50:16] 400 -    1KB - /+CSCOT+/translation                              
[15:50:17] 400 -    1KB - /+CSCOT+/translation-table?type=mst&textdomain=/%2bCSCOE%2b/portal_inc.lua&default-language&lang=../
[15:50:18] 400 -    1KB - /.config/psi+/profiles/default/accounts.xml       
[15:50:18] 200 -    8KB - /.DS_Store                                        
[15:50:20] 403 -  199B  - /.ht_wsr.txt                                      
[15:50:20] 403 -  199B  - /.htaccess.bak1                                   
[15:50:20] 403 -  199B  - /.htaccess.orig                                   
[15:50:20] 403 -  199B  - /.htaccess_orig
[15:50:20] 403 -  199B  - /.htaccess_extra
[15:50:20] 403 -  199B  - /.htaccessBAK                                     
[15:50:20] 403 -  199B  - /.htaccess.save
[15:50:20] 403 -  199B  - /.htaccessOLD2
[15:50:20] 403 -  199B  - /.htaccessOLD
[15:50:20] 403 -  199B  - /.htaccess.sample
[15:50:20] 403 -  199B  - /.htaccess_sc                                     
[15:50:20] 403 -  199B  - /.htm
[15:50:20] 403 -  199B  - /.html
[15:50:20] 403 -  199B  - /.htpasswd_test                                   
[15:50:20] 403 -  199B  - /.httr-oauth
[15:50:20] 403 -  199B  - /.htpasswds                                       
[15:50:20] 400 -    1KB - /.idea/workspace(6).xml                           
[15:50:20] 400 -    1KB - /.idea/workspace(4).xml
[15:50:20] 400 -    1KB - /.idea/workspace(5).xml                           
[15:50:20] 400 -    1KB - /.idea/workspace(3).xml                           
[15:50:20] 400 -    1KB - /.idea/workspace(2).xml
[15:50:20] 400 -    1KB - /.idea/workspace(7).xml                           
[15:50:26] 400 -    1KB - /;/login                                          
[15:50:26] 400 -    1KB - /;/admin                                          
[15:50:26] 400 -    1KB - /;json/                                           
[15:50:26] 400 -    1KB - /;admin/                                          
[15:50:26] 400 -    1KB - /;/json                                           
[15:50:26] 400 -    1KB - /;login/                                          
[15:50:26] 400 -    1KB - /@
[15:50:26] 400 -    1KB - /\..\..\..\..\..\..\..\..\..\etc\passwd
[15:50:28] 400 -    1KB - /a%5c.aspx                                        
[15:50:29] 400 -    1KB - /actuator/;/beans                                 
[15:50:29] 400 -    1KB - /actuator/;/configprops                           
[15:50:29] 400 -    1KB - /actuator/;/conditions
[15:50:29] 400 -    1KB - /actuator/;/auditLog
[15:50:29] 400 -    1KB - /actuator/;/caches
[15:50:29] 400 -    1KB - /actuator/;/configurationMetadata
[15:50:29] 400 -    1KB - /actuator/;/features
[15:50:29] 400 -    1KB - /actuator/;/exportRegisteredServices
[15:50:29] 400 -    1KB - /actuator/;/events
[15:50:29] 400 -    1KB - /actuator/;/auditevents
[15:50:29] 400 -    1KB - /actuator/;/dump
[15:50:29] 400 -    1KB - /actuator/;/env
[15:50:29] 400 -    1KB - /actuator/;/health
[15:50:29] 400 -    1KB - /actuator/;/healthcheck
[15:50:29] 400 -    1KB - /actuator/;/flyway
[15:50:29] 400 -    1KB - /actuator/;/heapdump
[15:50:29] 400 -    1KB - /actuator/;/integrationgraph                      
[15:50:29] 400 -    1KB - /actuator/;/liquibase
[15:50:29] 400 -    1KB - /actuator/;/info
[15:50:29] 400 -    1KB - /actuator/;/prometheus
[15:50:29] 400 -    1KB - /actuator/;/sessions
[15:50:29] 400 -    1KB - /actuator/;/logfile
[15:50:29] 400 -    1KB - /actuator/;/trace
[15:50:29] 400 -    1KB - /actuator/;/jolokia
[15:50:29] 400 -    1KB - /actuator/;/mappings
[15:50:29] 400 -    1KB - /actuator/;/loggers
[15:50:29] 400 -    1KB - /actuator/;/releaseAttributes
[15:50:29] 400 -    1KB - /actuator/;/scheduledtasks
[15:50:29] 400 -    1KB - /actuator/;/metrics
[15:50:29] 400 -    1KB - /actuator/;/loggingConfig
[15:50:29] 400 -    1KB - /actuator/;/refresh
[15:50:29] 400 -    1KB - /actuator/;/sso
[15:50:29] 400 -    1KB - /actuator/;/httptrace
[15:50:29] 400 -    1KB - /actuator/;/springWebflow
[15:50:29] 400 -    1KB - /actuator/;/ssoSessions
[15:50:29] 400 -    1KB - /actuator/;/registeredServices
[15:50:29] 400 -    1KB - /actuator/;/threaddump
[15:50:29] 400 -    1KB - /actuator/;/status
[15:50:29] 400 -    1KB - /actuator/;/shutdown
[15:50:29] 400 -    1KB - /actuator/;/statistics
[15:50:30] 400 -    1KB - /actuator/;/resolveAttributes                     
[15:50:31] 400 -    1KB - /admin/%3bindex/                                  
[15:50:34] 400 -    1KB - /admin;/                                          
[15:50:34] 400 -    1KB - /Admin;/                                          
[15:50:45] 403 -  199B  - /application                                      
[15:50:46] 403 -  199B  - /application/cache/                               
[15:50:46] 403 -  199B  - /application/configs/application.ini
[15:50:46] 403 -  199B  - /application/
[15:50:46] 403 -  199B  - /application/logs/                                
[15:50:46] 403 -  199B  - /assets/                                          
[15:50:46] 301 -  258B  - /assets  ->  http://mytarget.com/assets/
[15:50:53] 200 -  625B  - /composer.json                                    
[15:50:53] 200 -   47KB - /composer.lock                                    
[15:50:55] 200 -    6KB - /contributing.md                                  
[15:50:57] 302 -    0B  - /dashboard  ->  https://mytarget.com/login
[15:50:58] 302 -    0B  - /dashboard/  ->  https://mytarget.com/login
[15:51:11] 400 -    1KB - /index.php::$DATA                                 
[15:51:13] 400 -    1KB - /jkstatus;                                        
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/help/*
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/jfrStart/filename=!/tmp!/foo
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/vmLog/disable
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/jvmtiAgentLoad/!/etc!/passwd
[15:51:13] 400 -    1KB - /jolokia/read/java.lang:type=*/HeapMemoryUsage
[15:51:13] 400 -    1KB - /jolokia/exec/java.lang:type=Memory/gc
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/vmLog/output=!/tmp!/pwned
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/vmSystemProperties
[15:51:13] 400 -    1KB - /jolokia/exec/com.sun.management:type=DiagnosticCommand/compilerDirectivesAdd/!/etc!/passwd
[15:51:13] 400 -    1KB - /jolokia/search/*:j2eeType=J2EEServer,*           
[15:51:13] 400 -    1KB - /jolokia/write/java.lang:type=Memory/Verbose/true 
[15:51:13] 400 -    1KB - /jolokia/read/java.lang:type=Memory/HeapMemoryUsage/used
[15:51:15] 200 -  689B  - /license.txt                                      
[15:51:17] 302 -    0B  - /logout  ->  https://mytarget.com/login
[15:51:18] 302 -    0B  - /logout/  ->  https://mytarget.com/login
[15:51:24] 400 -    1KB - /New%20folder%20(2)                               
[15:51:30] 400 -    1KB - /phpmyadmin!!                                     
[15:51:41] 400 -    1KB - /secure/ConfigurePortalPages!default.jspa?view=popular
[15:51:41] 400 -    1KB - /secure/ContactAdministrators!default.jspa        
[15:51:41] 400 -    1KB - /secure/QueryComponent!Default.jspa
[15:51:42] 403 -  199B  - /server-status                                    
[15:51:42] 403 -  199B  - /server-status/ 

```

This tool will provide clear information from a target website, it will show what directory information is in it that we have successfully scanned using the dirsearch tool, along with the Response Code that we can do to take the next step.

These 2 tools are a small example in the reconnaissance process in doing ethical hacking, I hope that anyone who learns this tool will learn more deeply in using this tool, because there are still very many functions and commands in its use.

See you in the next article.