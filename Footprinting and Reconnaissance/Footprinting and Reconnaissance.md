# Footprinting Concepts
Footprinting is used to gather maximum information of the computer system or the servers or persons we are going to attack.

## Types :
+ Active Footprinting
+ Passive Footprinting

## Information Obtained in Footprinting:
+ Organization Information - employee details, contact nos, about organisation etc.
+ Network Information - Domain and sub-domains, Network blocks, Network topology, trusted routers, and firewalls, Whois records, DNS records and related information
+ System Information - OS, webservers, technology's and applications used.

## Footprinting Methodology
![footprinting](https://github.com/Kr1shna02/CEH-v12/assets/117007783/e1fda30d-11d3-468b-9dbb-295ff9acec1b)

# Footprinting through Search Engines
## Footprinting Using Advanced Google Hacking Techniques
operator:serach_term
Any Keyword can be specified before the operator.It is used to search for particular keyword in the particular searh query.
+ site -This operator restricts search results to the specified site or domain.
    - games site: www.certified.com
    
+ allinurl -This operator restricts results to only the pages containing all the query terms specified in the URL.
    - allinurl: google career   
+ inurl -This operator restricts the results to only the pages containing the specified word in the URL.
    - inurl: copy site:www.google.com

+ allintitle -All Query in Page title
    - allintitle: detect malware
+ intitle - This operator restricts results to only the pages containing the specified term in the title
    - intitle: help
+ inanchor - Search page contain specified word in the anchor link.
    - antivirus inachor: norton
+ allinanchor- Search page contain all the specified terms in anchor link.
    - allinanchor: best cloud service provider
+ cache: Display google cached version of the webpage.
    - cache:www.ef.org
+ link -This operator searches websites or pages that contain links to the specified website or page
    - link:www.google.com
+ related - Display all pages related to the url
    - related:www.microsoft.com
+ info - Finds information for a specified webpage
+ location -Finds Location of the specified Organization
    - location:www.google.com
+ filetype -Search results with specified file formats only
    - filetype: pdf site: www.google.com
## Google Hacking Database 
In the GHDB, you will find search terms for files containing usernames, vulnerable servers, and even files containing passwords

![google](https://github.com/Kr1shna02/CEH-v12/assets/117007783/07532c12-23fb-402e-879e-f1770e62f2c0)


## Other Techniques for Footprinting through Search Engines 
+ [advanced_search](https://www.google.com/advanced_search)
+ [image_search](https://www.google.com/advanced_image_search)
+ [reverse image search](https://www.google.com/imghp)
+ [Iot Search engine -SHODAN](https://www.shodan.io/)

# Footprinting through Web Services
## Finding a Company’s Top-Level Domains (TLDs) and Sub-domains
### Tools to Search Company’s Sub-domains
+ [Netcraft](https://www.netcraft.com)
  
+ [Sublist3r](https://github.com/aboul3la/Sublist3r)
+ [Pentest-Tools](https://pentest-tools.com)
  
![pentest](https://github.com/Kr1shna02/CEH-v12/assets/117007783/c19a28f8-b504-4095-9714-3be31b2d7eb9)



## Harvesting Email Lists
Tools:
+ theHarvester
## Determining the Operating System
Tools:
+ Netcraft
  
  ![netcraft](https://github.com/Kr1shna02/CEH-v12/assets/117007783/452b0eb3-beaf-4175-86ed-6383d43fe68a)
+ shodan
+ [censys](https://search.censys.io/)

# Footprinting through Social Networking Sites
Tools:
+  [BuzzSumo](https://buzzsumo.com)
+  [Followerwonk](https://followerwonk.com) 
+  Sherlock
# Website Footprinting 
Information gained:
+ Software used and its version
+ Operating system used
+ Sub-directories and parameters
+ Filename, path, database field name, or query
+ Scripting platform
+ Technologies Used

Tools:
+ [Burp Suite](https://github.com/Kr1shna02/Tools/blob/main/Burp%20Suite.md)
+ [Web Data Extractor](http://www.webextractor.com)
+ https://archive.org
+ [Extracting links: Octoparse](https://www.octoparse.com )
+ [Centalops](https://centralops.net/)
+ [Mirroring Website]( https://www.httrack.com)
+  ExifTool 

Methods:
+ Examining the HTML source code
+ Examining Cookies
+ Mirroring Entire Website

# Email Footprinting
## Tracking Email Communications
+ Recipient's System IP address
+  Geolocation
+  Email Received and Read
+  Read Duration
+  Links
## Collecting Information from Email Header 
Tools:
+ Infoga
+ [eMailTrackerPro](http://www.emailtrackerpro.com)
# Whois Footprinting
## Whois Lookup
Tools:
+ http://whois.domaintools.com
+ https://www.tamos.com
+ [Finding IP gelocation information  IP2Location ](https://www.ip2location.com)

# DNS Footprinting

![dns](https://github.com/Kr1shna02/CEH-v12/assets/117007783/c026a113-b6f0-4efa-bb73-81314bff6ef4)

Tools:
+ [SecurityTrails](https://securitytrails.com )
## Reverse DNS Lookup 
Tools:
+ dnsrecon
+ [reverse lookup](https://mxtoolbox.com)

# Network Footprinting
## Locate the Network Range
Tool:
[ARIN](https://www.arin.net/about/welcome/region)

## Traceroute
Methods:
traceroute utility helps find the IP addresses of intermediate devices such as routers and firewalls present between a source and its destination.
+ ICMP Traceroute
    - tracert ip
+ TCP Traceroute
    - tcptraceroute www.google.com
+ UDP Traceroute
    - traceroute www.google.com
Tools :
+ [Path Analyzer Pro](https://www.pathanalyzer.com)
+ [VisualRoute ]( http://www.visualroute.com)
# Footprinting through Social Engineering
+ Eavesdropping
+ Shoulder Surfing
+ Dumpster Driving
# Common Footprinting Tools
+ Maltego

![maltego](https://github.com/Kr1shna02/CEH-v12/assets/117007783/bcd87d20-6c18-4dd7-a5ac-23856d07aa29)

+ [Recon-ng](https://hackertarget.com/recon-ng-tutorial/)
+ [FOCA](https://www.elevenpaths.com)
+ OSRframework:
  
  OSRFramework includes applications related to username checking, DNS lookups, information leaks research, deep web search, and regular expression extraction
  - usufy.py – Checks for a user profile on up to 290 different platforms
  - mailfy.py – Check for the existence of a given email
  - searchfy.py – Performs a query on the platforms in OSRFramework
    
        - searchfy.py -q “<Target Username>"
    
  - domainfy.py – Checks for the existence of domains
  - phonefy.py – Checks for the existence of a given series of phones
  - entify.py – Uses regular expressions to extract entities
  
+ [OSINT Framework](https://osintframework.com/)
+ BillChiper(give complete footprinting)
+ Spyse

