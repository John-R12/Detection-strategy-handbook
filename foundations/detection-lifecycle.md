# 🔄 Detection Lifecycle

The **Detection Lifecycle** describes how an organization ideates, develops, tests, deploys, and maintains security detections.  
It ensures that detections evolve with adversary behavior, infrastructure changes, and business priorities.

---

## 🧩 1. Phases of the Detection Lifecycle

| Phase | Description | Example Output |
|-------|--------------|----------------|
| **1. Ideation / Hypothesis** | Define detection ideas based on threat intel, incidents, or hunt results. | Detection hypothesis document |
| **2. Design** | Map hypothesis to ATT&CK TTPs, define logic, required data sources, and success criteria. | Detection specification |
| **3. Implementation** | Develop rule/query in SIEM, EDR, or other detection systems. | Detection rule (YAML/Sigma/KQL/etc.) |
| **4. Validation** | Test logic using simulated or historical data; measure accuracy and coverage. | Validation report |
| **5. Deployment** | Deploy in production with alert routing, documentation, and version control. | Live detection alert |
| **6. Evaluation & Tuning** | Measure detections’ performance, adjust thresholds, and update logic. | Detection performance metrics |
| **7. Retirement / Replacement** | Decommission outdated or redundant detections and replace as needed. | Archived detection record |

---

## 🧠 2. Inputs and Outputs

| Inputs | Outputs |
|--------|----------|
| Threat Intelligence reports | New detection hypotheses |
| Incident reports | Post-incident detection improvements |
| Hunting findings | Detection logic and enrichment |
| Red/Purple Team results | Gaps and tuning opportunities |
| Engineering changes | Updated data source coverage |

---

## ⚙️ 3. Detection Lifecycle Integration

Detection engineering should integrate tightly with:
- **Threat Intelligence** (for prioritization and relevance)
- **Threat Hunting** (for new detection ideas)
- **Incident Response** (for lessons learned)
- **Purple Teaming** (for validation and simulation)
- **DevSecOps** (for telemetry reliability and automation)

---

## 📈 4. Key Metrics by Lifecycle Phase

| Phase | Example Metrics |
|--------|----------------|
| Ideation | % detections mapped to high-priority threats |
| Implementation | Mean time to deployment (MTTD) |
| Validation | False positive rate, true positive rate |
| Evaluation | Detection coverage vs. MITRE ATT&CK matrix |
| Retirement | % outdated detections removed quarterly |

---

## 🧰 5. Tooling and Automation

- **Version control:** Git / GitHub for rule management.  
- **CI/CD pipelines:** automated syntax validation, test runs, deployment.  
- **Simulation frameworks:** Atomic Red Team, CALDERA, Prelude Operator.  
- **Metrics dashboards:** Kibana, Grafana, Looker.  

---

## 📚 References
- Palantir — *Detection Maturity Framework (DMF)*  
- MITRE ATT&CK — *Adversary tactics & techniques*  
- Google Cloud — *Detection as Code Model*  
- SANS — *Detection Engineering Lifecycle*
