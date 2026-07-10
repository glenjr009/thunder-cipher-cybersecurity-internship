# Day 05 - Networking Fundamentals II: DNS, DHCP, NAT & Subnetting

**Date:** 08 July 2026

---

# Objective

The objective of today's session was to understand core networking services that enable communication across modern networks. The session focused on DNS, DHCP, NAT, subnetting, and practical network reconnaissance using Kali Linux.

---

# Session Overview

Today's class expanded upon the networking concepts introduced in the previous session. We explored how domain names are resolved, how devices obtain IP addresses automatically, how Network Address Translation (NAT) works, and how subnetting is used to efficiently manage IP address spaces. The session concluded with hands-on exercises involving DNS enumeration and packet analysis using industry-standard networking tools.

---

# Topics Covered

* Domain Name System (DNS)
* DNS Resolution Process
* DNS Record Types
* Recursive vs Iterative Queries
* DNS Enumeration
* Dynamic Host Configuration Protocol (DHCP)
* DHCP DORA Process
* Network Address Translation (NAT)
* Types of NAT
* Private IP Address Ranges
* CIDR Notation
* Subnetting
* Passive Reconnaissance
* Packet Analysis
* Wireshark
* tcpdump

---

# Theory Notes

## Domain Name System (DNS)

DNS translates human-readable domain names into IP addresses, allowing users to access websites without remembering numerical IP addresses.

The DNS resolution process includes:

1. Local DNS Cache
2. Recursive Resolver
3. Root Server
4. Top-Level Domain (TLD) Server
5. Authoritative Name Server
6. DNS Response to Client

---

## DNS Record Types

We learned the purpose of several common DNS records.

| Record | Purpose                                                    |
| ------ | ---------------------------------------------------------- |
| A      | Maps a hostname to an IPv4 address                         |
| AAAA   | Maps a hostname to an IPv6 address                         |
| CNAME  | Alias for another domain name                              |
| MX     | Mail server information                                    |
| NS     | Authoritative Name Server                                  |
| TXT    | Domain verification and security records (SPF, DKIM, etc.) |
| SOA    | Start of Authority information                             |
| PTR    | Reverse DNS lookup                                         |

---

## DNS Enumeration

The instructor explained how DNS enumeration is used during reconnaissance to gather publicly available information about a target.

Topics discussed included:

* Identifying DNS records
* Reverse DNS lookups
* Zone Transfer (AXFR)
* WHOIS lookups
* Subdomain enumeration

The importance of conducting reconnaissance only against authorized targets was also emphasized.

---

## DHCP

Dynamic Host Configuration Protocol (DHCP) automatically assigns network configuration to devices joining a network.

Configuration obtained through DHCP includes:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

---

## DHCP DORA Process

The complete DHCP communication process was explained using the DORA model:

1. Discover
2. Offer
3. Request
4. Acknowledge (ACK)

Understanding this process helps explain how systems automatically receive network configurations.

---

## Network Address Translation (NAT)

NAT enables multiple private devices to share a single public IP address while accessing the internet.

Types of NAT discussed:

* Static NAT
* Dynamic NAT
* Port Address Translation (PAT)

The role of NAT in conserving IPv4 addresses and hiding internal network structures was also covered.

---

## Private IP Address Ranges

We studied the three private IPv4 address ranges defined under RFC 1918:

* 10.0.0.0/8
* 172.16.0.0/12
* 192.168.0.0/16

---

## Subnetting

Subnetting was introduced as a method of dividing large networks into smaller logical networks.

Concepts covered:

* CIDR notation
* Subnet masks
* Network addresses
* Broadcast addresses
* Usable host calculation

These concepts are fundamental for designing secure and efficient network infrastructures.

---

# Practical Session

The hands-on session focused on DNS enumeration and packet analysis.

Activities performed included:

* DNS lookups using `dig`
* DNS queries using `nslookup`
* Reverse DNS lookups
* WHOIS lookups
* Attempting DNS Zone Transfer (AXFR)
* DNS enumeration using automated tools
* Capturing DNS traffic using Wireshark
* Capturing packets using `tcpdump`
* Observing DNS request and response packets
* Understanding DHCP traffic and the DORA process through packet analysis

---

# Tools Introduced

| Tool      | Purpose                                    |
| --------- | ------------------------------------------ |
| dig       | DNS lookup utility                         |
| nslookup  | DNS query tool                             |
| host      | DNS lookup utility                         |
| whois     | Domain registration information lookup     |
| dnsenum   | Automated DNS enumeration                  |
| dnsrecon  | DNS reconnaissance framework               |
| fierce    | DNS reconnaissance and subdomain discovery |
| Sublist3r | Subdomain enumeration                      |
| Wireshark | Network packet analysis                    |
| tcpdump   | Command-line packet capture utility        |

---

# Commands Practiced

```bash
dig example.com A
dig example.com MX
dig -x 8.8.8.8

nslookup example.com

host example.com

whois example.com

dnsenum example.com

dnsrecon -d example.com -t std

fierce --domain example.com

sublist3r -d example.com

sudo tcpdump -i eth0 udp port 53 -n -v
```

---

# Key Learnings

* Understood how DNS translates domain names into IP addresses.
* Learned the purpose of common DNS record types.
* Explored the complete DNS resolution process.
* Understood DHCP and the DORA process.
* Learned how NAT enables communication between private and public networks.
* Studied CIDR notation and subnetting fundamentals.
* Performed DNS enumeration using multiple tools.
* Captured and analyzed DNS packets using Wireshark and tcpdump.
* Understood how reconnaissance supports information gathering during security assessments.

---

# Challenges Faced

No significant challenges were encountered during today's session. The practical exercises reinforced the networking concepts discussed during the theory portion and provided valuable experience using common reconnaissance and packet analysis tools.

---

# Assignment

The assignment involved practicing DNS enumeration and packet analysis by:

* Identifying DNS records for a target domain.
* Performing reverse DNS lookups.
* Capturing DNS traffic using Wireshark and tcpdump.
* Understanding DHCP packet exchanges through the DORA process.
* Analyzing how DNS information can support reconnaissance activities.

---

# Reflection

Today's session significantly strengthened my understanding of networking services that are fundamental to cybersecurity. Learning how DNS, DHCP, NAT, and subnetting operate behind the scenes provided valuable insight into real-world network communication. The hands-on exercises using Wireshark, tcpdump, and DNS enumeration tools demonstrated how these concepts are applied during reconnaissance and network analysis, making today's session one of the most practical and informative sessions of the internship so far.

---

# Next Steps

* Practice subnetting calculations independently.
* Explore advanced Nmap scanning techniques.
* Gain deeper familiarity with Wireshark filters.
* Practice DNS enumeration against authorized lab environments.
* Continue strengthening networking concepts for future penetration testing and incident response scenarios.
