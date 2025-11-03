# 📈 Detection Performance Metrics

To manage detections as a **living capability**, performance must be measured, tracked, and improved continuously.

---

## 🧩 1. Key Performance Indicators (KPIs)

| Metric | Description | Target |
|--------|--------------|--------|
| **True Positive Rate (TPR)** | % of detections that identify real malicious activity | > 80% |
| **False Positive Rate (FPR)** | % of detections that generate noise | < 10% |
| **Detection Coverage** | % of ATT&CK techniques covered | > 70% of relevant techniques |
| **Detection Latency** | Average time to trigger alert | < 5 min |
| **Response Time** | Time from alert to analyst triage | < 15 min |
| **Mean Time to Tune (MTTT)** | Avg. time to correct or refine a detection | < 7 days |

---

## 📊 2. Program Maturity Metrics

| Category | Metric | Goal |
|-----------|--------|------|
| **Quality** | # of rules with validation status “Tested” | 100% |
| **Coverage** | # of tactics covered in ATT&CK matrix | ≥ 10 |
| **Velocity** | # of new detections per month | ≥ 5 |
| **Sustainability** | % of rules reviewed per quarter | ≥ 25% |
| **Collaboration** | # of feedback inputs from SOC | Continuous |

---

## 🧠 3. Dashboards & Visualization

Recommended dashboards:
- **Detection Efficacy Dashboard** (TPR/FPR over time)
- **Coverage Heatmap** (ATT&CK Tactics & Techniques)
- **Alert Trends** (volume, distribution, sources)
- **Operational Efficiency** (time to triage, tuning cycles)

Tools:
- Grafana / Kibana for operational data  
- Power BI / Tableau for strategic reporting  
- ATT&CK Navigator for coverage visualization  

---

## 📚 References
- MITRE ATT&CK – *Detection Metrics Framework*  
- SANS – *KPIs for SOC and Detection Engineering*  
- Palantir – *Detection Health and Maturity Tracking*
