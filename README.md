# 🔐 Task 3: Perform a Basic Vulnerability Scan on Your PC (Cybersecurity Internship)

## 🎯 Objective
Use a vulnerability scanner like **OpenVAS** or **Nessus Essentials** to scan your own system, identify weaknesses, and learn the basics of **vulnerability management**.

---

## 🛠 Tools Required
- **Kali Linux** or Ubuntu (with OpenVAS installed)
- OR **Nessus Essentials** (Free for personal use)

---

## ✅ Step-by-Step Guide

### 🔹 Step 1: Install OpenVAS
```bash
sudo apt update
sudo apt install openvas
sudo gvm-setup
sudo gvm-check-setup
```
Start scanner:
```bash
sudo gvm-start
```
Access via: `https://localhost:9392`

Alternatively, install Nessus from: https://www.tenable.com/products/nessus/nessus-essentials

### 🔹 Step 2: Set Your Target
- Choose **localhost (127.0.0.1)** or your own IP as the scan target.
- In Nessus/OpenVAS, create a new scan with default profile.

### 🔹 Step 3: Start a Full Vulnerability Scan
- Name the scan (e.g., "Localhost Vulnerability Scan").
- Launch it.
- ⚠️ Takes 30–60 minutes depending on system.

📸 Screenshot examples:
- `screenshots/openvas_launch.png`
- `screenshots/openvas_results.png`

### 🔹 Step 4: Review Vulnerabilities
After scan finishes:
- Review **high**, **medium**, **low** severity issues.
- Click on vulnerabilities to see:
  - **CVE IDs**
  - **CVSS Scores**
  - **Description and fix** suggestions

📸 Save screenshot: `screenshots/vuln_details.png`

---

## 🔎 Example Output Breakdown
| CVE ID     | CVSS Score | Risk Level | Description |
|------------|------------|------------|-------------|
| CVE-2021-26855 | 9.8 | Critical | Microsoft Exchange SSRF vulnerability |
| CVE-2020-0601  | 8.1 | High | Windows CryptoAPI spoofing vulnerability |
| CVE-2019-0708  | 9.8 | Critical | Remote Desktop Services RCE (BlueKeep) |

---

## 🧯 How to Fix Common Vulnerabilities
- **Install OS updates** (patch known CVEs)
- **Disable unused services** (reduce attack surface)
- **Enforce strong passwords** and 2FA
- **Use antivirus and host firewall**

---

## 📚 Key Concepts
- **Vulnerability Scanner**: Tool that scans systems for known flaws.
- **CVSS**: Common Vulnerability Scoring System; ranks severity from 0.0 to 10.0.
- **False Positive**: A reported vulnerability that isn’t actually exploitable.
- **Risk Score**: Combines likelihood and impact of a vulnerability.

---

## ❓ Interview Q&A

### 1. What is vulnerability scanning?
Vulnerability scanning is an **automated process** that inspects a system for known security issues and reports them with severity levels.

### 2. Difference between vulnerability scanning and penetration testing?
- **Vulnerability scanning** identifies issues but does **not exploit** them.
- **Penetration testing** actively exploits vulnerabilities to prove risk.

### 3. What are common vulnerabilities in personal computers?
- Outdated software (e.g., unpatched Windows)
- Weak passwords
- Open ports and insecure services (RDP, SMB)

### 4. How do scanners detect vulnerabilities?
They use **signatures**, **CVE databases**, and **network/service fingerprinting** to identify known issues.

### 5. What is CVSS?
A standardized scoring system that ranks vulnerability severity from **0 (informational)** to **10 (critical)**.

### 6. How often should vulnerability scans be performed?
- **Monthly** for personal systems
- **Weekly or continuously** for enterprise environments

### 7. What is a false positive?
When a scanner flags something as a vulnerability that **isn’t actually dangerous**.

### 8. How do you prioritize vulnerabilities?
Use a **risk matrix** considering:
- CVSS score
- Asset criticality
- Exploit availability
- Remediation effort

---

## 🗂 GitHub Repo Structure
```
vulnerability-scan-task/
├── README.md
├── screenshots/
│   ├── openvas_launch.png
│   ├── openvas_results.png
│   └── vuln_details.png
├── scan_report.pdf or scan_report.html
```



## ✅ Task Completed By:
**Nitin sanap**  
Cybersecurity Intern
