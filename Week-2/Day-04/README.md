# Day 04 - Networking Fundamentals & Network Reconnaissance

**Date:** 07 July 2026

**Duration:** 6:30 PM – 8:30 PM

---

# Objective

The objective of today's session was to build a strong foundation in computer networking by understanding network communication models, common protocols, reconnaissance techniques, and practical network analysis tools used in cybersecurity.

---

# Session Overview

After the weekend break, the session focused on networking fundamentals, which are essential for every cybersecurity professional. We explored the OSI Model, TCP/IP communication, common ports and protocols, reconnaissance techniques, and concluded with hands-on exercises using industry-standard networking tools such as Nmap, Wireshark, and tcpdump.

---

# Topics Covered

* Networking Fundamentals
* OSI Model
* Security Relevance of Each OSI Layer
* TCP vs UDP
* TCP Three-Way Handshake
* ARP Spoofing
* Ports and Protocols
* Passive Reconnaissance
* Network Scanning using Nmap
* DNS Enumeration (`dig` and `nslookup`)
* ARP Table
* `ip neigh` Command
* `tcpdump`
* Wireshark Packet Analysis

---

# Theory Notes

## Networking Fundamentals

The session began with an introduction to networking concepts and how devices communicate over a network. Understanding networking is fundamental in cybersecurity because most attacks and defenses occur across networked systems.

---

## OSI Model

The OSI (Open Systems Interconnection) Model was explained in detail.

The seven layers include:

1. Physical Layer
2. Data Link Layer
3. Network Layer
4. Transport Layer
5. Session Layer
6. Presentation Layer
7. Application Layer

Each layer performs a specific function in data communication.

---

## Security Relevance of the OSI Model

The instructor explained how different attacks target different layers of the OSI Model.

Examples discussed included:

* ARP Spoofing at the Data Link Layer
* IP Routing at the Network Layer
* TCP communication at the Transport Layer
* Web-based attacks at the Application Layer

Understanding the security responsibilities of each layer helps in identifying attack vectors and implementing appropriate defenses.

---

## TCP vs UDP

The differences between TCP and UDP were discussed.

### TCP

* Connection-oriented
* Reliable communication
* Error checking
* Ordered packet delivery

### UDP

* Connectionless
* Faster communication
* No delivery guarantee
* Commonly used for streaming and real-time applications

---

## TCP Three-Way Handshake

We learned how TCP establishes a reliable connection using the three-way handshake.

The communication process consists of:

1. SYN
2. SYN-ACK
3. ACK

This process ensures that both devices are ready before data transmission begins.

---

## ARP Spoofing

An introduction to ARP Spoofing was provided.

Topics discussed:

* Purpose of the Address Resolution Protocol (ARP)
* ARP Cache
* ARP Poisoning attacks
* Risks associated with Man-in-the-Middle (MITM) attacks

---

## Ports and Protocols

The session covered commonly used network ports and their associated services.

Examples included:

| Protocol | Default Port |
| -------- | -----------: |
| FTP      |           21 |
| SSH      |           22 |
| Telnet   |           23 |
| SMTP     |           25 |
| DNS      |           53 |
| HTTP     |           80 |
| POP3     |          110 |
| IMAP     |          143 |
| HTTPS    |          443 |

Understanding ports is essential for network enumeration and security assessments.

---

## Passive Reconnaissance

Passive reconnaissance techniques were introduced as methods for gathering information without directly interacting with the target system.

The discussion emphasized how passive information gathering helps identify potential attack surfaces while minimizing detection.

---

# Practical Session

Today's hands-on exercises focused on network reconnaissance and traffic analysis.

Activities performed:

* Running Nmap scans for host and service discovery
* Exploring DNS records using `dig`
* Querying DNS information with `nslookup`
* Viewing the ARP table
* Inspecting neighboring devices using the `ip neigh` command
* Capturing packets using `tcpdump`
* Capturing and analyzing network traffic using Wireshark

These practical exercises demonstrated how networking tools are used during reconnaissance and network troubleshooting.

---

# Tools Introduced

| Tool      | Purpose                                   |
| --------- | ----------------------------------------- |
| Nmap      | Network discovery and port scanning       |
| Wireshark | Network packet capture and analysis       |
| tcpdump   | Command-line packet capture tool          |
| dig       | DNS lookup utility                        |
| nslookup  | DNS query tool                            |
| arp       | Display and manage the ARP table          |
| ip neigh  | View neighboring devices in the ARP cache |

---

# Commands Practiced

```bash
nmap

dig

nslookup

arp

ip neigh

tcpdump
```

---

# Key Learnings

* Understood the OSI Model and the role of each layer.
* Learned the security significance of every OSI layer.
* Differentiated between TCP and UDP communication.
* Understood the TCP Three-Way Handshake process.
* Learned the basics of ARP Spoofing.
* Studied commonly used ports and protocols.
* Explored passive reconnaissance techniques.
* Practiced network scanning using Nmap.
* Learned DNS enumeration using `dig` and `nslookup`.
* Captured and analyzed network traffic using Wireshark and `tcpdump`.

---

# Challenges Faced

No significant challenges were encountered during today's session. The practical exercises provided valuable hands-on experience and reinforced the networking concepts discussed during the theory session.

---

# Assignment

No separate assignment was provided. The practical networking exercises and packet analysis activities served as hands-on practice for the concepts covered.

---

# Reflection

Today's session highlighted the importance of networking knowledge in cybersecurity. Understanding how systems communicate, how network traffic flows, and how reconnaissance tools operate provides the foundation for penetration testing, threat analysis, and incident response. The hands-on experience with Nmap, Wireshark, and other networking utilities helped bridge the gap between theory and practical application, making this one of the most engaging sessions so far.

---

# Next Steps

* Practice Nmap scanning with different scan techniques.
* Explore additional Wireshark filters and packet analysis features.
* Revise common ports and protocols.
* Gain a deeper understanding of ARP-based attacks and network reconnaissance techniques.
