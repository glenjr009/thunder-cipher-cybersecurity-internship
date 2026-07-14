# Day 07 - Active Reconnaissance, Enumeration & Web Discovery

**Date:** 13 July 2026

---

# Objective

The objective of today's session was to introduce active reconnaissance techniques using Nmap and Gobuster, understand service enumeration, explore the Nmap Scripting Engine (NSE), and apply these concepts by solving practical labs on the ThunderCipher platform.

---

# Session Overview

Today's session transitioned from passive reconnaissance to active reconnaissance techniques. We explored how security professionals identify live hosts, enumerate services, discover hidden web resources, and automate information gathering using Nmap scripts. The session concluded with hands-on labs on the ThunderCipher platform, where we applied these techniques in real-world scenarios.

---

# Topics Covered

- Active Reconnaissance
- Network Enumeration
- Nmap
- Nmap Scan Types
- Service & Version Detection
- Nmap Scripting Engine (NSE)
- Gobuster
- Directory Enumeration
- SSH Enumeration
- Hydra (Introduction)
- Password Brute Force Concepts
- ThunderCipher Practical Labs

---

# Theory Notes

## Active Reconnaissance

Unlike passive reconnaissance, active reconnaissance involves directly interacting with the target system. This includes scanning hosts, identifying open ports, discovering running services, and collecting information required for vulnerability assessment.

---

## Nmap

Nmap (Network Mapper) is one of the most widely used network scanning tools in cybersecurity.

It can be used to:

- Discover live hosts
- Identify open ports
- Detect running services
- Determine service versions
- Perform operating system detection
- Execute NSE scripts

---

## Common Nmap Scan Types

We discussed several scan techniques, including:

- TCP Connect Scan
- SYN Scan
- Version Detection
- Service Enumeration
- Script Scanning

These scans help security professionals understand the attack surface of a target.

---

## Nmap Scripting Engine (NSE)

The Nmap Scripting Engine (NSE) extends Nmap's capabilities by allowing scripts to automate information gathering and vulnerability detection.

Popular NSE categories covered:

- HTTP Enumeration
- SMB Discovery
- FTP Anonymous Login Check
- SSL Certificate Enumeration
- Vulnerability Detection

NSE enables faster reconnaissance and improves penetration testing workflows.

---

## Gobuster

Gobuster is a directory and file enumeration tool commonly used during web application assessments.

It performs brute-force discovery of hidden:

- Directories
- Files
- Endpoints

using predefined wordlists.

---

## SSH Enumeration

The session also introduced SSH enumeration and discussed how authentication services are commonly assessed during penetration tests.

---

## Hydra

Hydra was briefly introduced as a password auditing tool capable of testing login credentials against multiple network services.

The instructor emphasized that such tools should only be used within authorized environments.

---

# Practical Session

Today's practical session involved applying active reconnaissance techniques.

Activities included:

- Running Nmap scans against lab targets
- Performing service enumeration
- Executing Nmap NSE scripts
- Using Gobuster for directory enumeration
- Understanding SSH authentication
- Observing Hydra command syntax for password auditing
- Solving multiple ThunderCipher hands-on labs
- Enumerating hidden resources within web applications

---

# Tools Introduced

| Tool | Purpose |
|------|---------|
| Nmap | Network discovery and port scanning |
| NSE | Nmap scripting for automation and enumeration |
| Gobuster | Directory and file enumeration |
| Hydra | Password auditing and brute-force testing |
| SSH | Secure remote administration protocol |
| ThunderCipher Platform | Practical cybersecurity labs |

---

# Commands Practiced

```bash
# Basic Scan
nmap <target-ip>

# Service Version Detection
nmap -sV <target-ip>

# NSE Scan
nmap --script http-enum -p80 <target-ip>

# SMB Discovery
nmap --script smb-os-discovery -p445 <target-ip>

# Gobuster Directory Enumeration
gobuster dir -u http://<target-ip>/ -w /usr/share/wordlists/dirb/common.txt

# Hydra (Demonstration)
hydra -l <username> -P <wordlist> ssh://<target-ip>
```

---

# Hands-on Labs

During today's session, we completed several practical exercises on the ThunderCipher platform, including:

- Network scanning using Nmap
- Directory enumeration with Gobuster
- Running NSE scripts for service enumeration
- Exploring SSH authentication
- Solving web-based enumeration challenges
- Applying reconnaissance techniques to identify exposed services and hidden resources

---

# Key Learnings

- Understood the difference between passive and active reconnaissance.
- Learned how to enumerate systems using Nmap.
- Explored different Nmap scan techniques.
- Learned how NSE automates reconnaissance tasks.
- Used Gobuster to discover hidden directories.
- Understood the basics of password auditing using Hydra.
- Applied enumeration techniques during ThunderCipher practical labs.
- Strengthened practical skills in identifying web application attack surfaces.

---

# Challenges Faced

The ThunderCipher labs required careful observation and methodical enumeration. Rather than relying on a single tool, combining multiple techniques such as Nmap scanning, NSE scripts, and Gobuster enumeration proved essential for successfully solving the exercises.

---

# Assignment

The practical lab served as today's assignment.

Tasks included:

- Perform network scanning using Nmap.
- Enumerate services using NSE scripts.
- Discover hidden directories using Gobuster.
- Solve the assigned ThunderCipher web enumeration labs.

---

# Reflection

Today's session was one of the most practical and engaging sessions of the internship so far. Learning how to actively enumerate systems using Nmap and Gobuster demonstrated how reconnaissance progresses from passive information gathering to identifying accessible services and hidden resources. Solving the ThunderCipher labs reinforced the importance of systematic enumeration and showed how combining multiple tools leads to more effective security assessments.

---

# Next Steps

- Practice advanced Nmap scan techniques.
- Explore additional NSE scripts.
- Learn virtual host enumeration.
- Practice Gobuster with larger wordlists.
- Continue solving web enumeration labs to strengthen reconnaissance skills.