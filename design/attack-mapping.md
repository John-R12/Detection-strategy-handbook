# 🗺️ ATT&CK Mapping and Coverage

Mapping detections to the **MITRE ATT&CK framework** allows organizations to visualize coverage, identify gaps, and prioritize future development.

---

## 🧩 1. Why ATT&CK Mapping Matters

- Creates a **shared vocabulary** across detection, response, and intel teams.  
- Enables **coverage analysis** of tactics and techniques.  
- Supports **maturity assessment** and roadmap planning.  
- Enhances communication with leadership and auditors.

---

## 📊 2. Mapping Framework

Each detection should be tagged with:
- **Tactic ID and Name** (e.g., TA0005 – Defense Evasion)  
- **Technique ID and Name** (e.g., T1036 – Masquerading)  
- **Sub-technique** if applicable (e.g., T1036.003 – Rename System Utilities)  
- **Data Source(s)** from [ATT&CK Data Sources](https://attack.mitre.org/datasources/)  
- **Confidence Level** (Low, Medium, High)

---

## 📈 3. Example Detection Mapping

| Detection Name | ATT&CK Technique | Data Source | Confidence | Coverage |
|----------------|------------------|--------------|-------------|-----------|
| PowerShell Execution with Encoded Commands | T1059.001 | Script execution logs | High | ✅ |
| Suspicious Service Creation | T1543.003 | Windows event logs | Medium | ✅ |
| Unusual Beaconing Pattern | T1071.001 | Proxy/network logs | Medium | ⚠️ Partial |

---

## 🧠 4. Coverage Visualization

You can visualize ATT&CK coverage using tools like:
- [ATT&CK Navigator](https://mitre-attack.github.io/attack-navigator/)
- OpenCTI Coverage Matrices
- Jupyter or Python notebooks (matrix heatmaps)
- Custom dashboards (e.g., Grafana, Power BI)

> Export your detection metadata (TID, name, owner, coverage status) to JSON or CSV for automated visualization.

---

## 🧩 5. Coverage Metrics

| Metric | Description |
|--------|--------------|
| **Technique Coverage (%)** | % of relevant ATT&CK techniques with at least one detection |
| **Tactic Coverage Depth** | Average number of detections per tactic |
| **Detection Confidence Distribution** | Ratio of high vs. medium vs. low confidence detections |
| **Change Over Time** | Trends in coverage increase or decrease per quarter |

---

## 📚 References
- MITRE ATT&CK Navigator  
- MITRE Engenuity – *ATT&CK Evaluations*  
- Palantir – *Detection Coverage Framework*
