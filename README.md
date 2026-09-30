# Burp Suite – Web Application Penetration Testing

## Project Overview

This project demonstrates an authorized web application security assessment using Burp Suite and the intentionally vulnerable OWASP Juice Shop application.

The assessment was performed in a controlled local laboratory environment using Kali Linux, Docker, Firefox and Burp Suite.

The project focuses on understanding HTTP traffic, authentication, API authorization, session handling, input validation and evidence-based security testing.

---

## Objectives

- Understand the role of Burp Suite in web application penetration testing.
- Configure Firefox to route web traffic through Burp Suite.
- Capture and analyze HTTP requests and responses.
- Analyze authentication and token-based sessions.
- Use Burp Repeater for manual request testing.
- Use Burp Intruder for controlled repeated testing.
- Analyze API authorization and object identifiers.
- Perform controlled XSS-oriented testing.
- Review CSRF and session-security considerations.
- Document security observations and remediation recommendations.

---

## Lab Environment

| Component | Technology |
|---|---|
| Operating System | Kali Linux |
| Web Application | OWASP Juice Shop |
| Container Platform | Docker |
| Browser | Firefox |
| Security Tool | Burp Suite |
| Target | http://localhost:3000 |
| Burp Proxy | 127.0.0.1:8080 |

---

## Architecture

```text
Firefox
   |
   | HTTP/HTTPS Traffic
   v
Burp Suite Proxy
127.0.0.1:8080
   |
   | Inspected / Controlled Requests
   v
OWASP Juice Shop
localhost:3000
   |
   v
HTTP Response
   |
   v
Burp Suite
   |
   v
Firefox
```
Testing Methodology

The assessment followed an evidence-driven workflow:

* Define scope and authorization.
* Deploy OWASP Juice Shop using Docker.
* Verify the application locally.
* Configure Firefox to use Burp Suite.
* Capture normal application traffic.
* Analyze HTTP requests and responses.
* Test authentication behavior.
* Perform controlled testing using Repeater.
* Perform controlled repeated testing using Intruder.
* Analyze API authorization behavior.
* Review input handling and XSS-oriented testing.
* Consider CSRF and session-security controls.
* Document observations and evidence.
* Prepare remediation recommendations.
---
Burp Suite Components Used

Proxy : 
Used to intercept and inspect browser traffic.

HTTP History : 
Used to review captured application requests and responses.

Repeater : 
Used for manually modifying and replaying selected requests.

Intruder : 
Used for controlled repeated testing with a small laboratory dataset.

---

Security Testing Areas: 

* Authentication
* Login request analysis
* Authentication failure analysis
* Controlled credential testing
* Authentication input manipulation
* Token/session handling

API Security:

* Authenticated API requests
* Basket API testing
* Object identifier behavior
* Authorization testing
* HTTP method behavior
* User endpoint analysis

Input Security:

* Controlled XSS-oriented testing
* Input validation considerations
* Output encoding considerations

Session Security:

* Token transmission
* Token storage considerations
* Session lifecycle
* Logout and expiration considerations
* CSRF considerations

---
Evidence:
The project contains evidence showing:

* Docker deployment
* Juice Shop startup
* Application baseline
* Burp Proxy configuration
* Firefox proxy configuration
* HTTP interception
* Authentication requests
* Repeater testing
* Intruder configuration
* Intruder results
* API authorization testing
* Basket API testing
* User endpoint analysis
* XSS-oriented testing
* CSRF/session-security analysis

Detailed evidence is available in:
```
docs/Evidence_and_Screenshots.pdf
```
---
Project Documentation:
```
| Document                   | Description                  |
| -------------------------- | ---------------------------- |
| Security Assessment Report | Complete project report      |
| Evidence and Screenshots   | Testing evidence             |
| Project Presentation       | PPT presentation             |
| Final Checklist            | Final verification checklist |
```
---
Findings and Risk Assessment:

The assessment focuses on security testing areas including:
* Authentication input handling
* Authentication response behavior
* Token/session handling
* API authorization
* Object-level authorization
* Input validation
* XSS-oriented testing
* CSRF/session-security considerations
Security conclusions are based on the available evidence and are not treated as confirmed vulnerabilities unless the evidence supports that conclusion.

---
Remediation Areas

Recommended defensive controls include: 
* Parameterized database queries
* Strong authentication controls
* Rate limiting
* Proper authorization checks
* Input validation
* Context-aware output encoding
* CSRF protections where applicable
* Secure token handling
* Session expiration and logout controls
* Data minimization

---
Ethical Scope
This project was performed against an intentionally vulnerable OWASP Juice Shop instance running locally.

Target:
```
http://localhost:3000
```
The techniques demonstrated in this project must only be used against systems for which explicit authorization has been provided.
Do not use these techniques against public websites, systems or accounts without permission.

---
Tools and Technologies:
* Kali Linux
* Burp Suite
* OWASP Juice Shop
* Docker
* Firefox
* HTTP/HTTPS
* REST APIs
* Web Application Security Testing

---
Disclaimer:

This repository is intended for educational and authorized security-testing purposes only.
No production systems were intentionally targeted.
Sensitive credentials, authentication tokens and other secrets should not be committed to this repository.

---
Author

Chavali Keshava Gopalu

Cybersecurity / Network Security

GitHub: Kesav3107

---
