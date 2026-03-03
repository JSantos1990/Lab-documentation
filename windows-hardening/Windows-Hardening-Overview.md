# 🪟 Windows Hardening Overview

This document provides an introduction to Windows hardening techniques used to secure enterprise environments.  
Screenshots will be added later as configuration steps are applied in the home lab.

---

## 🔐 1. What Is Windows Hardening?

Windows hardening reduces the attack surface by configuring:

- User access control
- Firewall rules
- System policies
- Logging and auditing
- Service security

It is essential for preventing privilege escalation and lateral movement.

📸 Screenshot placeholder: Local Security Policy window.

---

## 👤 2. User Account & Access Control

Key steps:

- Disable or rename default administrator account
- Enforce strong password policies
- Limit membership of local Administrators group
- Enable UAC at secure settings

Tools involved:

- `lusrmgr.msc`
- `secpol.msc`

📸 Screenshot placeholder: Local Users and Groups panel.

---

## 🛡️ 3. Group Policy (GPO) Security Settings

GPO is critical for enforcing domain-wide configurations:

Common hardening policies include:

- Password & lockout policies
- Audit policies
- Restricted groups
- Firewall rules
- Service management
- Script enforcement

📸 Screenshot placeholder: GPO editor.

---

## 🌐 4. Windows Firewall

Hardening the firewall includes:

- Allow only required inbound services
- Disable unneeded outbound connections
- Enable logging
- Enforce rules with GPO

📸 Screenshot placeholder: Windows Firewall advanced view.

---

## 📊 5. Logging & Auditing

Critical logs:

- Security logs (authentication events)
- Sysmon logs
- PowerShell logs
- AppLocker logs
- RDP activity

Tools:

- Event Viewer
- Sysmon
- Winlogbeat

📸 Screenshot placeholder: Event Viewer security log.

---

## 🧭 6. Hardening Checklist

- [ ] Enforce GPO audit policies
- [ ] Configure Windows Firewall
- [ ] Enable Sysmon
- [ ] Restrict admin privileges
- [ ] Remove legacy protocols (SMBv1)
- [ ] Enable PowerShell logging

---

## 📝 7. Notes

Additional screenshots and real examples will be added during lab deployment.

---
