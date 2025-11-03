# 🧮 Detection Prioritization Model

With limited time and resources, SOCs must **prioritize detections** based on impact, likelihood, and operational feasibility.  
This model provides a structured scoring approach for ranking detection opportunities.

---

## 🧩 Core Criteria

| Criterion | Description | Weight |
|------------|--------------|--------|
| **Threat Relevance** | How closely the behavior aligns with active adversaries. | 30% |
| **Business Impact** | Potential damage if undetected. | 25% |
| **Detectability** | Availability and reliability of telemetry sources. | 20% |
| **Complexity** | Effort required to implement and maintain. | 15% |
| **Coverage Gap** | Whether the behavior is already detected. | 10% |

---

## 🧠 Example Scoring

| Detection Candidate | Threat Relevance | Business Impact | Detectability | Complexity | Coverage Gap | **Total Score** |
|----------------------|------------------|-----------------|----------------|-------------|---------------|----------------|
| Credential Dumping (LSASS) | 5 | 5 | 4 | 3 | 4 | **4.4 / 5** |
| Command-Line Obfuscation | 4 | 3 | 5 | 2 | 5 | **3.9 / 5** |
| Lateral Movement via SMB | 3 | 4 | 3 | 4 | 2 | **3.3 / 5** |

> Focus first on high-scoring detections that are feasible and threat-relevant.

---

## 🧰 Best Practices
- Re-evaluate priorities quarterly or after major incidents.  
- Involve CTI, SOC, and Red Team in scoring workshops.  
- Document assumptions and confidence levels.  
- Use a weighted scoring spreadsheet or automation script to standardize decisions.
