# 📊 SIEM Architecture & Log Ingestion Overview

This document provides an overview of the SIEM environment in my home lab.  
It explains the purpose of the SIEM, the architecture used, and the log ingestion pipeline.  
Screenshots will be added later as the lab configuration progresses.

---

## 🔎 1. What is a SIEM?

A Security Information and Event Management (SIEM) system is used to:

- Centralize logs from multiple devices and servers
- Detect suspicious or malicious behavior
- Correlate events across systems
- Provide dashboards for monitoring activity
- Trigger alerts based on predefined rules

SIEMs are widely used in SOC environments for visibility and detection.

📸 Screenshot placeholder: Example SIEM dashboard.

---

## 🧱 2. SIEM Components in This Lab

The initial SIEM setup includes:

### 🟣 Elasticsearch
Stores indexed log data for searching and analysis.

### 🟡 Kibana
Visual dashboard interface used to:

- Query logs  
- Build dashboards  
- Investigate alerts  
- Visualize network activity  

### 🔵 Wazuh or Winlogbeat (log shippers)
Agents installed on endpoints that send logs to the SIEM.

Types of logs collected:

- Windows Event Logs
- Sysmon logs
- Authentication logs
- System activity logs
- Application logs

📸 Screenshot placeholder: Log shipper configuration.

---

## 🌐 3. SIEM Network Architecture (Initial Draft)

Below is a simple logical view of how logs flow into the SIEM:

[ ASCII SIEM LOG FLOW DIAGRAM — TO BE REPLACED LATER ]

                  [ Windows Client ] ----\
                                           \
                  [ Windows DC ] ---------> [ Winlogbeat/Wazuh ] ---> [ Elastic / Wazuh Manager ]
                                           /
                       [ Linux Host ] ----/

                                               |
                                               v

                                       [ Kibana Dashboard ]

📸 Screenshot placeholder: Draw.io architecture diagram.

---

## 🔌 4. Log Sources Included in This Lab

### 🟦 Windows Server (Domain Controller)
- Authentication logs (4624, 4625, 4768, 4769, etc.)
- Kerberos activity
- Privilege escalation attempts
- GPO changes

### 🟩 Windows Client
- User logon activity
- File access
- Application logs

### 🟥 Linux (Ubuntu)
- Syslog
- Auth.log
- SSH activity
- System updates

### 🟧 Network Activity (optional future)
- Suricata alerts
- Zeek logs
- Firewall logs

📸 Screenshot placeholder: Log source overview.

---

## ⚙️ 5. Log Shipper Setup (High-Level)

General steps (details added later):

1. Install agent (Wazuh, Winlogbeat, or Filebeat)
2. Configure endpoint to send logs to SIEM server
3. Enable required modules (Windows, Sysmon, system logs, etc.)
4. Verify logs are being indexed
5. Build initial dashboards

📸 Screenshot placeholder: Winlogbeat test command output.

---

## 📈 6. Queries & Dashboards

Example dashboards to build later:

- Authentication attempts (success/failure)
- Kerberos activity overview
- Sysmon process tree analysis
- Network connection timeline
- Suspicious event alerts

📸 Screenshot placeholder: Kibana visualization.

---

## 🧭 7. Future Enhancements (Roadmap)

- [ ] Add Suricata to ingest IDS alerts  
- [ ] Add Zeek for network metadata logs  
- [ ] Configure alerting rules  
- [ ] Integrate with OSSEC/Wazuh  
- [ ] Correlate events across Windows + Linux  
- [ ] Create a “failed login investigation” dashboard  

---

## 📝 8. Notes

This document is the starting point for the SIEM environment.  
Screenshots, dashboards, and configuration files will be added as the SIEM is deployed and tested.

---
