# 🎯 Detection Use Cases

Detection Use Cases (DUCs) translate **business and threat context** into actionable detection objectives.  
They connect *why* we detect something (risk, threat) with *how* we implement it (telemetry, logic).

---

## 🧩 1. What is a Detection Use Case?

A **Detection Use Case** defines:
- The **threat scenario or behavior** being detected.  
- The **adversary tactics and techniques** involved.  
- The **data sources** and **detection logic** needed.  
- The **response expectations** and **success criteria**.

It acts as a blueprint between strategy and implementation.

---

## 🧠 2. Detection Use Case Template

| Field | Description | Example |
|--------|--------------|----------|
| **Name** | Short descriptive title | “Credential Dumping via LSASS Access” |
| **Objective** | What is the detection meant to identify or prevent? | Detect attempts to read LSASS process memory |
| **Threat Context** | Why this matters to your org (threats, assets, business impact) | Common post-exploitation tactic in ransomware attacks |
| **MITRE ATT&CK** | Mapped tactics/techniques | TA0006 – Credential Access / T1003.001 |
| **Data Sources** | Relevant telemetry | EDR process creation logs, Sysmon, memory access events |
| **Detection Logic** | Rule, query, or heuristic description | Detect `mimikatz.exe` or suspicious `ReadProcessMemory` on LSASS |
| **Severity / Priority** | Risk-based score | High |
| **Validation Method** | How the detection is tested | Atomic Red Team simulation |
| **Response Guidance** | What to do when triggered | Isolate host, dump memory for forensics |

---

## ⚙️ 3. Detection Use Case Lifecycle

1. **Ideate** from Threat Intel, Hunting, or Incident findings  
2. **Design** using ATT&CK and telemetry analysis  
3. **Implement** in your detection platform (SIEM, EDR, XDR, etc.)  
4. **Validate** using adversary emulation or test data  
5. **Evaluate** impact, performance, and detection coverage  

---

## 📈 4. Categorizing Detection Use Cases

| Category | Examples |
|-----------|-----------|
| **Initial Access** | Phishing attachments, exploit delivery |
| **Execution** | PowerShell abuse, LOLBins, script interpreters |
| **Persistence** | Registry autoruns, scheduled tasks |
| **Privilege Escalation** | Token manipulation, UAC bypass |
| **Defense Evasion** | Disabling AV, tampering with logs |
| **Credential Access** | LSASS dump, SAM extraction |
| **Exfiltration** | Data transfer via cloud or FTP |

---

## 📚 References
- MITRE ATT&CK – *Use Case Mapping Guide*  
- SANS – *Detection Use Case Framework*  
- Palantir – *Detection Maturity Model (DMF)*  
