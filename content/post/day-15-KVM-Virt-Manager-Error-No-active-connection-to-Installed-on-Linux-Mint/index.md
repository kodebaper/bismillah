+++
title = 'Day 15 KVM Virt Manager Error: No Active Connection to Installed on Linux Mint'
date = 2025-01-17T20:44:01+07:00
description = "Solved: KVM Virt Manager Linux Mint error no active connection"
tags = [
    "tips&tricks",
    "programming",
    "static-website",
    "hugo-static",
    "linux-tips",
]
categories = [
    "programming",
    "hugo-static",
    "bloging",
    "Linux",
]
series = ["Themes Guide"]
aliases = ["static-website"]
image = "ubuntu.jpg"
+++

When I try to install a new virtual machine in virt-manager Linux Mint virtualization, I get an error message error no active connection. In this situation, I'll just go to Terminal and then paste this command to run and fix it.

``````
$ sudo chown $USER:$USER /var/run/libvirt/libvirt-sock

``````
afrer running this command, all was fine. Good luck!