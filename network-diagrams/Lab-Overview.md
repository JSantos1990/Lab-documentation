# 🏠 Home Lab Overview & Network Topology

This document describes the initial design of my cybersecurity home lab.  
It outlines the network topology, the virtual machines used, and the purpose of each component.  
Future screenshots will be added as I build the lab environment.

---

## 🌐 1. Lab Objectives

The main goals of this home lab are:

- Practice SOC and Blue Team workflows  
- Analyze logs from multiple systems (Windows, Linux, network devices)  
- Deploy and test SIEM tools  
- Build and secure a Windows Active Directory environment  
- Capture network traffic and investigate PCAPs  
- Test common attack and defense scenarios  
- Automate tasks using Python and Bash  

---

## 🖥️ 2. Network Topology (Initial Draft)

Below is the first version of the lab network diagram.  
A more detailed visual diagram (Draw.io) will be added later.

```text
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
