# SQL Injection Concepts

SQL injection exploits unsanitized user input to inject malicious SQL queries, enabling attackers to gain unauthorized access or extract sensitive data from backend databases.

SQL injection can be used to implement the following attacks:

+ Authentication Bypass
+ Authorization Bypass
+ Information Disclosure
+ Compromised Data Integrity
+ Compromised Availability of Data
+ Remote Code Execution

## SQL Query vs SQL Injection Query

Below Diagrams shows the difference

![1](https://github.com/Kr1shna02/hack-flow/assets/117007783/56a7eccb-ac13-45f9-8405-cd96f87eac36)

![2](https://github.com/Kr1shna02/hack-flow/assets/117007783/093b3c70-1d4c-4140-84c9-2da97347132f)

# Types of SQL Injection

+  In-band SQL Injection:
Same-channel injection and retrieval.Error-based and UNION SQL injection are prevalent in-band techniques.

+  Blind/Inferential SQL Injection:
  
Error-free boolean-based data retrieval.
+  Out-of-Band SQL Injection:

Data exfiltration via side/alternate channels.

![3](https://github.com/Kr1shna02/hack-flow/assets/117007783/34a992a6-5dc6-423b-be1d-601ed2cfca44)

Piggybacked Query attack: In piggybacked SQL injection, attackers append a malicious query to the original one, exploiting batched SQL queries by using semicolons as delimiters to inject additional commands.
```sql
 SELECT * FROM EMP WHERE EMP.EID = 1001 AND EMP.ENAME = ’Bob’; DROP TABLE DEPT;
```
## Link for the detailed explanation of all attacks = [Portswigger labs](https://portswigger.net/web-security/sql-injection)
## Fuzz Testing 

It is an adaptive SQL injection testing technique used to discover coding errors by inputting a massive amount of random data and observing the changes in the output. 

Tools -
  + [BeSTORM](https://www.beyondsecurity.com)
  + [Burp Suite](https://portswigger.net) 
  + [HCL AppScan](https://www.hcltechsw.com)
  + [Peach Fuzzer](https://sourceforge.net)

Detecting Input Sanitization - use '' ,"",[] in the input field to chech weather application filers malicious input.

## Source Code Review to Detect SQL Injection Vulnerabilities

Source code review helps in finding and removing security vulnerabilities such as SQL injection vulnerabilities, format string exploits, race conditions, memory leaks, buffer overflows.

Tools-
+ [Veracode](https://www.veracode.com)
+ [Sonar](https://sonarsource.com)
+ [PVS-Studio](https://www.viva64.com)
+ [Coverity Scan](https://scan.coverity.com)







