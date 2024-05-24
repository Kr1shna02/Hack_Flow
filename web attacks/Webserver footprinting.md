# Information gathering using Ghost Eye
+ Ghost Eye is an information-gathering tool written in Python 3. To run, Ghost Eye only needs a domain or IP
+ Ghost Eye gathers information such as Whois lookup, DNS lookup, EtherApe, Nmap port scan, HTTP header grabber, Clickjacking test, Robots.txt scanner, Link grabber, IP location finder, and traceroute.

![eye](https://github.com/Kr1shna02/CEH-v12/assets/117007783/66a0c442-8490-4ff2-ad4f-462acda1d19b)

### Whois lookup
<br>![who](https://github.com/Kr1shna02/CEH-v12/assets/117007783/edcf3f2b-e7e8-4bd0-84e3-d2b6594573be)

### Clickjacking 

<br>![click](https://github.com/Kr1shna02/CEH-v12/assets/117007783/cd947cc4-95ed-41cf-8aba-039fcc17a589)

<br>![res](https://github.com/Kr1shna02/CEH-v12/assets/117007783/50502c56-f0b9-4b01-ac2c-f73c2ac21f51)

# Perform Web Server Reconnaissance using Skipfish

Skipfish is an active web application (deployed on a webserver) security reconnaissance tool. It prepares an interactive sitemap for the targeted site by carrying out a recursive crawl and dictionary-based probes. The resulting map is then annotated with the output from a number of active (but hopefully non-disruptive) security checks.


<br>![test](https://github.com/Kr1shna02/CEH-v12/assets/117007783/5bc696b5-2a76-4409-a34a-d46cfc5a5261)

<br>![skip](https://github.com/Kr1shna02/CEH-v12/assets/117007783/794b165f-a7c6-4841-a9bf-db80a72fb589)

<br>![res](https://github.com/Kr1shna02/CEH-v12/assets/117007783/f739e1b5-e45e-4ea7-9482-93bb6a046233)

# Footprint a Web Server using the httprecon Tool

httprecon is a tool for advanced web server fingerprinting. This tool performs banner-grabbing attacks, status code enumeration, and header ordering analysis on its target web server.

<br>![h](https://github.com/Kr1shna02/CEH-v12/assets/117007783/a53ec497-3480-42cf-8b8f-040d63e4995e)

# Enumerate Web Server Information using Nmap Scripting Engine (NSE)
+ Enumerate the directories used by web servers and web applications.
  ```
  nmap -sV --script=http-enum [target website]
  ```
  ![L1](https://github.com/kr1shna02/CEH-v12/assets/117007783/27138781-efbd-4d7d-9b78-a427836ebe12)

+ To discover the hostnames that resolve the targeted domain.
```
  nmap --script hostmap-bfk -script-args hostmap-bfk.prefix=hostmap- www.goodshopping.com
```
+ Check whether Web Application Firewall is configured on the target host or domain.
```
  nmap -p80 --script http-waf-detect www.goodshopping.com
```
![w](https://github.com/kr1shna02/CEH-v12/assets/117007783/77e78af5-2add-4141-bded-e64decfb574d)

# Uniscan Web Server Fingerprinting
Uniscan is a versatile server fingerprinting tool that not only performs simple commands like ping, traceroute, and nslookup, but also does static, dynamic, and stress checks on a web server. 
+ To search for dirtories
```
  uniscan -u http:url -q
```
+ use the dynamic testing option by giving the command -d
```
 uniscan -u http://10.10.1.22:8080/CEH -d
```
![t](https://github.com/kr1shna02/CEH-v12/assets/117007783/82f0bb8a-c4ab-435e-8de6-5d8f0c3a8dad)

Result are stored as a html page in uniscan directory with IP of the domain a file name.

# Perform a Web Server Attack
## Crack FTP Credentials using a Dictionary Attack
1. Perform nmap to check ftp is open in target server.
```
  nmap -p 21 target_IP
```
![1](https://github.com/kr1shna02/CEH-v12/assets/117007783/36ff2cbb-1012-4b01-8632-a44441ee772d)

2. Check FTP server is hosted
```
  ftp target_IP
```
![2](https://github.com/kr1shna02/CEH-v12/assets/117007783/42e03209-8b58-45e9-89b8-0d0229a9bf31)

3. Now perform password cracking attack using Hydra
```
  hydra -L username.txt -P password.txt fpt://target_IP
```
If the password of FTP is weak the we can get the username and password .And we can login as legitimate user.

