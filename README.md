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
