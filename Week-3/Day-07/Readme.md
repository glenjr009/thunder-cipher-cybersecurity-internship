# Day 07 - Scanning & Enumeration with Nmap

**Date:** 13 July 2026

---

## Objective

To understand the role of scanning and enumeration in penetration testing using Nmap and related tools, and to apply these concepts through practical labs on the ThunderCipher platform.

---

## Topics Covered

- Scanning vs Enumeration
- TCP Three-Way Handshake
- Port States
- Nmap Fundamentals
- Nmap Scan Types
- Host Discovery
- Service & Version Detection
- OS Fingerprinting
- Banner Grabbing
- Nmap Scripting Engine (NSE)
- Gobuster Directory Enumeration
- SSH Enumeration
- Basic Hydra Usage
- Legal & Ethical Considerations

---

## Practical Activities

- Performed host discovery using Nmap
- Scanned open ports and identified running services
- Used version detection (`-sV`) and OS fingerprinting (`-O`)
- Explored Nmap NSE scripts for service enumeration
- Enumerated web directories using Gobuster
- Observed banner grabbing techniques
- Solved guided ThunderCipher labs focused on scanning and enumeration

---

## Tools Used

| Tool | Purpose |
|------|---------|
| Nmap | Network scanning & service enumeration |
| NSE | Automated service enumeration |
| Gobuster | Directory enumeration |
| Netcat | Banner grabbing |
| Hydra | Password auditing (Introduction) |
| ThunderCipher Platform | Hands-on cybersecurity labs |

---

## Commands Practiced

```bash
nmap -sn <target>

sudo nmap -sS -sV -O <target>

sudo nmap -A <target>

nmap --script http-enum -p80 <target>

gobuster dir -u http://<target>/ -w /usr/share/wordlists/dirb/common.txt

nc -nv <target> 22

curl -I http://<target>
```

---

## Key Learnings

- Understood the difference between scanning and enumeration.
- Learned various Nmap scan techniques and their use cases.
- Performed service and version detection using Nmap.
- Explored NSE scripts for automated enumeration.
- Used Gobuster to discover hidden web directories.
- Applied reconnaissance techniques by solving ThunderCipher labs.

---

## Reflection

Today's session strengthened my understanding of the scanning and enumeration phase of penetration testing. The combination of Nmap, NSE, and Gobuster demonstrated how multiple tools work together to identify services, gather information, and prepare for deeper security assessments. The hands-on labs provided practical experience in applying these concepts within an authorized environment.

---

## Screenshots

Screenshots from the practical session are available in the `screenshots/` directory.