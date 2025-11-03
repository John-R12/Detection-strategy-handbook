# 🎛️ Detection Monitoring & Tuning

Once deployed, detections require **continuous monitoring and tuning** to stay effective, reduce noise, and maintain analyst trust.

---

## 🧩 1. Why Monitoring Matters

Detection logic degrades over time due to:
- **Changes in attacker behavior**
- **New log formats or data gaps**
- **Environmental drift**
- **SOC desensitization** from alert fatigue

> Continuous tuning ensures **high signal-to-noise ratio** and operational relevance.

---

## ⚙️ 2. Detection Health Metrics

| Metric | Description | Goal |
|---------|--------------|------|
| **Alert Volume** | Number of alerts generated | Stable, proportional to baseline |
| **False Positive Rate** | Ratio of benign alerts | As low as possible |
| **True Positive Rate** | Ratio of valid alerts | Maximize without noise |
| **Detection Latency** | Time between event and alert | < 5 min (depending on platform) |
| **Staleness** | Time since last validation | < 90 days |

---

## 🧠 3. Tuning Workflow

1. **Collect Feedback** – from SOC analysts, hunts, or IR investigations  
2. **Analyze Patterns** – recurring false positives, missed detections  
3. **Refine Logic** – narrow conditions, add filters, improve context  
4. **Revalidate** – test updated rule before redeployment  
5. **Document** – version notes, tuning rationale, validation results  

---

## 🧩 4. Common Tuning Techniques

| Technique | Description |
|------------|--------------|
| **Contextual Filtering** | Include only relevant hosts, users, or processes |
| **Baseline Learning** | Establish normal activity profiles |
| **Threshold Adjustment** | Modify alerting thresholds dynamically |
| **Correlation with Other Signals** | Combine multiple weak indicators |
| **Suppression Windows** | Avoid duplicate alerts during known maintenance |

---

## 📊 5. Alert Review Cadence

| Rule Criticality | Review Frequency |
|-------------------|------------------|
| High | Weekly |
| Medium | Monthly |
| Low | Quarterly |
| Deprecated | As needed |

---

## 📚 References
- Red Canary – *Maintaining Detection Health*  
- Palantir – *Detection Tuning Framework*  
- SANS – *Operationalizing Detection Engineering*
