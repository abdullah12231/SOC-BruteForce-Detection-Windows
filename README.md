# SOC Brute Force Detection - Windows

## 📌 Project Overview
This project simulates and detects a brute force attack in a Windows environment using Event Viewer logs.  
The focus is on analyzing authentication events, identifying suspicious login patterns, and understanding how brute force attacks can be detected using Windows Security logs.

---

## 🧪 Lab Environment
- Windows Server (Active Directory Domain Controller)
- Windows 11 Client Machine
- VMware Virtualization Environment
- User Account: "Abdullah"

---

## 🛠️ Tools Used
- Windows Event Viewer
- Active Directory
- Windows Security Logs
- Notion (for dashboard visualization)
- VMware Workstation

---

## 🎯 Objective
- Simulate a brute force attack scenario
- Analyze Windows Event Logs (4624, 4625)
- Identify failed and successful login attempts
- Correlate events to detect suspicious behavior
- Document findings and visualize results using a dashboard

---

## ⚠️ Attack Scenario
Multiple failed login attempts (Event ID 4625) were observed targeting the user account "Abdullah".

These attempts were followed by a successful login (Event ID 4624), indicating that the correct credentials were eventually used.

The pattern of repeated failed attempts followed by a successful login is consistent with a brute force attack.

---

## 🔍 Detection Method
- Event ID 4625 → Failed login attempts  
- Event ID 4624 → Successful login  
- Analysis of:
  - Source IP (127.0.0.1 - localhost)
  - Logon Type (Type 2 - Interactive)
  - Status Codes (e.g., 0xC000006A for wrong password)

A high number of failed attempts within a short time window followed by a successful login indicates potential brute force activity.

---

## 📸 Screenshots
The repository includes the following screenshots:

- Windows 11 Client system information and connectivity tests
- Active Directory user creation
- Failed login attempts (Event ID 4625)
- Successful login (Event ID 4624)
- Logs access and permission issues
- Brute force simulation evidence

---

## 📊 Dashboard
A dashboard was created using Notion to visualize login attempts and attack progression.

The dashboard includes:
- Timeline of login attempts
- Failed vs successful logins
- Correlated events
- Visual representation of the attack flow

The dashboard was exported as a PDF and included in the project.

---

## 📁 Repository Structure
SOC-BruteForce-Detection-Windows/
│
├── README.md
├── report.pdf
│
├── /screenshots/
│ ├── 4624.png
│ ├── 4625.png
│ ├── BruteForce.png
│ ├── Win-11.png
│ ├── user1.png
│ ├── user1.1.png
│ ├── user1.2.png
│ └── userDeniedToReadLogs.png
│
└── /dashboard/
└── notion-dashboard.pdf



---

## ✅ Key Takeaways
- Understanding Windows authentication events is critical for SOC analysis
- Event IDs 4624 and 4625 are essential for login monitoring
- Repeated failed logins followed by success may indicate brute force attacks
- Log correlation and timeline analysis help in detecting suspicious behavior

---

## 📌 Author
Abdullah

---

## 📎 Notes
This project is part of a cybersecurity learning lab focused on Blue Team / SOC fundamentals and Windows log analysis.
