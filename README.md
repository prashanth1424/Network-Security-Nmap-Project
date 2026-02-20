# Network Enumeration & Vulnerability Assessment Project

### 🛡️ Project Overview
This project demonstrates the use of **Nmap (Network Mapper)** for network discovery, service version detection, and vulnerability assessment. The goal was to map a local network environment, identify active hosts, and audit them for critical security flaws (specifically SMB vulnerabilities).

### 🔧 Tools Used
* **Nmap:** Network discovery and security auditing.
* **NSE (Nmap Scripting Engine):** Automated vulnerability scanning.
* **Kali Linux:** Operating environment.

### 💻 Technical Execution
**1. Network Sweep & Discovery**
Executed a ping sweep to identify live hosts within the `10.0.2.0/24` subnet, mapping the network topology without triggering heavy traffic alerts.

**2. Service Version Detection**
Performed a targeted scan on the host (`10.0.2.2`) to identify running services:
* `Port 135`: Microsoft Windows RPC
* `Port 445`: Microsoft-DS (SMB)
* `Port 3306`: MySQL Database (v8.0.43)

**3. Vulnerability Assessment (NSE)**
Utilized the Nmap Scripting Engine to audit the SMB protocol for high-risk vulnerabilities, specifically checking for `ms10-061` (Print Spooler) and `ms10-054` memory corruption flaws.

### 📊 Results & Analysis
The scan confirmed the host is **not vulnerable** to the tested SMB exploits (`ms10-054: false`). However, the detection of an open MySQL port (3306) indicates a potential attack surface that requires strong authentication policies to secure.

---
*This project was built as part of a hands-on cybersecurity portfolio.*
