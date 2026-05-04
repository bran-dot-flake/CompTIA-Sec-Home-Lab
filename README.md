# Sec+ Home Lab

## Overview
This home lab demonstrates foundational cybersecurity concepts aligned with CompTIA Security+ objectives. It covers virtualization, network scanning, vulnerability assessment, system hardening, encryption, and network defense techniques using common security tools and Windows/Linux environments.

---

## Lab Environment
- Virtualization: Oracle VirtualBox  
- Operating Systems: Windows 10, Kali Linux  
- Network: Internal lab network (isolated)  
- Tools: Nmap, Nessus, Wireshark, OWASP Juice Shop, Ophcrack, PuTTY, Tor Browser  

---

## Lab Exercises

### 1. Virtualization Setup
Installed VirtualBox and deployed Windows 10 and Kali Linux virtual machines to simulate a controlled security testing environment.

---

### 2. Snapshots & Change Management
Enabled VirtualBox snapshots to allow system rollback and safe configuration testing.

---

### 3. Network Discovery
Used IP scanning tools to identify active devices and map the local network.

---

### 4. Vulnerability Scanning
Performed vulnerability assessments using Nessus to identify system weaknesses and misconfigurations.

---

### 5. Password Security & Cracking
Demonstrated password strength analysis using Ophcrack and brute-force/dictionary techniques in Kali Linux.

- Weak passwords were easily cracked  
- Complex passwords (e.g., `P@ssw0rd!`) significantly increased resistance  
- Dictionary-based attacks proved more effective than brute force in many cases  

---

### 6. Web Application Security Testing
Used OWASP Juice Shop (intentionally vulnerable application) to explore common web vulnerabilities such as:
- SQL Injection  
- Cross-Site Scripting (XSS)  

---

### 7. Network Traffic Analysis
Configured an insecure FTP server and captured login credentials using Wireshark to demonstrate plaintext transmission risks.

---

### 8. Secure Remote Access
Established SSH connections from Windows 10 using PuTTY to securely manage remote systems.

---

### 9. Password Policy Enforcement
Configured and enforced strong password policies to improve authentication security.

---

### 10. Steganography
Embedded hidden messages within files to demonstrate covert data transmission techniques.

---

### 11. Disk Encryption
Enabled full disk encryption using built-in Windows encryption tools to protect data at rest.

---

### 12. Role-Based Access Control (RBAC)
Configured user roles and permissions within Windows to enforce least privilege access.

---

### 13. Firewall Configuration
Configured Windows Firewall rules, including allowing FTP traffic for controlled services.

---

### 14. Patch Management
Maintained system updates while acknowledging the need for controlled testing before deployment in production environments.

---

### 15. System Hardening (Group Policy)
Applied Group Policy configurations to harden Windows systems and restrict insecure behaviors.

---

### 16. Wireless Security
Configured secure wireless networking using WPA3, changed default credentials, and created a guest network for IoT and segmented device access.

---

### 17. File Encryption
Applied file-level encryption to protect sensitive data within the operating system.

---

### 18. Backup & Router Security
Performed router configuration backups, firmware updates, and restoration procedures to ensure recovery readiness.

---

### 19. DMZ Configuration
Configured a Demilitarized Zone (DMZ) to isolate public-facing services from internal network resources.

---

### 20. Anonymity & Threat Research
Used the Tor network to explore anonymity concepts and privacy-focused browsing techniques.

---

### 21. Network Segmentation (VLANs)
Implemented VLANs to separate network traffic and improve security boundaries.

---

### 22. Intrusion Prevention Systems
Explored IPS concepts and configuration to detect and prevent malicious network activity.

---

### 23. Web Filtering
Configured web filtering controls to restrict access to malicious or non-productive websites.

---

## Key Takeaways
- Network segmentation and least privilege are essential for defense-in-depth  
- Weak authentication remains one of the easiest attack vectors  
- Encryption (data at rest and in transit) significantly improves security posture  
- Monitoring tools like Wireshark and Nessus provide critical visibility into threats  
- Proper configuration and hardening are just as important as security tools  

---

## Future Improvements
- Expand SIEM logging and monitoring (e.g., Splunk or ELK stack)  
- Add Active Directory domain environment  
- Simulate real attack/defense scenarios (red vs blue team exercises)  
- Implement automated vulnerability scanning pipeline  
