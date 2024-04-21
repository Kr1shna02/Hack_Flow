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

![s](https://github.com/kr1shna02/CEH-v12/assets/117007783/574e03e7-70dc-4172-8b99-6f97a40d8fb1)

![s1](https://github.com/kr1shna02/CEH-v12/assets/117007783/56c15573-0295-4a0d-8923-6d070df1e2e2)

# Types of SQL Injection

+  In-band SQL Injection:
In-band SQL injection attacks leverage the same channel for both injection and data retrieval. Error-based and UNION SQL injection are prevalent in-band techniques, exploiting error messages or combining query results for data extraction.
+  Blind/Inferential SQL Injection:
SQL injection relies on boolean-based queries, without direct error feedback, to infer database structure and data, posing challenges for attackers due to the absence of transmitted data, hence earning the name "blind".
+  Out-of-Band SQL Injection:
Out-of-Band SQL Injection involves exploiting vulnerabilities to initiate data exfiltration or command execution via alternative communication channels, circumventing traditional in-band methods.

![t](https://github.com/kr1shna02/CEH-v12/assets/117007783/dd6c8b2d-e4cb-429d-aa94-50c1d3d12c2f)

Piggybacked Query attack: In piggybacked SQL injection, attackers append a malicious query to the original one, exploiting batched SQL queries by using semicolons as delimiters to inject additional commands.
```sql
 SELECT * FROM EMP WHERE EMP.EID = 1001 AND EMP.ENAME = ’Bob’; DROP TABLE DEPT;
```
## Link for the detailed explanation of all attacks = [Portswigger labs](https://github.com/kr1shna02/portSwigger-labs/tree/main/SQL%20injection)
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







