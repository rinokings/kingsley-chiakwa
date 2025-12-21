# 🛡️ Microsoft Sentinel SOC Analyst Lab

A comprehensive hands-on security operations lab designed to simulate real-world cyber attacks, implement advanced detection logic (KQL), and automate incident response using SOAR (Security Orchestration, Automation, and Response).

## 🏗️ Lab Architecture
- **SIEM/SOAR:** Microsoft Sentinel (Azure)
- **Log Management:** Azure Log Analytics Workspace
- **Virtualization:** Oracle VirtualBox (Bridged Networking)
- **Attacker Node:** Kali Linux (Nmap, Hydra)
- **Victim Node:** Windows 10 Home (Hardened with Sysmon & Advanced Auditing)
- **Connectors:** Azure Monitor Agent (AMA), Microsoft Entra ID

## 🚀 Lab Scenarios (Triages)
I have documented four distinct attack phases, mimicking the MITRE ATT&CK framework. Each folder contains a detailed incident report, KQL queries, and evidence screenshots.

| Scenario | Focus | Tools Used | Status |
| :--- | :--- | :--- | :--- |
| **[01. Brute Force](./01-Brute-Force-RDP)** | Credential Access (RDP) | Hydra, Kali Linux | ✅ Complete |
| **[02. Persistence](./02-Persistence-Scheduled-Task)** | Scheduled Tasks | Windows CMD, Sysmon | ✅ Complete |
| **[03. Reconnaissance](./03-Internal-Recon)** | Discovery & Enumeration | Nmap, Net Commands | ✅ Complete |
| **[04. Impossible Travel](./04-Impossible-Travel)** | Identity & SOAR | Logic Apps, Entra ID | ✅ In Progress |

## 🛠️ Technical Skills Demonstrated
- **Kusto Query Language (KQL):** Writing custom detection rules and hunting queries.
- **Log Analysis:** Deep dive into Windows Security Events (4625, 4698, 4740) and Sysmon (Event ID 1, 3).
- **Automation:** Building Azure Logic App Playbooks for automated user notification and account locking.
- **Incident Triage:** Following the full lifecycle of an incident from alert to remediation.

## 📁 Repository Structure
- `/01-Brute-Force-RDP`: Analysis of RDP brute force attempts.
- `/02-Persistence`: Detecting malicious scheduled tasks.
- `/Config-Files`: Includes `Sysmon-Config` and custom `DCR` templates used.
