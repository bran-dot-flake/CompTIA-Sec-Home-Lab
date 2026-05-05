# Brandon Chaney's CompTIA Security+ Homelab 

![Security+](https://img.shields.io/badge/CompTIA-Security%2B-blue)
![Status](https://img.shields.io/badge/Project-Complete-green)

A hands-on cybersecurity lab built to practice and demonstrate core concepts aligned with CompTIA Security+ objectives.

> **What is a homelab?**
> 
> A homelab is a personal computing environment used to build and experiment with servers, networks, and security tools outside of production systems. It is used to learn IT concepts, test configurations, and develop hands-on skills. For Security+ (Sec+) preparation, it helps practice topics like networking, system administration, identity and access management, firewalls, and basic security testing. It provides a safe space to experiment and troubleshoot without affecting real systems.


## Overview
This home lab demonstrates foundational cybersecurity concepts aligned with [CompTIA Security+](https://www.comptia.org/en-us/certifications/security/) objectives. It covers virtualization, network scanning, vulnerability assessment, system hardening, encryption, and network defense techniques using common security tools and Windows/Linux environments.

### Objectives
- [x] Virtualized lab environment setup  
- [x] Defense-in-depth implementation  
- [x] Vulnerability identification and exploitation  
- [x] [Identity and access management (IAM)](https://www.microsoft.com/en-us/security/business/security-101/what-is-identity-access-management-iam) 
- [x] Network security and [segmentation](https://www.cisco.com/site/us/en/learn/topics/security/what-is-network-segmentation.html)  
- [x] Traffic analysis and protocol security  
- [x] Vulnerability scanning and monitoring  
- [x] [System hardening](https://www.beyondtrust.com/resources/glossary/systems-hardening) and encryption  
- [x] Patch and change management  
- [x] Offensive vs defensive security concepts  

---

## Lab Environment
This lab was built in a virtual environment using VirtualBox to simulate a small network for hands-on cybersecurity practice. It included Windows 10 and Kali Linux virtual machines to explore both defensive and offensive security concepts in a safe setup. A variety of tools were used for tasks like network scanning, vulnerability testing, password analysis, traffic monitoring, and web security testing. Network and system security features such as firewalls, secure remote access, and router configuration were also explored, along with privacy tools like Tor.

### Tech Stack

| Tool | Logo | Description |
|------|------|-------------|
| VirtualBox | ![VirtualBox](https://img.shields.io/badge/VirtualBox-183A61?style=for-the-badge&logo=virtualbox&logoColor=white) | Virtual machines for isolated testing |
| Windows 10 | ![Windows](https://img.shields.io/badge/Windows%2010-0078D6?style=for-the-badge&logo=windows&logoColor=white) | Host OS for security testing |
| Kali Linux | ![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kalilinux&logoColor=white) | Penetration testing OS |
| PuTTY | ![PuTTY](https://img.shields.io/badge/PuTTY-1BA2F6?style=for-the-badge) | SSH remote access client |
| FileZilla | ![FileZilla](https://img.shields.io/badge/FileZilla-BF0000?style=for-the-badge&logo=filezilla&logoColor=white) | FTP/SFTP file transfers |
| Angry IP Scanner | ![IP Scanner](https://img.shields.io/badge/Angry%20IP%20Scanner-FF6A00?style=for-the-badge) | Network host discovery |
| Nessus | ![Nessus](https://img.shields.io/badge/Nessus-00945E?style=for-the-badge&logo=tenable&logoColor=white) | Vulnerability scanning tool |
| Ophcrack | ![Ophcrack](https://img.shields.io/badge/Ophcrack-555555?style=for-the-badge) | Password cracking tool |
| PentestTools | ![PentestTools](https://img.shields.io/badge/PentestTools-2E2E2E?style=for-the-badge) | Web vulnerability scanner |
| Wireshark | ![Wireshark](https://img.shields.io/badge/Wireshark-1679A7?style=for-the-badge&logo=wireshark&logoColor=white) | Network traffic analyzer |
| Windows Defender Firewall | ![Firewall](https://img.shields.io/badge/Windows%20Firewall-0078D6?style=for-the-badge&logo=microsoftdefender&logoColor=white) | Traffic filtering and control |
| TP-Link Router | ![TP-Link](https://img.shields.io/badge/TP--Link-4ACBD6?style=for-the-badge&logo=tp-link&logoColor=white) | Network routing & VLAN testing |
| Tor Browser | ![Tor](https://img.shields.io/badge/Tor-7D4698?style=for-the-badge&logo=torproject&logoColor=white) | Anonymous browsing network |
---

## Table Of Conents

- [Lab Exercises](#lab-exercises)
  - [1. Virtualization Setup](#1-virtualization-setup)
  - [2. Snapshots & Change Management](#2-snapshots--change-management)
  - [3. Network Discovery](#3-network-discovery)
  - [4. Vulnerability Scanning](#4-vulnerability-scanning)
  - [5. Password Security & Cracking](#5-password-security--cracking)
  - [6. Web Application Security Testing](#6-web-application-security-testing)
  - [7. Network Traffic Analysis](#7-network-traffic-analysis)
  - [8. Secure Remote Access](#8-secure-remote-access)
  - [9. Password Policy Enforcement](#9-password-policy-enforcement)
  - [10. Steganography](#10-steganography)
  - [11. Disk Encryption](#11-disk-encryption)
  - [12. Role-Based Access Control (RBAC)](#12-role-based-access-control-rbac)
  - [13. Firewall Configuration](#13-firewall-configuration)
  - [14. Patch Management](#14-patch-management)
  - [15. System Hardening (Group Policy)](#15-system-hardening-group-policy)
  - [16. Wireless Security](#16-wireless-security)
  - [17. File Encryption](#17-file-encryption)
  - [18. Backup & Router Security](#18-backup--router-security)
  - [19. DMZ Configuration](#19-dmz-configuration)
  - [20. Anonymity & Threat Research](#20-anonymity--threat-research)
  - [21. Network Segmentation (VLANs)](#21-network-segmentation-vlans)
  - [22. Intrusion Prevention Systems](#22-intrusion-prevention-systems)
  - [23. Web Filtering](#23-web-filtering)

- [Key Takeaways](#key-takeaways)

- [Acknowledgements](#acknowledgements)

---

## Lab Exercises

### 1. Virtualization Setup
Installed VirtualBox and deployed Windows 10 and Kali Linux virtual machines to simulate a controlled security testing environment.
<p align="center">
  <img src="https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_e66d35dc.png"/>
  <br/>
  <em>Figure 1: Adding Windows 10 to VirtualBox</em>
</p>
<p align="center">
  <img src="https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_46eba064.png"/>
  <br/>
  <em>Figure 2: Adding Kali Linux to VirtualBox</em>
</p>

> This approach reflects the principle of safe isolation, allowing security testing and offensive techniques to be performed without risking production systems. Virtualization is widely used in cybersecurity for malware analysis, penetration testing, and lab simulations.

---

### 2. Snapshots & Change Management
Enabled VirtualBox snapshots to allow system rollback and safe configuration testing.
<p align="center">
  <img src="https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_49dcee31.png"/>
  <br/>
  <em>Figure 3: Enabling VirtualBox Snapshots</em>
</p>

> Snapshots support change management and system recovery, ensuring that configurations can be tested without permanent impact. This aligns with Security+ concepts around maintaining system integrity and minimizing downtime.

---

### 3. Network Discovery
Used IP scanning tools to identify active devices and map the local network.
<p align="center">
  <img src="https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_a8aefb3a.png">
   <br/>
  <em>Figure 4: Angry IP Scanner</em>
</p>
<p align="center">  
  <img src="https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_31319698.png">
  <br/>
  <em>Figure 5: Scanning Devices On Network</em>
</p>

> Network discovery is a key part of reconnaissance and asset identification, helping administrators understand what devices exist on a network and detect unauthorized or rogue systems.

---

### 4. Vulnerability Scanning
Performed vulnerability assessments using Nessus to identify system weaknesses and misconfigurations.
![Network Scan](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_812902af.png)

> Vulnerability scanning is a core component of risk management, enabling organizations to proactively identify and remediate known security flaws before they can be exploited.

---

### 5. Password Security & Cracking
Demonstrated password strength analysis using Ophcrack and brute-force/dictionary techniques in Kali Linux.

- Weak passwords were easily cracked  
- Complex passwords (e.g., `P@ssw0rd!`) significantly increased resistance  
- Dictionary-based attacks proved more effective than brute force in many cases  
![NTLM Password Hash](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_b56b9bec.png)
![Ophcrack Brute Force](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_58664aaf.png)
![Password Lookup Table](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_f01a4529.png)

> This highlights the importance of strong authentication practices and demonstrates how weak credentials can be exploited. It reinforces Security+ topics like password policies, hashing, and attack methods.

---

### 6. Web Application Security Testing
Used OWASP Juice Shop (intentionally vulnerable application) to explore common web vulnerabilities such as:
- SQL Injection  
- Cross-Site Scripting (XSS)
![Website Scanner - Inital](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_1063382b.png)
![Website Scanner - Findings](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_56d83f2d.png)
![Website Scanner - Info](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_79da1919.png)

> This demonstrates awareness of OWASP Top 10 risks, such as injection and XSS, emphasizing the importance of secure coding practices and input validation in web applications.

---

### 7. Network Traffic Analysis
Configured an insecure FTP server and captured login credentials using Wireshark to demonstrate plaintext transmission risks.
![FTP Server](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_d0ae9b20.png)
![FTP Server - Initialization](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_8fa07424.png)
![WireShark Sniffing](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_2a40852d.png)

> This illustrates the danger of unencrypted protocols and reinforces the need for secure alternatives (e.g., SFTP, HTTPS) to protect data in transit.

---

### 8. Secure Remote Access
Established SSH connections from Windows 10 using PuTTY to securely manage remote systems.
```bash
sudo apt install openssh-server
sudo service ssh start
```
![PuTTY](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_86ddb2bb.png)

> SSH provides encrypted remote administration, ensuring confidentiality and integrity of management traffic compared to insecure protocols like Telnet.

---

### 9. Password Policy Enforcement
Configured and enforced strong password policies to improve authentication security.
![Complex Password - Enable](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_a7f48d11.png)

> This aligns with identity and access management (IAM) principles, enforcing complexity and reducing the risk of credential-based attacks.

---

### 10. Steganography
Embedded hidden messages within files to demonstrate covert data transmission techniques.
![Image Encode](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_cb20fdad.png)
![Image Decode](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_1049d852.png)
![Image - Comparison](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_eeb39e3a.png)

> Demonstrates data obfuscation techniques, which can be used for both legitimate privacy purposes and malicious data exfiltration, highlighting the need for monitoring and detection.

---

### 11. Disk Encryption
Enabled full disk encryption using built-in Windows encryption tools to protect data at rest.
![Windows Bitlocker](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_ae5c6c32.png)

> Protects data at rest, ensuring that sensitive information remains secure even if physical devices are lost or stolen.

---

### 12. Role-Based Access Control (RBAC)
Configured user roles and permissions within Windows to enforce least privilege access.
![Group Creation](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_457525e3.png)
![RBAC](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_5f0b4c28.png)

> Implements the principle of least privilege, limiting access to only what is necessary and reducing the attack surface.

---

### 13. Firewall Configuration
Configured Windows Firewall rules, including allowing FTP traffic for controlled services.
![Windows Firewall](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_ba660da.png)
![Firewall Outbound Rule](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_fb5553c9.png)
![Rule - Verification](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_8cec16d4.png)

> Firewalls enforce network security boundaries by controlling inbound and outbound traffic based on predefined rules.

---

### 14. Patch Management
Maintained system updates while acknowledging the need for controlled testing before deployment in production environments.
![Windows Update](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_304c236b.png)

> Patch management is critical for vulnerability mitigation, ensuring systems are protected against known exploits while minimizing operational risk.

---

### 15. System Hardening (Group Policy)
Applied Group Policy configurations to harden Windows systems and restrict insecure behaviors.
![Group Policy](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_1c727064.png)
![Group Policy - Denied](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_c0469226.png)

> System hardening reduces the attack surface by disabling unnecessary features and enforcing security configurations.

---

### 16. Wireless Security
Configured secure wireless networking using WPA3, changed default credentials, and created a guest network for IoT and segmented device access.
![Router WPA3](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_b05ccdef.png)
![Guest Network](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_c2cabf1b.png)

> Demonstrates secure network design, protecting wireless communications and isolating less-trusted devices to prevent lateral movement.

---

### 17. File Encryption
Applied file-level encryption to protect sensitive data within the operating system.
![File Encryption](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/5d3ffba17acda26162bded950596948b9f151f8e/images/Sec%2B%20Labs_html_843e94d5.png)

> Provides granular data protection, ensuring sensitive files remain secure even within a system.

---

### 18. Backup & Router Security
Performed router configuration backups, firmware updates, and restoration procedures to ensure recovery readiness.
![Router Backup](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_fbdb749b.png)
![Router Update](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_ac62b44.png)
![Router Update - Apply](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_98519a75.png)

> Supports disaster recovery and business continuity, ensuring configurations can be restored and vulnerabilities in firmware are addressed.

---

### 19. DMZ Configuration
Configured a Demilitarized Zone (DMZ) to isolate public-facing services from internal network resources.
![DMZ](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_8ccf410.png)

> A DMZ adds a layered defense strategy, isolating public-facing services from internal networks to reduce risk.

---

### 20. Anonymity & Threat Research
Used the Tor network to explore anonymity concepts and privacy-focused browsing techniques.
![Tor - Connect](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_f2dfe51c.png)
![Tor - Connected](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_153f9170.png)

> Highlights anonymity and privacy concepts, as well as how such tools may be used in both legitimate and malicious contexts.

---

### 21. Network Segmentation (VLANs)
Implemented VLANs to separate network traffic and improve security boundaries.
![VLAN - Add](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_fb5553c9.png)
![VLAN - Added](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_3079537f.png)

> Segmentation limits lateral movement and improves containment during a security incident.

---

### 22. Intrusion Prevention Systems
Explored IPS concepts and configuration to detect and prevent malicious network activity.
![IPS - On](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_c91ce3c.png)

> IPS solutions provide real-time threat detection and prevention, actively blocking malicious activity.

---

### 23. Web Filtering
Configured web filtering controls to restrict access to malicious or non-productive websites.
![Web Filtering - On](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_b4229ddf.png)
![Web Filtering - Rule](https://github.com/bran-dot-flake/CompTIA-Sec-Home-Lab/blob/ddd0b821353775217e7be22f8f8566397e094f67/images/Sec%2B%20Labs_html_cd60a6bf.png)

> Helps enforce acceptable use policies and protects users from malicious or high-risk websites.

---

## Key Takeaways
- Network segmentation and least privilege are essential for defense-in-depth  
- Weak authentication remains one of the easiest attack vectors  
- Encryption (data at rest and in transit) significantly improves security posture  
- Monitoring tools like Wireshark and Nessus provide critical visibility into threats  
- Proper configuration and hardening are just as important as security tools  

---

## Reflection

Building and documenting this home lab gave me a clearer understanding of how cybersecurity concepts apply in real environments. More than simply learning definitions, I was able to see how different security controls (like network segmentation, encryption, and access controls) work together to protect systems. Setting this lab up and strengthening secury as well as causing failure points within a controlled environment helped reinforce the importance of layering defenses rather than relying on a single tool or configuration.

One of the biggest takeaways for me was how easy common weaknesses like poor password practices or unencrypted protocols can be exploited; running tools like vulnerability scanners and packet analyzers made those risks feel much more tangible. It also showed me that security isn’t just about deploying tools, but rather configuring them properly and understanding what they’re telling you.

This lab also helped me think more critically about the balance between usability and security. For example, implementing stricter policies or segmentation improves security, but it also requires more planning and management. Working through these trade-offs gave me a better appreciation for real-world security challenges.

Overall, this experience strengthened my understanding of core Security+ concepts and gave me hands-on exposure to both defensive and offensive techniques. It’s made me more confident in approaching security problems and more aware of how different components of a system can introduce risk if they’re not properly secured.

---

## Acknowledgements
- [Andrew Ramdayal, TIA Training: CompTIA Security+ SY0-701 course](https://www.udemy.com/share/10aebA3@dUBTAjCnBCejkPZSQi7kNBkx_G1MscfBq5WHy47wSwLocjbT4Ydzvb1l8oGpkIHafw==/)
