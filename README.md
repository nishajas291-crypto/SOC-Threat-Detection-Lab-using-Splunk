# SOC-Threat-Detection-Lab-using-Splunk
Project Overview
This project simulates a Security Operations Center (SOC) environment using Splunk to monitor, analyze, and detect potential threats from Windows security logs. It demonstrates end-to-end threat detection, log analysis, alerting, and incident investigation, providing practical experience in a SOC analyst workflow.

Key Features

Simulated SOC monitoring environment using Splunk and Kali Linux.

Collection and analysis of Windows security logs to identify suspicious activity.

Generation of security events to simulate attacks, such as brute-force login attempts.

Creation of interactive dashboards to visualize security events and authentication behavior.

Configuration of alerts for abnormal activity and potential security breaches.

Use of OSINT (Maltego) for mapping potential threat actors and connections.

Tools & Technologies

SIEM & Monitoring: Splunk

Operating System: Kali Linux, Windows

Threat Intelligence / OSINT: Maltego

Protocols & Logs: Windows Security Logs, TCP/IP, HTTP/HTTPS

Attack Simulation: Brute-force attempts, abnormal login generation

Objectives & Learning Outcomes

Understand and implement SOC monitoring workflows.

Gain hands-on experience in security log analysis and identifying anomalous behavior.

Learn to create custom dashboards and configure actionable alerts in Splunk.

Develop knowledge of incident investigation procedures for security events.

Apply OSINT techniques for threat actor analysis.

Project Structure
SOC_Threat_Detection_Lab/
│
├── Windows_Logs/               # Sample Windows security log files
├── Splunk_Dashboards/          # Dashboard JSON and configuration files
├── Alerts_Config/              # Pre-configured Splunk alert settings
├── Kali_Scripts/               # Scripts to generate simulated attacks
├── Maltego_Mappings/           # OSINT threat maps and entity relationships
└── README.md                   # Project documentation
Implementation Steps

Log Collection: Import Windows security logs into Splunk.

Event Simulation: Use Kali Linux to generate test events, such as failed logins or anomalous authentication attempts.

Analysis: Perform log analysis in Splunk to detect suspicious patterns.

Dashboard Creation: Build visual dashboards to monitor authentication activity and security events.

Alert Configuration: Set alerts to notify for brute-force attempts or other critical anomalies.

Threat Mapping (OSINT): Use Maltego to map potential threat actors and analyze relationships.

Results / Impact

Successfully simulated SOC monitoring for Windows security environments.

Detected abnormal authentication behaviors and potential brute-force attacks.

Visual dashboards and alerts provided real-time situational awareness for SOC analysts.

Strengthened understanding of SOC operations, threat intelligence, and incident response workflows.

Skills & Keywords Highlighted
SOC Analyst | Security Monitoring | Splunk | SIEM | Log Analysis | Threat Detection | Incident Investigation | Brute-Force Alerts | Dashboard Creation | Kali Linux | Maltego | OSINT | Windows Security Logs


Conclusion
This project provides hands-on, practical experience in SOC operations and security monitoring, simulating real-world scenarios to prepare for roles in cybersecurity, SOC L1 analyst positions, and incident response teams.
