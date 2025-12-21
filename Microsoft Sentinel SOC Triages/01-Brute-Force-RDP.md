# Triage Report: RDP Brute Force Detection

## 🛡️ Scenario Overview
Simulated an external brute force attack originating from a Kali Linux VM targeting a Windows 10 victim.

## 🔍 Investigation Steps (Phase 1)
1. **Source:** Kali Linux (IP: 192.168.x.x) using **Hydra**.
2. **Detection:** Monitored `SecurityEvent` table for **Event ID 4625**.
3. **Analysis:** Identified a spike of 50+ failed logins within 2 minutes.

## 💻 KQL Query Used
```kusto
SecurityEvent
| where EventID == 4625
| summarize count() by IpAddress, TargetUserName
| where count_ > 10
