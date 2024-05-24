# Web server Concepts
## Web server Operations

![a](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/b9646f92-031c-4ee0-b1ce-ba0a8e5553dd)

### Components of web server
+ Document Root -The document root is one of the root file directories of the web server that stores critical HTML files related to the web pages of a domain name, which will be sent in response to requests.

+ Server Root -It is the top-level root directory under the directory tree in which the server’s configuration and error, executable, and log files are stored. It consists of the code that implements the server.
  
+ Virtual Hosting -It is a technique of hosting multiple domains or websites on the same server
+ Web Proxy -A proxy server is located between the web client and web server. They are used to prevent IP blocking and maintain anonymity.

### open-source web server architecture 
![b](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/c6fa0019-f9ae-4055-a67f-4e51a0293f2d)
+ Linux - web server os
+ Apache - web server
+ Mysql -Database
+ php -backend connector
#### IIS Web Server Architecture
![c](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/63d62e16-b461-4c2d-bae6-f11db2c24296)![i](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/6ce32846-3cec-468f-bd80-71f25251d5f9)
The Internet Information Service (IIS) is a web server application developed by Microsoft for Windows. It supports HTTP, HTTPS,FTP, FTPS,SMTP and NNTP.t has several components, including a protocol listener such as HTTP.sys and services such as the World Wide Web Publishing Service (WWW Service) and Windows Process Activation Service (WAS).

## Web server Security Issues

![d](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/bf2bd067-56c7-48e5-840c-dd7839ba32b0)
### Impact of Web Server Attacks
+ Compromise of user accounts
+ Website defacement
+ Secondary attacks from the website
+ Root access to other applications or server
+ Data Tampering 
+ Data Theft
 
# Web Server attacks 
## DNS Server Hijacking

![e](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/c9b3459c-74fb-4f47-a8b0-85f4d8c85b72)
## DNS Amplification Attack

In this attack the attacker spoof dns request with victim IP and sends it to multiple DNS servers , which results in large amount dns replays to the victim causing DDOS.

![f](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/a651194e-1efc-42dc-83c2-f8ffb9932523)


## Directory Traversal Attacks

The design of web servers limits public access to some extent. Directory traversal is the exploitation of HTTP through which attackers can access restricted directories and execute commands outside the web server’s root directory by manipulating a Uniform Resource Locator (URL). In directory traversal attacks, attackers use the dot-dot-slash (../) sequence to access restricted directories outside the web server’s root directory. 
![g](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/b293ca53-537e-4056-9ba3-339b7b028368)


## Website Defacement
+ Website defacement refers to unauthorized changes made to the content of a single web page or an entire website, resulting in changes to the visual appearance of the web page or website.

## Web Server Misconfiguration

 + Verbose debug/error messages
 + Anonymous or default users/passwords
 + Sample configuration and script files
 + Remote administration functions
 + Unnecessary services enabled
 + Misconfigured/default SSL certificates

## HTTP Response-Splitting Attack

+ In this attack, the attacker controls the input parameter and cleverly constructs a request header that elicits two responses from the server. The attacker alters a single request to appear as two requests by adding header response data into the input field.
+ Cross-site scripting (XSS), cross-site request forgery (CSRF), and Structured Query Language (SQL) injection are examples of this type of attack.
![h](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/c270a818-94f3-47bd-8063-dcf892ba4f0c)


# Web Server Attack Methodology
+ Information Gathering
+ Web Server Footprinting
+ Website Mirroring
+ Vulnerability Scanning
+ Session Hijacking
+ Web Server Passwords Hacking

## Information Gathering
Information gathering tools
+ [who.is](https://who.is)
+ [Domain Dossier](https://centralops.net)
+ [Find Subdomains](https://pentest-tools.com)
  
## Information Gathering from Robots.txt File
A website owner creates a robots.txt file to list the files or directories a web crawler should index for providing search results. Poorly written robots.txt files can cause the complete indexing of website files and directories.
![i](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/6ce32846-3cec-468f-bd80-71f25251d5f9)


## Web Server Footprinting/Banner Grabbing
Tools
+ Netcat -netcat is a networking utility that reads and writes data across network connections by using the TCP/IP protocol.
![j](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/9e244811-3c04-41a5-b768-af4114901e92)


+ httprecon -httprecon is a tool for advanced web server fingerprinting. This tool performs banner-grabbing attacks, status code enumeration, and header ordering analysis on the target web server and provides accurate web server fingerprinting information.
![k](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/450c05ed-d357-46fc-bdb7-869eaca1936b)

+ ID Serve -ID Serve is a simple Internet server identification utility.
![l](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/2212e0fa-257b-4a48-bd15-17d4fc3101f0)


## Enumerating Web Server Information Using Nmap
+ Discover virtual domains with hostmap:
  ```
  nmap --script hostmap <host>
  ```
+ Detect a vulnerable server that uses the TRACE method:
  ```
  nmap --script http-trace -p80 localhost
  ```
+ Harvest email accounts with http-google-email:
  ```
  nmap --script http-google-email <host>
  ```
+ Enumerate users with http-userdir-enum:
```
  nmap -p80 --script http-userdir -enum localhost
```
+ Detect HTTP TRACE:
```
  nmap -p80 --script http-trace <host>
```
+ Check if the web server is protected by a web application firewall (WAF) or IPS:
```
  nmap -p80 --script http-waf-detect --script-args=”http-waf-detect.uri=/testphp.vulnweb.com/artists.php,http-waf-detect.detectBodyChanges” www.modsecurity.org
```
+ Enumerate common web applications
```
  nmap --script http-enum -p80 <host>
```
+ Obtain robots.txt
```
  nmap -p80 --script http-robots.txt <host>
```

## Vulnerability Scanning 
Vulnerability scanning is performed to identify vulnerabilities and misconfigurations in a target web server or network.

Tools

[Acunetix Web Vulnerability Scanner](https://www.acunetix.com )

## Finding Exploitable Vulnerabilities
Baesd on information obtained in previous process, now we search for a expoilt with help of those informations in various expiot databases like,
[Exploit-DB](https://www.exploit-db.com)

## Session Hijacking
An attacker can hijack or steal valid session content using various techniques such as session token prediction, session replay, session fixation, sidejacking, and XSS. By using these techniques, the attacker attempts to capture valid session cookies and IDs in established sessions.

Tools
[Burpsuite](https://github.com/kr1shna02/Cybersec-tools/blob/main/Burp%20Suite.md)

## Using Application Server as a Proxy
Web servers are occasionally configured to perform functions such as forwarding or reverse HTTP proxy.
![m](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/92f1b617-8d9f-4eb8-9425-0631bc6d36d5)

## Web Server Attack Tools: Metasploit 
The Metasploit Framework is a penetration-testing toolkit, exploit development platform, and research tool that includes hundreds of working remote exploits for various platforms.
[Metasploit reference](https://github.com/kr1shna02/Cybersec-tools/blob/main/Metasploit.md)

## Other tools:

Immunity’s CANVAS provides penetration testers and security professionals with hundreds of exploits, an automated exploitation system, and a comprehensive, reliable exploit development framework. 

[Immunity’s CANVAS]( https://www.immunityinc.com)

# Web Server Attack Countermeasures
## Place Web Servers in Separate Secure Server Security Segment on Network 

![n](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/3bb9af6c-e868-485f-b38c-0a59cf112ca7)

## Countermeasures
+ Countermeasures: Patches and Updates
+ Countermeasures: Protocols and User Accounts
+ Countermeasures: Files and Directories

## Detecting Web Server Hacking Attempts
A website change detection system (WDS) is a script that runs on the server to detect changes made to any executable file or the presence of any new file on the web server.

+ Ports: Monitor all ports on the web server regularly to prevent unnecessary traffic toward the target web server.
+ Server Certificates: Server certificates guarantee security and are signed by a trusted authority. An attacker may compromise certified servers using forged certificates to intercept secure communications by performing MITM attacks.
+ Code Access Security: Secure coding

## How to Defend against DNS Hijacking
+  Choose a registrar accredited by the Internet Corporation for Assigned Names and Numbers (ICANN) and encourage them to set REGISTRAR-LOCK on the domain name.
+  Domain Name System Security Extensions (DNSSEC): It adds an extra layer to DNS that prevents it from being hacked.

## Web Application Security Scanners
+ [Syhunt Hybrid](https://www.syhunt.com)
+ [N-Stalker X](https://www.nstalker.com)

## Web Server Security Scanners
+ [Qualys Community Edition](https://www.qualys.com)
+ [QualysGuard Malware Detection ]( https://www.qualys.com )
+ [Fortify WebInspect](https://www.microfocus.com )

# Patch Management
patch management is an area of systems management that involves acquiring, testing, and installing multiple patches (code changes) in an administered computer system.

[GFI LanGuard ](https://www.gfi.com)
