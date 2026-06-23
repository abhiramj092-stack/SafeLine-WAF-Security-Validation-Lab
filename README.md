# SafeLine WAF Security Validation Lab

## Overview

This project demonstrates the deployment and validation of SafeLine Web Application Firewall (WAF) using DVWA (Damn Vulnerable Web Application) in a controlled cybersecurity lab environment.

The objective was to evaluate SafeLine WAF's ability to detect and block common web application attacks.

---

## Technologies Used

* Ubuntu Linux
* Docker
* SafeLine WAF
* DVWA
* Firefox Browser

---

## Lab Architecture

Attacker Browser

↓

SafeLine WAF

↓

DVWA

↓

Database

---

## Attack Scenarios

### SQL Injection

Payload Tested:

' OR '1'='1

Result:

* Attack Detected
* Attack Logged
* Request Blocked

### Cross Site Scripting (XSS)

Payload Tested:

<script>alert(1)</script>

Result:

* Attack Detected
* Attack Logged
* Access Denied

### Command Injection

Payload Tested:

127.0.0.1 && whoami

Result:

* Attack Detected
* Attack Logged
* Execution Prevented

---

## Screenshots

### SQL Injection Test

![SQLi](Screenshots/01-SQLi-Test.png)

### SQL Injection Detection

![SQLi Detection](Screenshots/02-SQLi-Detection.png)

### XSS Test

![XSS](Screenshots/03-XSS-Test.png)

### XSS Blocked

![XSS Blocked](Screenshots/04-XSS-Blocked.png)

### Command Injection Test

![CMDi](Screenshots/05-CMDi-Test.png)

### Command Injection Blocked

![CMDi Blocked](Screenshots/06-CMDi-Blocked.png)

### SafeLine WAF Attack Logs

![Logs](Screenshots/07-WAF-Logs.png)

---

## Findings

* SafeLine successfully detected SQL Injection attacks.
* SafeLine blocked reflected XSS payloads.
* SafeLine prevented Command Injection attempts.
* Detailed attack logs were generated for analysis.
* Real-time visibility into malicious requests was available through the SafeLine dashboard.

---

## Skills Demonstrated

* Web Application Security
* WAF Deployment
* Linux Administration
* Docker
* Security Monitoring
* Threat Detection
* Attack Analysis
* OWASP Top 10 Awareness

---

## Conclusion

This project successfully validated SafeLine WAF's capability to detect, log, and block multiple OWASP Top 10 attack vectors in a controlled lab environment.

