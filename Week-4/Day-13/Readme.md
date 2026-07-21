# Day 13 – Access Control & Linux Privilege Escalation (Week 4)

**Date:** 21 July 2026  
**Duration:** 6:30 PM – 8:30 PM

---

# Objective

To strengthen my understanding of access control mechanisms, Linux privilege escalation, and authorization vulnerabilities through theoretical concepts and hands-on labs using TryHackMe and PortSwigger Web Security Academy.

---

# Topics Covered

- IAAA Security Model
- Access Control Vulnerabilities
- Broken Access Control (Revision)
- Linux Privilege Escalation
- Referer-Based Access Control
- GTFOBins
- Wayback Machine
- TryHackMe – Linux Privilege Escalation Room
- PortSwigger – Referer-Based Access Control Lab

---

# IAAA Security Model

The **IAAA** model defines the core process of securely managing user identities and access.

| Component | Description | Example |
|-----------|-------------|---------|
| **Identification** | User claims an identity. | Entering a username. |
| **Authentication** | Verifying the user's identity. | Password, OTP, or biometric authentication. |
| **Authorization** | Determining what resources the user can access. | Admins can manage users, while normal users have limited permissions. |
| **Accounting (Auditing)** | Recording user activities for monitoring and investigation. | Login history and audit logs. |

---

# Access Control Vulnerabilities

Access control vulnerabilities occur when an application fails to properly restrict users from accessing resources or performing actions beyond their assigned permissions.

### Common Causes

- Missing authorization checks
- Improper role validation
- Insecure Direct Object References (IDOR)
- Client-side access control
- Misconfigured permissions

---

# Broken Access Control

Broken Access Control occurs when users are able to perform actions outside their intended permissions.

**Example**

```
/profile?id=101
```

Changing it to

```
/profile?id=102
```

may allow access to another user's profile if proper authorization checks are missing.

---

# Linux Privilege Escalation

Privilege escalation is the process of obtaining higher privileges on a Linux system after gaining initial access.

### Common Techniques

- SUID binaries
- Weak file permissions
- Misconfigured services
- Scheduled Cron Jobs
- Kernel vulnerabilities

---

# Referer-Based Access Control

Some web applications rely on the HTTP **Referer** header to determine whether a request is authorized.

Since HTTP headers can be modified, relying solely on the Referer header is insecure.

**Example**

A restricted endpoint checks whether the request originated from the admin dashboard. An attacker can modify the Referer header using Burp Suite, potentially bypassing this protection if proper server-side authorization checks are absent.

---

# GTFOBins

**GTFOBins** is a curated repository of Unix binaries that can be abused in misconfigured environments for privilege escalation, file transfer, or shell execution.

It is widely used by penetration testers to identify potential privilege escalation vectors during Linux security assessments.

---

# Wayback Machine

The **Wayback Machine** is an online archive maintained by the Internet Archive that stores historical snapshots of websites.

During reconnaissance and OSINT activities, it can help identify:

- Deleted web pages
- Previous website structures
- Hidden directories
- Archived sensitive files
- Historical application changes

It is a valuable resource for understanding how a target website has evolved over time.

---

# Practical Activities

## TryHackMe – Linux Privilege Escalation

Completed the **Linux Privilege Escalation** room on TryHackMe to understand how attackers identify and exploit common Linux misconfigurations after gaining initial access.

During the lab, I performed system enumeration to identify users, groups, running services, file permissions, scheduled tasks, and SUID binaries. I explored common privilege escalation vectors and understood how insecure configurations can lead to elevated privileges.

The lab also introduced **GTFOBins**, demonstrating how legitimate Linux binaries may be abused in misconfigured environments. Overall, the exercise emphasized the importance of system hardening, proper permission management, and the Principle of Least Privilege.

### Key Concepts Learned

- Linux Enumeration
- User & Group Permissions
- SUID Binaries
- Privilege Escalation Techniques
- Principle of Least Privilege
- GTFOBins

---

## PortSwigger – Referer-Based Access Control

Completed the **Referer-Based Access Control** lab on PortSwigger Web Security Academy.

The lab demonstrated how relying solely on the HTTP **Referer** header for authorization is insecure. Using **Burp Suite**, I analyzed and modified HTTP requests to understand how improper server-side authorization checks can result in unauthorized access.

### Key Concepts Learned

- Authorization Validation
- Referer Header Manipulation
- Broken Access Control
- HTTP Request Analysis
- Burp Suite Interception

---

# Key Learnings

- Understood the IAAA security model.
- Explored common access control vulnerabilities.
- Learned Linux privilege escalation fundamentals.
- Understood the risks of Broken Access Control.
- Learned why Referer headers should never be trusted for authorization.
- Explored GTFOBins as a Linux privilege escalation reference.
- Learned how the Wayback Machine supports OSINT and reconnaissance.
- Gained hands-on experience through TryHackMe and PortSwigger labs.

---

# Reflection

Today's session provided a deeper understanding of access control and privilege management in both Linux systems and web applications. The practical labs demonstrated how seemingly small security misconfigurations can lead to unauthorized access or privilege escalation. Learning resources such as GTFOBins and the Wayback Machine also highlighted the importance of reconnaissance and secure system configuration during penetration testing.

---

# Assignment

- Complete additional Linux Privilege Escalation rooms on TryHackMe.
- Explore more GTFOBins techniques.
- Practice additional PortSwigger Access Control labs.
- Revise the IAAA Security Model and Access Control concepts.

---

# Screenshots

Screenshots from today's theory session and practical labs are available in the **`screenshots/`** directory.