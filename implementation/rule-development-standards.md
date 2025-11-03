# 🧱 Rule Development Standards

Standardizing rule development ensures **consistency**, **maintainability**, and **scalability** across your detection portfolio.

---

## 🧩 1. Rule Development Lifecycle

| Phase | Description |
|--------|--------------|
| **Define** | Identify detection objective and ATT&CK mapping |
| **Design** | Specify data sources and logic approach |
| **Implement** | Write detection in platform-specific syntax |
| **Validate** | Test rule accuracy and performance |
| **Deploy** | Push rule to production with version control |
| **Review** | Evaluate FP/FN rate and operational relevance |

---

## 🧠 2. Rule Naming Convention

| Type | Example |
|------|----------|
| **Tactic-based** | `TA0005_DefenseEvasion_Suspicious_Script_Execution` |
| **Behavior-based** | `CredentialDumping_LSASS_ReadProcessMemory` |
| **Source-based** | `Sysmon_Suspicious_Service_Creation` |

> Use consistent naming for searchability, automation, and ATT&CK alignment.

---

## ⚙️ 3. Rule Structure Example (YAML)

```yaml
title: LSASS Memory Access
id: DUC-2025-001
status: active
author: Threat Detection Team
date_created: 2025-01-03
description: Detects processes accessing LSASS memory for credential dumping
references:
  - https://attack.mitre.org/techniques/T1003.001/
logsource:
  category: process_access
  product: windows
detection:
  selection:
    TargetImage|endswith: 'lsass.exe'
    GrantedAccess: '0x1fffff'
  condition: selection
falsepositives:
  - legitimate EDR or AV access
level: high
```


## 📊 4. Rule Quality Criteria
| Category	| Description |
|-----------|-------------|
| Clarity |	Logic and purpose are clearly explained |
| Efficiency |	Minimal performance impact |
| Specificity |	Targets malicious behavior, not noise |
| Validation |	Tested against both benign and malicious data |
| Documentation |	Metadata and mapping complete |

📚 References
- Sigma HQ – Rule Development Guidelines
- SANS — Detection Rule Engineering and QA
- Elastic — SIEM Rule Writing Best Practices
