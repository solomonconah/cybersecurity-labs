# Lab 05: Web Application Security Assessment with OWASP ZAP

## Overview

This lab demonstrates the use of **OWASP Zed Attack Proxy (ZAP)** to perform a web application security assessment in a controlled and authorized environment. The assessment focuses on identifying security weaknesses through passive analysis and manual inspection of HTTP traffic.

The objective is to understand how web applications communicate, identify common security issues, and recommend defensive improvements based on industry best practices.

---

# Objectives

This lab aims to:

- Configure OWASP ZAP as an intercepting proxy
- Capture HTTP requests and responses
- Explore a web application
- Perform passive security analysis
- Review HTTP security headers
- Inspect cookies and session management
- Analyze OWASP ZAP alerts
- Document findings professionally

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable 2 |
| Target IP | 172.16.59.129 |
| Web Server | Apache HTTP Server |
| Tool | OWASP ZAP |
| Browser | Firefox |

---

# Tools Used

- OWASP ZAP
- Firefox
- Curl
- Kali Linux

---

# Assessment Methodology

The assessment followed a structured approach:

1. Configure browser proxy settings.
2. Launch OWASP ZAP.
3. Browse the target application.
4. Capture HTTP traffic.
5. Review requests and responses.
6. Analyze passive alerts.
7. Review HTTP headers.
8. Evaluate cookie security.
9. Document findings.
10. Recommend mitigations.

---

# Repository Structure

```
06-owasp-zap/
│
├── README.md
├── images/
│   ├── dashboard.png
│   ├── alerts.png
│   ├── headers.png
│   ├── cookies.png
│   ├── sites-tree.png
│   └── request-response.png
│
└── reports/
    └── zap-report.md
```

---

# Assessment Activities

## 1. Proxy Configuration

Configured Firefox to route all HTTP traffic through the OWASP ZAP proxy.

**Objective**

Allow OWASP ZAP to intercept and inspect all web traffic.

---

## 2. Site Discovery

Browsed the application to allow ZAP to build the site map automatically.

**Evidence**

*(Insert screenshot of the Sites Tree.)*

---

## 3. Passive Analysis

Reviewed alerts generated during passive scanning.

Examples include:

- Missing security headers
- Cookie observations
- Information disclosure
- Server banner disclosure
- Cache control observations

Passive scanning does not modify requests and is suitable for initial reconnaissance.

---

## 4. HTTP Request Analysis

Reviewed:

- Request methods
- URLs
- Parameters
- Headers
- Status codes

**Evidence**

*(Insert screenshot.)*

---

## 5. HTTP Response Analysis

Reviewed:

- Response headers
- Cookies
- Response body
- Security headers

---

## 6. Security Header Review

Evaluated the presence of:

- Content-Security-Policy
- X-Frame-Options
- X-Content-Type-Options
- Referrer-Policy
- Strict-Transport-Security

---

## Findings

Document each finding using the following format.

### Finding ID

WS-001

### Title

Missing HTTP Security Header

### Severity

Low

### Description

Explain what OWASP ZAP observed.

### Evidence

Insert screenshot.

### Risk

Explain why the finding matters.

### Recommendation

Describe how the issue could be addressed.

---

## Mitigations

Recommended improvements include:

- Enable HTTPS where appropriate.
- Implement recommended HTTP security headers.
- Secure cookies using appropriate attributes.
- Minimize unnecessary information disclosure.
- Remove deprecated functionality.
- Keep software updated.
- Review authentication and session management controls.

---

## Lessons Learned

This assessment demonstrated that:

- Passive analysis provides valuable security insight with minimal impact.
- HTTP headers reveal important information about server configuration.
- Browser security headers improve client-side protections.
- Cookie configuration is an important aspect of session security.
- Automated tools require analyst review and validation.
- Professional documentation is an essential cybersecurity skill.

---

## Skills Demonstrated

- Web Application Security Testing
- HTTP Analysis
- Proxy Configuration
- Passive Security Assessment
- Header Analysis
- Cookie Analysis
- Security Reporting
- Defensive Security Recommendations

---

## References

- OWASP Web Security Testing Guide (WSTG)
- OWASP ZAP Documentation
- OWASP Top 10 (2021)
- RFC 9110: HTTP Semantics

---

## Disclaimer

This assessment was performed exclusively within an authorized laboratory environment using intentionally vulnerable systems for educational and defensive security purposes. The techniques documented in this repository are intended to support secure system assessment and should only be applied to systems where explicit authorization has been obtained.
