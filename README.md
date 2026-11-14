# Network Scanning and Network Security Assessment

## Apex Planet Cybersecurity Internship

### Project Overview
This project focuses on understanding network reconnaissance, network scanning, vulnerability assessment, network traffic analysis, and firewall configuration.

The practical exercises were performed in an isolated virtual lab environment using Kali Linux and Metasploitable2.

## Objectives

- Perform passive and active reconnaissance.
- Identify active hosts in a network.
- Discover open ports and running services using Nmap.
- Perform vulnerability assessment using OpenVAS.
- Capture and analyze network traffic using Wireshark.
- Understand TCP, UDP, HTTP, FTP and DNS traffic.
- Configure basic firewall rules using iptables.
- Understand how firewall rules affect network scanning.

## Lab Environment

| Component | Details |
|---|---|
| Attacker Machine | Kali Linux |
| Target Machine | Metasploitable2 |
| Virtualization | Oracle VirtualBox |
| Network Mode | Host-Only Adapter |
| Scanning Tool | Nmap |
| Vulnerability Scanner | OpenVAS / Greenbone |
| Traffic Analyzer | Wireshark |
| Firewall | iptables |
| Additional Tools | WHOIS, Netcat, hping3 |

## Target Information

- Target IP: 192.168.56.101
- Attacker: Kali Linux
- Target: Metasploitable2
- Network: Isolated Host-Only Lab

## 1. Reconnaissance

Reconnaissance is the process of collecting information about a target before performing security testing.

### Tools Used
- WHOIS
- Nslookup
- Google Dorking
- Shodan
- Ping
- Netcat

### Activities
- Domain information gathering.
- DNS lookup.
- Search engine reconnaissance.
- Host discovery.
- Basic service banner identification.

## 2. Network Scanning Using Nmap

Nmap was used to discover active hosts, open ports, services and operating system information.

### Commands Used

Host discovery:

    nmap -sn 192.168.56.0/24

TCP SYN scan:

    nmap -sS 192.168.56.101

UDP scan:

    sudo nmap -sU 192.168.56.101

Service version detection:

    nmap -sV 192.168.56.101

Operating system detection:

    sudo nmap -O 192.168.56.101

Combined scan:

    sudo nmap -sS -sV -O -oN nmap_report.txt 192.168.56.101

### Purpose

- Identify open ports.
- Detect running services.
- Identify service versions.
- Understand possible security weaknesses.

## 3. Vulnerability Assessment Using OpenVAS

OpenVAS (Greenbone Vulnerability Management) was configured to assess the target system.

### Activities
- Configure scanner.
- Synchronize vulnerability feeds.
- Create a scan target.
- Configure a scan task.
- Run vulnerability assessment.
- Review discovered vulnerabilities.

Note: Assessment results are documented after successful scan completion and report generation.

## 4. Network Traffic Analysis Using Wireshark

Wireshark was used to capture and inspect network packets.

### Protocols Studied
- HTTP
- FTP
- DNS
- TCP
- UDP

### Display Filters

HTTP:

    http

FTP:

    ftp

DNS:

    dns

TCP:

    tcp

UDP:

    udp

### Objective

Understand packet communication and identify potentially insecure traffic, including unencrypted protocol communication.

## 5. Firewall Configuration Using iptables

Basic firewall rules were explored to understand network traffic filtering.

### Commands

Display firewall rules:

    sudo iptables -L -n -v

Allow HTTP traffic:

    sudo iptables -A INPUT -p tcp --dport 80 -j ACCEPT

Block FTP traffic:

    sudo iptables -A INPUT -p tcp --dport 21 -j DROP

Display updated rules:

    sudo iptables -L -n -v

Delete the FTP blocking rule after testing:

    sudo iptables -D INPUT -p tcp --dport 21 -j DROP

### Objective

- Understand INPUT chain policies.
- Allow and deny specific ports.
- Observe the effect of firewall rules.
- Understand how filtering affects network connectivity and scanning.

## 6. Controlled SYN Traffic Testing

A limited SYN packet test was performed in the isolated lab environment using hping3.

Example:

    sudo hping3 -S -p 80 -c 20 -i u100000 192.168.56.101

This was used to understand TCP SYN packets and observe network responses.

## Security Observations

The practical exercises demonstrate:

- The importance of identifying exposed services.
- Why outdated services require security assessment.
- The risks associated with unencrypted network protocols.
- How firewall rules can reduce unnecessary network exposure.
- Why regular vulnerability assessments are important.

Actual findings should be recorded from the generated scan reports and packet captures.

## Screenshots and Evidence

Screenshots of the practical exercises are organized in the Screenshots directory.

- Reconnaissance
- Nmap scanning
- OpenVAS vulnerability assessment
- Wireshark packet analysis
- Firewall configuration

## Conclusion

This project provided practical exposure to network reconnaissance, port scanning, vulnerability assessment, packet analysis and firewall configuration.

It helped develop an understanding of network security concepts and practical security testing techniques in an isolated virtual lab environment.

## Disclaimer

All testing was performed on an authorized, isolated virtual lab environment for educational purposes only.

No unauthorized systems or networks were scanned.
