```
# Web Application Penetration Testing Methodology

## 1. Scope and Authorization

The assessment was conducted against the authorized local OWASP Juice Shop laboratory.

Target:

http://localhost:3000

The testing environment consisted of Kali Linux, Docker, Firefox and Burp Suite.

Security testing was restricted to the intentionally vulnerable local application.

---

## 2. Reconnaissance

The initial stage focused on understanding the application and identifying:

- Application pages
- User workflows
- HTTP requests
- HTTP methods
- Parameters
- Authentication endpoints
- API endpoints
- Security-sensitive operations

Normal application behavior was established before performing security tests.

---

## 3. Traffic Interception

Firefox was configured to route traffic through the Burp Suite proxy.

```text
Firefox
    |
    v
Burp Suite Proxy
127.0.0.1:8080
    |
    v
OWASP Juice Shop
localhost:3000

```

---
Burp Suite was used to intercept, inspect and forward HTTP requests.

HTTP History was used to review captured application traffic.

---
