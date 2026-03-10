
---

# SOC Threat Detection Lab using Splunk

## Project Overview

This project demonstrates a **Security Operations Center (SOC) threat detection lab** built using **Splunk Enterprise** to monitor, analyze, and detect suspicious activities from **Windows Security Logs**.

The lab simulates **multiple failed login attempts** to replicate a **brute-force attack scenario** and demonstrates how a SOC analyst can detect, investigate, and respond using SIEM tools.

This project provides practical experience in **log analysis, threat detection, SIEM monitoring, dashboard creation, and alert configuration**.

---

# Objectives

* Build a **basic SOC monitoring environment**
* Collect and analyze **Windows Security Event Logs**
* Detect suspicious authentication activity
* Create **security monitoring dashboards**
* Configure **automated threat detection alerts**

---

# Tools & Technologies

* **Splunk Enterprise**
* **Splunk Universal Forwarder**
* **Windows 10**
* Virtual Machine Environment

---

# Lab Architecture

SOC Environment consists of:

**1. Splunk Server**

* Collects logs
* Analyzes security events
* Generates alerts

**2. Windows Machine**

* Generates authentication logs
* Sends security logs to Splunk

**3. Splunk Universal Forwarder**

* Collects Windows logs
* Forwards logs to Splunk SIEM

```
Windows Machine
      │
      │  Security Logs
      ▼
Splunk Universal Forwarder
      │
      ▼
Splunk Enterprise (SIEM)
      │
      ├── Log Analysis
      ├── Dashboards
      └── Alerts
```

---

# Implementation Steps

## 1. Lab Environment Setup

* Installed **Splunk Enterprise** on the main system.
* Set up a **Windows machine** to generate security logs.
* Created a small virtual lab environment for monitoring and analysis.

---

## 2. Windows Log Collection Setup

* Installed **Splunk Universal Forwarder** on the Windows system.
* Configured the forwarder to collect **Windows Security Event Logs**.
* Connected the forwarder to the **Splunk server**.

---

## 3. Log Ingestion

* Verified that Windows logs were successfully ingested into **Splunk Web**.
* Created a custom index:

```
index=windows_logs
```

* Confirmed that security events were visible in Splunk search.

---

## 4. Suspicious Activity Simulation

To simulate suspicious authentication activity:

* Multiple **incorrect login attempts** were performed on the Windows system.
* This generated security events that mimic **brute-force attack patterns**.

These events were captured and analyzed using Splunk.

---

# Log Analysis

The following Windows Event IDs were analyzed:

| Event ID | Description                 |
| -------- | --------------------------- |
| 4625     | Failed Login Attempt        |
| 4624     | Successful Login            |
| 4634     | User Logoff                 |
| 4672     | Special Privileges Assigned |

Example Splunk Query:

```
index=windows_logs EventCode=4625
```

This query displays **all failed login attempts**.

---

# Dashboard Creation

SOC monitoring dashboards were created to visualize security activity.

Dashboard Panels:

1. Failed Login Attempts
2. Login Activity Timeline
3. Top Users with Failed Logins
4. Authentication Activity Overview

These dashboards help SOC analysts quickly detect suspicious patterns.

---

# Alert Configuration

An automated alert rule was configured in **Splunk Enterprise**.

### Alert Condition

Trigger an alert when:

**More than 5 failed login attempts occur within 1 minute**

Example detection query:

```
index=windows_logs EventCode=4625
| stats count by user
| where count > 5
```

This helps detect **possible brute-force attacks**.

---

# Investigation Process

SOC investigation steps included:

1. Identify repeated failed login attempts
2. Check user accounts involved
3. Analyze login patterns
4. Investigate abnormal authentication activity
5. Document incident findings

---

# Key Skills Demonstrated

* SIEM Monitoring
* Log Analysis
* Threat Detection
* Incident Investigation
* Security Dashboard Creation
* Alert Configuration
* SOC Operations

---

# Project Outcome

This project demonstrates hands-on experience with **Security Operations Center workflows** including:

* Monitoring Windows security logs
* Detecting suspicious authentication activity
* Investigating security events
* Configuring automated alerts

It simulates a **real-world SOC analyst workflow using Splunk Enterprise**.

---

# Future Improvements

* Integrate additional log sources
* Implement advanced threat detection rules
* Add automated incident response
* Integrate threat intelligence feeds

---

# Author

**Jas**
Cyber Security Enthusiast | SOC Analyst Aspirant

---


These will make your **GitHub look like an experienced SOC analyst profile.**
