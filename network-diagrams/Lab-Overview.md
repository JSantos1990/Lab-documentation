# 🏠 Home Lab Overview & Network Topology

This document describes the initial design of my cybersecurity home lab.
It outlines the network topology, the virtual machines used, and the purpose of each component.
Future screenshots will be added as I build the lab environment.

---

## 🌐 1. Lab Objectives

The main goals of this home lab are:

- Practice SOC and Blue Team workflows
- Analyze logs from Windows, Linux, and network devices
- Deploy and test SIEM tools
- Build and secure a Windows Active Directory environment
- Capture network traffic and investigate PCAPs
- Test common attack and defense scenarios
- Automate tasks using Python and Bash

---

## 🖥️ 2. Network Topology (Initial Draft)

Below is the first version of the lab network diagram (ASCII draft).
A more detailed visual diagram (Draw.io) will be added later.

[ ASCII NETWORK DIAGRAM — WILL BE REPLACED LATER ]

                    [ Internet ]
                         |
                     [ Router ]
                         |
                 -----------------
                 |               |
          [ Admin PC ]      [ Home Lab Switch ]
                                 |
         -------------------------------------------------
         |                  |                 |         |
 [ Windows DC ]     [ Windows Client ]   [ Ubuntu SIEM ]  [ Kali / Attacker VM ]

📸 Screenshot placeholder: Full Draw.io diagram will be added here.

---

## 🧱 3. Components & Roles

### 🔵 Windows Domain Controller (DC)
**Purpose**
- Active Directory domain services
- User/group management
- Kerberos authentication
- GPO policy testing

📸 Screenshot placeholder: Windows Server setup.

---

### 🟢 Windows Client Machine
**Purpose**
- Used for AD authentication tests
- Generating logs for SIEM ingestion
- Policy testing and monitoring

📸 Screenshot placeholder: Windows client VM.

---

### 🟣 Ubuntu SIEM Server (Elastic / Wazuh)
**Purpose**
- Store and visualize logs from all machines
- Detect suspicious behavior
- Build dashboards
- Test ingestion pipelines

📸 Screenshot placeholder: SIEM dashboard.

---

### 🔴 Kali / Attacker VM
**Purpose**
- Running controlled attack simulations
- Testing detection rules
- Practicing ethical offensive techniques

📸 Screenshot placeholder: attacker VM interface.

---

## 🔌 4. Network Segments

For simplicity, the initial setup uses one segment:

`192.168.1.0/24`

All machines will be assigned static IPs later to keep logs consistent.

📸 Screenshot placeholder: Network adapter settings.

---

## ⚙️ 5. Hypervisor Used

Recommended hypervisors for this lab:

- VirtualBox
- VMware Workstation
- Proxmox (future expansion)

📸 Screenshot placeholder: Virtual machine list.

---

## 🧭 6. Future Improvements (Roadmap)

- [ ] Add professional Draw.io diagram
- [ ] Configure Windows Server 2022 AD
- [ ] Install Wazuh + Filebeat + Winlogbeat
- [ ] Configure Sysmon on Windows
- [ ] Route all logs into Elastic SIEM
- [ ] Test brute-force attack scenario
- [ ] Create detection rules for login anomalies
- [ ] Add Suricata or Zeek to the network

---

## 📝 7. Notes

This document will evolve as the lab grows.
Screenshots, diagrams, and configuration files will be added progressively.

---
