# Day 06 - OSINT & Reconnaissance Methodology

**Date:** 09 July 2026

---

# Objective

The objective of today's session was to understand the fundamentals of Open-Source Intelligence (OSINT) and reconnaissance methodologies. The session focused on passive and active reconnaissance techniques, industry-standard OSINT tools, and building a structured target profile using publicly available information.

---

# Session Overview

Today's session introduced OSINT as the first phase of cybersecurity engagements such as penetration testing, red teaming, bug bounty hunting, and incident response. We learned the importance of intelligence gathering before exploitation and explored several tools used to enumerate publicly available information about a target. The session concluded with a hands-on OSINT challenge that combined multiple reconnaissance techniques.

---

# Topics Covered

* Introduction to OSINT
* Reconnaissance Methodology
* Passive Reconnaissance
* Active Reconnaissance
* Cyber Kill Chain – Reconnaissance Phase
* MITRE ATT&CK Reconnaissance
* PTES Intelligence Gathering
* WHOIS
* DNS Reconnaissance
* Shodan
* theHarvester
* Target Profiling
* Ethical and Legal Considerations in Reconnaissance

---

# Theory Notes

## Open-Source Intelligence (OSINT)

OSINT is the process of collecting intelligence from publicly available sources. It forms the foundation of reconnaissance and helps security professionals understand a target's digital footprint before performing any active assessments.

OSINT is widely used in:

* Penetration Testing
* Red Team Operations
* Bug Bounty Hunting
* Threat Intelligence
* Incident Response
* Digital Investigations

---

## Reconnaissance

Reconnaissance is the process of gathering information about a target before attempting any security assessment.

The reconnaissance workflow generally includes:

1. Footprinting
2. Enumeration
3. Infrastructure Mapping
4. DNS Analysis
5. Correlation
6. Reporting

---

## Passive Reconnaissance

Passive reconnaissance gathers publicly available information without directly interacting with the target's systems.

Examples include:

* WHOIS lookups
* Search engines
* DNS records
* Social media
* Public code repositories
* Shodan
* theHarvester

Passive reconnaissance is generally low-risk because it does not generate traffic toward the target.

---

## Active Reconnaissance

Active reconnaissance involves directly interacting with the target's infrastructure.

Examples include:

* Port Scanning
* Banner Grabbing
* Service Enumeration
* Live Host Discovery

Unlike passive reconnaissance, active techniques are detectable and should only be performed with proper authorization.

---

## WHOIS

WHOIS provides domain registration information including:

* Registrar
* Registration Date
* Expiry Date
* Name Servers
* Registrant Information (when publicly available)

This information assists in understanding the ownership and administrative details of a domain.

---

## DNS Reconnaissance

We learned how DNS information contributes to target profiling.

DNS records explored included:

* A Records
* MX Records
* NS Records
* TXT Records

These records help identify hosting providers, mail servers, and other infrastructure components.

---

## Shodan

Shodan was introduced as a search engine for internet-connected devices.

The instructor demonstrated how Shodan can identify:

* Open Ports
* Running Services
* Service Banners
* Device Information
* Geographical Location

Understanding Shodan enables security professionals to assess an organization's exposed attack surface.

---

## theHarvester

theHarvester is an OSINT tool used to collect information from multiple public sources.

It can enumerate:

* Email Addresses
* Subdomains
* Hostnames
* Publicly Indexed Information

The collected data can be used to build a comprehensive reconnaissance profile.

---

## Legal & Ethical Considerations

A strong emphasis was placed on conducting reconnaissance ethically.

Key points discussed:

* Use only authorized targets.
* Passive reconnaissance is generally safer than active scanning.
* Active reconnaissance requires explicit written permission.
* Always operate within the defined scope of engagement.

---

# Practical Session

Today's hands-on activities focused on passive reconnaissance and OSINT.

Activities included:

* Performing WHOIS lookups
* Querying DNS records using `nslookup`
* Exploring internet-facing assets using Shodan
* Enumerating emails and subdomains using theHarvester
* Building a target profile by correlating information from multiple OSINT sources
* Participating in the ThunderCipher OSINT Challenge

---

# Tools Introduced

| Tool         | Purpose                                      |
| ------------ | -------------------------------------------- |
| WHOIS        | Domain registration information              |
| nslookup     | DNS record lookup                            |
| dig          | Advanced DNS queries                         |
| Shodan       | Search engine for internet-connected devices |
| theHarvester | Email, host, and subdomain enumeration       |

---

# Commands Practiced

```bash
whois example.com

nslookup example.com

nslookup -type=MX example.com

nslookup -type=NS example.com

nslookup -type=TXT example.com

dig example.com ANY +noall +answer

theHarvester -d example.com -b google,bing,crtsh

theHarvester -d example.com -b all -l 200
```

---

# Key Learnings

* Understood the role of OSINT in cybersecurity engagements.
* Differentiated between passive and active reconnaissance.
* Learned how reconnaissance fits into the Cyber Kill Chain and MITRE ATT&CK framework.
* Explored domain intelligence using WHOIS.
* Performed DNS reconnaissance using nslookup and dig.
* Learned how Shodan identifies publicly exposed systems and services.
* Used theHarvester to enumerate emails, hosts, and subdomains.
* Understood the importance of documenting reconnaissance findings before moving to vulnerability assessment.

---

# Challenges Faced

No significant challenges were encountered during today's session. The practical exercises provided valuable exposure to industry-standard OSINT tools and demonstrated how multiple sources of publicly available information can be combined to build a comprehensive reconnaissance profile.

---

# Assignment

The assignment involved completing the ThunderCipher OSINT Challenge by creating a comprehensive reconnaissance profile for an authorized target. The profile included:

* WHOIS information
* DNS records
* Name Servers
* Mail Servers
* Shodan findings
* Discovered subdomains
* Email addresses
* Observed security weaknesses

---

# Reflection

Today's session demonstrated that effective cybersecurity begins with thorough reconnaissance. Before any vulnerability assessment or penetration test, understanding the target's publicly available information is essential. Learning how to use WHOIS, Shodan, theHarvester, and DNS reconnaissance techniques provided valuable insight into how security professionals map an organization's attack surface while remaining within ethical and legal boundaries. The OSINT challenge reinforced the importance of correlating information from multiple sources to produce a well-documented reconnaissance report.

---

# Next Steps

* Practice OSINT techniques against authorized lab environments.
* Explore advanced Google Dorking and Certificate Transparency logs.
* Improve proficiency with Shodan search filters.
* Learn additional reconnaissance tools such as Amass and Subfinder.
* Prepare for active scanning techniques in the upcoming sessions.
