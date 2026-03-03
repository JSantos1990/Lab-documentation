# 🪟 Active Directory Overview & Initial Setup

This document provides an overview of the Windows Active Directory (AD) environment used in my home lab.  
It explains the purpose of AD, the components involved, and the initial setup steps.  
Screenshots will be added later as the lab is fully deployed.

---

## 📘 1. What is Active Directory?

Active Directory (AD) is Microsoft’s directory service used to:

- Store information about users, groups, and devices
- Centralize authentication and authorization
- Apply policies to Windows systems (GPO)
- Provide secure access to resources in a networked environment

It is commonly found in enterprise networks and is a critical part of security operations.

📸 Screenshot placeholder: Diagram of AD domain structure.

---

## 🧩 2. Core Components of an Active Directory Domain

### 🔵 Domain Controller (DC)
The server responsible for:
- Authenticating users via Kerberos
- Managing user/group accounts
- Applying domain-wide policies
- Storing AD database (NTDS.dit)

📸 Screenshot placeholder: Server Manager on Windows Server.

---

### 🟠 Users & Groups
AD stores security principals such as:
- Standard user accounts
- Admin users
- Security groups (global, domain local, universal)
- Organizational units (OU)

📸 Screenshot placeholder: AD Users & Computers window.

---

### 🟣 Group Policy Objects (GPO)
Policies used to configure Windows machines automatically:
- Password policies
- Audit & security settings
- Software restrictions
- Firewall settings

📸 Screenshot placeholder: Group Policy Management Console.

---

### 🟢 DNS Service
AD integrates with DNS for:
- Locating domain controllers
- Resolving hostnames inside the domain

📸 Screenshot placeholder: DNS Manager interface.

---

## ⚙️ 3. Initial Lab Setup Plan

This home lab will contain:

- 1 × Windows Server 2022 — Domain Controller  
- 1 × Windows 10/11 Client — Joined to the domain  
- 1 × Sysmon + Winlogbeat — For log collection  
- Future: Additional servers for testing GPO and escalations  

📸 Screenshot placeholder: Virtual machine list.

---

## 🛠️ 4. Installing Windows Server (Domain Controller)

Steps (screenshots will be added later):

1. Create a new Virtual Machine  
2. Allocate ~4GB RAM and 2 CPUs  
3. Install Windows Server 2022  
4. Set server name (e.g., `LAB-DC01`)  
5. Configure static IP  
6. Install AD Domain Services role  
7. Promote server to Domain Controller  
8. Create domain name (e.g., `lab.local`)

📸 Screenshot placeholder: AD DS installation wizard.

---

## 🔐 5. Creating Users & OUs

Once AD is installed:

1. Open *Active Directory Users and Computers*  
2. Create Organizational Units:  
   - `LAB-Admins`  
   - `LAB-Workstations`  
   - `LAB-Users`  
3. Create test users  
4. Assign users to groups  
5. Join Windows Client to the domain

📸 Screenshot placeholder: OU structure.

---

## 📊 6. Logging & Monitoring Integration

The AD environment will be integrated with the SIEM for:

- Windows Event Logs  
- Sysmon logs  
- Authentication patterns  
- Privilege escalation attempts  

Tools used:

- Winlogbeat  
- Sysmon  
- Wazuh or Elastic Stack

📸 Screenshot placeholder: Sysmon configuration.

---

## 🧭 7. Future Enhancements (Roadmap)

- [ ] Add second Domain Controller  
- [ ] Implement password policies via GPO  
- [ ] Configure audit policies  
- [ ] Test Kerberoasting attack  
- [ ] Create detection rules in SIEM  
- [ ] Add Windows file server  
- [ ] Add Linux machine joined to AD (SSSD)

---

## 📝 8. Notes

This document introduces the AD environment used in the home lab.  
More technical configurations and screenshots will be added as the lab evolves.

---
