# SOC-BruteForce-Detection-Windows
SOC project simulating and detecting brute force attacks on Windows using Event Viewer logs, including log analysis, event correlation, detection logic, dashboard, and incident reporting.

This project demonstrates how to detect brute force login attempts on a Windows system using Event Viewer logs.

TOOLS :
- Windows Event Viewer
- Windows Logs (Security)
- Notion
- GitHub

Detection Logic : 
- Event ID 4625 → Failed login attempts
- Event ID 4624 → Successful login
- Detect multiple failed attempts followed by a successful login

