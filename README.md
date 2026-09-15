# Future Interns Cyber Security Task 1

## Vulnerability Assessment Report

This repository contains my Vulnerability Assessment Report completed as part of the Future Interns Cyber Security Task 1.

### 👤 Prepared By
**G.Manicharan**

### 🎯 Objective

The objective of this task was to perform a read-only security assessment of a publicly accessible website, identify common security weaknesses, classify the associated risks, and provide practical remediation recommendations.

### 🌐 Website Tested

**Target:** https://testfire.net/

**Application:** Altoro Mutual Demo Banking Application

The assessment was performed only against the publicly accessible pages of the selected test/demo website.

### 🔒 Scope

The assessment was conducted using a passive and read-only approach.

Activities included:

- Public website inspection
- Basic port and service exposure analysis
- HTTP/HTTPS behavior checking
- Security header inspection
- Cookie security attribute inspection
- Documentation of observed security weaknesses

### 🛠️ Tools Used

- **Nmap 7.991** – Basic port and service exposure analysis
- **Google Chrome DevTools** – HTTP response headers, cookies, and HTTPS behavior
- **OWASP ZAP** – Intended for passive scanning, but the scan was not completed because Windows Security blocked the ZAP package. No security controls were disabled or bypassed.

### 🔍 Key Findings

| ID | Finding | Risk |
|---|---|---|
| F-01 | Session Cookie Missing Explicit SameSite Attribute | Medium |
| F-02 | HSTS Header Not Observed | Low |
| F-03 | Clickjacking Protection Not Observed | Low |
| F-04 | X-Content-Type-Options Not Observed | Low |
| F-05 | Server Technology Banner Disclosure | Informational |

### 📌 Important Observation

The presence of an open port or a missing security header does not automatically mean that the website is compromised. The findings in this assessment are documented as security weaknesses or hardening opportunities based on the observed configuration.

### 🛡️ Recommended Remediation

Recommended security improvements include:

- Configure an appropriate `SameSite` attribute for session cookies.
- Enable HTTP Strict Transport Security (HSTS).
- Implement clickjacking protection using `X-Frame-Options` or CSP `frame-ancestors`.
- Add `X-Content-Type-Options: nosniff`.
- Review and minimize unnecessary server technology information exposed through HTTP response headers.
- Review externally exposed services and restrict unnecessary services where appropriate.

### 📂 Repository Contents

- **Vulnerability Assessment Report** – Complete assessment report in PDF format.
- **Evidence Screenshots** – Supporting screenshots from the assessment.
- **README.md** – Project overview, scope, methodology, findings, and remediation summary.

### ⚖️ Ethical Statement

This assessment was performed for educational and internship purposes using a read-only/passive approach.

No login bypass, brute-force attempts, exploitation, denial-of-service activity, or other harmful testing was performed.

The assessment was conducted with the principle of:

> Think like a security auditor, not an attacker.

---

**Future Interns Cyber Security Task 1 – Vulnerability Assessment**
