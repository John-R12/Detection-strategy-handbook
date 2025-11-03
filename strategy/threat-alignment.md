# 🎯 Threat Alignment

Detection strategy must reflect **real adversary behavior** — not arbitrary log events.  
This file outlines how to align detection coverage with **threat intelligence** and **MITRE ATT&CK**.

---

## 🧩 Key Steps

1. **Identify Threat Actors or Campaigns**  
   - Use CTI inputs to list priority threat groups (e.g., APT29, FIN7).  
   - Review their typical TTPs and target sectors.  

2. **Map to MITRE ATT&CK**  
   - Align observed or probable TTPs to ATT&CK techniques.  
   - Note relevant data sources and platforms (Windows, Linux, Cloud, etc.).  

3. **Define Detection Objectives**  
   - What behavior or signal do we want to observe?  
   - What log sources or telemetry are required?  

4. **Validate with Red Team or Purple Team Exercises**  
   - Test detection logic against simulated attacker activity.  
   - Use feedback to improve fidelity and reduce false positives.

---

## 📊 Example Mapping

| Threat Actor | ATT&CK Technique | Detection Focus | Data Source |
|---------------|-----------------|-----------------|--------------|
| APT29 | T1059.001 – PowerShell | Script execution monitoring | Sysmon, EDR |
| FIN7 | T1071.001 – Web Protocols | Suspicious HTTP C2 patterns | Proxy logs |
| Scattered Spider | T1566 – Phishing | Abnormal login post-phishing | Email + Auth logs |

> Threat-driven alignment ensures detections address real-world risks — not hypothetical ones.
