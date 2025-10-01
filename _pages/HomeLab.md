
This page documents the design and build of my personal cybersecurity home lab.  
The lab is an **isolated, controlled environment** where I safely practice core skills such as reconnaissance, enumeration, exploitation, and defensive monitoring without impacting production systems.

The setup uses **VirtualBox**, a **Windows 10 VM** (victim/target), and a **Kali Linux VM** (attacker).  
By simulating both offensive and defensive roles, I explore how attackers identify and exploit vulnerabilities and how defenders detect, contain, and remediate threats. The lab supports hands-on work with tools like `nmap`, `smbclient`, `winPEAS`, Sysmon, Wireshark, and log aggregation stacks.

---

## 🎯 Goals of the Lab

- **Fundamentals**
  - Learn and practice TCP/IP, ports, and common protocol behavior (DNS, SMB, RDP, HTTP).
  - Build fluency with the Linux command line and Windows troubleshooting/PowerShell.

- **Offensive Skills**
  - Conduct safe discovery and enumeration (nmap, enum4linux, smbclient).
  - Execute controlled exploitation and post-exploitation techniques on intentionally vulnerable targets.
  - Practice credential harvesting, password-cracking (John/Hashcat), and lateral movement primitives.

- **Privilege Escalation**
  - Use automated enumeration (winPEAS/winpeas) and manual checks to identify escalation vectors.
  - Reproduce and remediate classic escalation scenarios (unquoted service paths, weak ACLs, scheduled tasks).

- **Defensive & Detection**
  - Install and configure Sysmon / Windows Event Forwarding / ELK or Wazuh for log collection.
  - Create detection rules for common attacker behaviors and validate through lab exercises.
  - Harden Windows settings (SMB signing, firewall policies, least privilege).

- **Operational Practice**
  - Maintain repeatable exercises using VM snapshots and documented playbooks.
  - Perform incident response drills and evidence collection on compromised VMs.
  - Track findings, remediation steps, and lessons learned in a lab notebook.

- **Career & Certification Prep**
  - Map exercises to skills required for roles/certifications (SOC Analyst, Pentester, Azure security tasks).
  - Produce reproducible write-ups and evidence for portfolio/demo use.

---



## Getting Started
[📄 View PDF](/assets/Home_Lab/setupLab.pdf)
---
## Priviledge Escalation(WinPeas)
[📄 View PDF](/assets/Home_Lab/PriviledgeEscalation.pdf)
---
