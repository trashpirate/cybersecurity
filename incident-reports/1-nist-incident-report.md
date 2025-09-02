# Incident Report Analysis

## Table of Contents
- [Overview](#overview)
- [Instructions](#instructions)
- [NIST Framework Analysis](#nist-framework-analysis)
  - [Summary](#summary)
  - [Identify](#identify)
  - [Protect](#protect)
  - [Detect](#detect)
  - [Respond](#respond)
  - [Recover](#recover)
- [Reflections/Notes](#reflectionsnotes)
- [Author Information](#author-information)

## Overview
This incident report is part of the Google Cybersecurity Professional course. It analyzes a realistic scenario and applies the NIST Cybersecurity Framework (CSF). The CSF is a voluntary framework that consists of standards, guidelines, and best practices to manage cybersecurity risk. 

## NIST Framework Analysis

### Summary
Employees reported that they were not able to access any network resousrces within the internal network for 2 hours due to an incoming flood of ICMP packets. The incident management team immediately blocked incoming ICMP packets to stop all non-critical network services and restoring critical network services. The cybersecurity team investigating the incident found that a malicious actor performed a ICMP flood attack by sending ICMP pings into the company's network through an unconfigured firewall. This allowed the attacker to overwhelm the network through an distributed denial of service (DDoS) attack. In response to the incident, the security team blocked all ICMP traffice, stopping non-critcal network services, so critical services could be resumed. 

### Identify
The security team audited the systems, devices, and access policies involved in the attack to identify gaps in the company's security posture. The team found that the firewall of the internal network was not configured properly allowing a malicious attacker to overwhelm the network with a ICMP packets performing a DDoS attack. This made the internal network unresponsive for over 2 hours halting all internal network traffic.

### Protect
The security team immediately blocked incoming ICMP packets, stopping all non-critical network services. After the attack, the team implemented new security measures to protect against future attacks: 
- a new firewall rule to rate limit the incoming ICMP traffic
- installed an IPS system to filter out ICMP traffic with suspicious characteristics

### Detect
To detect new ICMP flood attacks, the security team has hardened the newtork security by
- source IP verification on the firewall to detect spoofed IP addresses on incoming ICMP traffic
- installing network monitoring software to detect abnormal network traffic
- installing a IDS system to detect suspicious/harmful ICMP traffic

### Respond
The security team will make sure to monitor newtork traffic to the internal network using the installed SIEM and IDS tools. These tools will allow the team to identify ICMP flood attacks quickly and respond by isolating and blocking reponsiple IP addresses, and restore normal network traffic. The team will then analyze logs to check for suspicious activity. The team will also report on such incidents to upper management and legal entities where necessary.

### Recover
By isolating and blocking ICMP traffic from malicious IP addresses, taking non-critical network services offline, so critical network services can resume. After the attack, all non-critical network services can be resumed.

## Reflections/Notes
*The CSF is used to improve on existing security posture after an incident occurs. It helps to gather and structure relevant information about the incident for future reference and can inform future security guidelines.*

## Author Information
**Nadina (Oates) Zweifel**
Blockchain Engineer | Security Researcher | Web3 | Cybersecurity | PhD  
🌐 [trashpirate.io](https://trashpirate.io)  
✖️ [x.com/0xTrashPirate](https://x.com/0xTrashPirate)  
💻 [github.com/trashpirate](https://github.com/trashpirate)  
🔗 [linkedin.com/in/nadinaoates](https://linkedin.com/in/nadinaoates)


*This document is maintained in a public GitHub repository for collaboration and reference. Contributions or feedback are welcome via pull requests or issues.*

_Date: September 2, 2025_