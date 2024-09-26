+++
title = 'Day 11 Easy Burpsuite Configuration With External Browser'
date = 2024-09-25T11:52:27+07:00
description = "process of configuring the Burpsuite application for external browsers on a Linux operating system"
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
image = "day11.png"
+++

### Explainations

The article discusses the process of configuring the Burpsuite application for external browsers on a Linux operating system. It involves downloading Burpsuite, installing the latest version of Firefox, and installing the FoxyProxy extension with proper configuration.

### Preparations

There are several things that we need to prepare of course to be able to use the Burpsuite application for the purposes of vulnerability testing or security mitigation of a system.

1. We need to download the Burpsuite application first as the main application that we will use.

2. Install the latest version of Firefox Web Browser

3. Install the FoxyProxy extension on the Firefox Web Browser that has been installed on our Kali Linux operating system

### Implementations

> Burpsuite Download

We need to download the burpsuite application first on this official portswigger page [Burpsuite-Download](https://portswigger.net/burp/communitydownload) and install it as usual on our kali linux operating system.

> Install the latest version of Firefox Web Browser

Usually on the Kali Linux default operating system at the first time of installation, the firefox browser is automatically installed, but keep in mind my experience at that time the firefox installed on the kali linux operating system was an old version.

This results in the FoxyProxy Extension cannot be installed on the firefox browser, so make sure the Firefox Web Browser version installed on your Kali Linux operating system is the latest version, if not the latest version then please update first.

> Installation of FoxyProxy extension on Firefox Web Browser

At this stage for the installation process that must be done, namely: 

1. We have to enter the extension page on the firefox web to install Foxyproxy, installing the extension is so easy for that complete the entire installation process, for the extension page display as shown below

![Extension-Page](/post/images/add.png)

2. After the installation process is complete, we enter the next stage, we configure FoxyProxy, follow the configuration as shown below.

![Extension-Page](/post/images/setup.png)

3. At the next configuration stage, we need to enter the burpsuite certificate by downloading it through accessing this link http://burpsuite as shown below.

![Extension-Page](/post/images/certdown.png)

Then we configure the import certificate through the following page, enter the certificate that has been downloaded as on the page above

![Extension-Page](/post/images/setcert.png)

after that the next step we only need to enter the certificate file in the following configuration

![Extension-Page](/post/images/importcert.png)

if already at this stage the entire process of configuring our burpsuite and foxyproxy on the external browser has been completed. Hope this article was useful!

