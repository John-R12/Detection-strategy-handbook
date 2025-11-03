# 🗂️ Detection Matrix

The **Detection Matrix** visualizes your detection portfolio against MITRE ATT&CK coverage.

---

## 🧩 Example Layout

| Detection | Tactic | Technique | Coverage (Yes/Partial/No) | Priority |
|-----------|--------|-----------|---------------------------|---------|
| PowerShell Execution | Execution | T1059.001 | Yes | High |
| Phishing Credential Harvest | Initial Access | T1566 | Partial | High |
| Lateral Movement via SMB | Lateral Movement | T1021.002 | No | Medium |
| C2 via HTTP | Command & Control | T1071.001 | Yes | High |

---

## 🧠 Tips

- Update matrix after each new detection deployment.  
- Highlight **coverage gaps** for planning roadmap actions.  
- Color-code or score by **priority** for visual clarity.
