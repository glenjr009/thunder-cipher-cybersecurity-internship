# Day 12 – OWASP Top 10 & Web Application Security (Week 4)

**Date:** 20 July 2026

---

# Objective

To understand the fundamentals of Web Application Penetration Testing (WAPT), study the OWASP Top 10 (2025), learn access control concepts, and solve a practical authorization vulnerability lab.

---

# Topics Covered

- Introduction to Web Application Penetration Testing (WAPT)
- OWASP Foundation
- OWASP Top 10 (2025)
- OWASP Mobile Top 10
- A01: Broken Access Control
- CIA Triad (Revision)
- IDOR (Insecure Direct Object References)
- Privilege Escalation
- Role-Based Access Control (RBAC)
- Mandatory Access Control (MAC)
- Discretionary Access Control (DAC)
- Website Security Checker
- Thunder Cipher Lab – **DeleteMe**

---

# What is WAPT?

**Web Application Penetration Testing (WAPT)** is the process of testing web applications to identify security vulnerabilities before attackers can exploit them.

**Example:**
Testing whether a normal user can access an admin panel without authorization.

---

# OWASP Top 10 (2025) – Short Notes

| Vulnerability | Description | Example |
|---------------|-------------|---------|
| **A01 – Broken Access Control** | Users can access resources they shouldn't. | A normal user deletes another user's account by changing the URL. |
| **A02 – Cryptographic Failures** | Weak or missing encryption exposes sensitive data. | Passwords stored in plain text. |
| **A03 – Injection** | Untrusted input is executed as commands or queries. | SQL Injection bypasses login authentication. |
| **A04 – Insecure Design** | Security wasn't considered during application design. | No rate limiting on login page allowing brute-force attacks. |
| **A05 – Security Misconfiguration** | Unsafe default settings or incorrect configurations. | Directory listing enabled on the web server. |
| **A06 – Vulnerable Components** | Using outdated libraries or software. | Running an application with an old Log4j version. |
| **A07 – Identification & Authentication Failures** | Weak login or session management. | Weak passwords or session IDs that never expire. |
| **A08 – Software & Data Integrity Failures** | Applications trust unverified updates or data. | Installing unsigned software updates. |
| **A09 – Security Logging & Monitoring Failures** | Attacks aren't detected due to poor logging. | Multiple failed login attempts are never recorded. |
| **A10 – Server-Side Request Forgery (SSRF)** | Server makes requests on behalf of an attacker. | Fetching internal cloud metadata through a vulnerable URL parameter. |

---

# Access Control Concepts

## IDOR (Insecure Direct Object Reference)

Occurs when an application allows users to access another user's data simply by changing an identifier.

**Example**

```
/profile?id=101
```

Changing it to

```
/profile?id=102
```

reveals another user's profile.

---

## Privilege Escalation

When a user gains permissions beyond their authorized level.

**Example**

A normal employee becomes an administrator by exploiting a vulnerability.

---

## RBAC (Role-Based Access Control)

Permissions are assigned based on roles.

**Example**

- Admin → Full Access
- Manager → Edit
- Employee → View Only

---

## DAC (Discretionary Access Control)

The owner decides who can access a resource.

**Example**

A Google Drive owner shares a file with selected users.

---

## MAC (Mandatory Access Control)

Permissions are enforced by the operating system or organization.

**Example**

Military documents classified as Top Secret can only be accessed by users with appropriate clearance.

---

# CIA Triad (Revision)

- **Confidentiality** → Prevent unauthorized access to data.
- **Integrity** → Ensure data remains accurate and unaltered.
- **Availability** → Ensure systems remain accessible when needed.

---

# Practical Activity

- Studied OWASP Top 10 vulnerabilities.
- Explored access control weaknesses.
- Learned about website security checking tools.
- Solved the **Thunder Cipher "DeleteMe" Lab**, which demonstrated **Broken Access Control (A01)** and **IDOR** concepts in a controlled environment.

---

# Key Learnings

- Understood the purpose of OWASP in improving web security.
- Learned all OWASP Top 10 (2025) vulnerabilities with practical examples.
- Understood why Broken Access Control is one of the most critical web vulnerabilities.
- Learned the difference between RBAC, DAC, and MAC.
- Gained practical exposure to authorization vulnerabilities through the DeleteMe lab.

---

# Reflection

Today's session introduced the core concepts of web application security and the OWASP Top 10. The practical examples made it easier to understand how common vulnerabilities arise in real-world applications. Solving the DeleteMe lab reinforced the importance of implementing proper authorization checks to prevent unauthorized access and privilege escalation.

---

# Assignment

- Revise the OWASP Top 10 (2025).
- Practice identifying Broken Access Control and IDOR vulnerabilities using safe learning labs.
- Explore additional OWASP Web Security Academy and Thunder Cipher exercises.

---

# Screenshots

Screenshots from today's session and the DeleteMe lab are available in the `screenshots/` directory.