# 🚦 Detection Prioritization Framework

Not all detections are equally important.  
A prioritization framework ensures resources are focused on the **most relevant and impactful** detection opportunities.

---

## 🧩 1. Prioritization Dimensions

| Dimension | Description | Example Metric |
|------------|--------------|----------------|
| **Threat Relevance** | Is the technique used by adversaries targeting your sector? | Intel correlation |
| **Business Impact** | Would exploitation cause material risk to assets? | Risk matrix |
| **Detection Feasibility** | Is sufficient telemetry available? | Data coverage score |
| **False Positive Risk** | How likely is this detection to be noisy? | Validation test result |
| **Response Readiness** | Can the SOC respond effectively if triggered? | Playbook availability |

---

## ⚙️ 2. Scoring Model

| Factor | Weight | Example Score (1–5) | Weighted |
|--------|---------|----------------------|-----------|
| Threat Relevance | 30% | 5 | 1.5 |
| Business Impact | 25% | 4 | 1.0 |
| Detection Feasibility | 20% | 3 | 0.6 |
| False Positive Risk | 15% | 2 | 0.3 |
| Response Readiness | 10% | 4 | 0.4 |
| **Total** | 100% |  | **3.8 / 5** |

> You can adapt this model to your organization’s priorities — e.g., focusing on impact or feasibility.

---

## 📊 3. Prioritization Workflow

1. **Collect candidates** from hypothesis, threat intel, and incidents  
2. **Score** each candidate across the dimensions  
3. **Rank** detections by total weighted score  
4. **Select** top opportunities for design/implementation  
5. **Review quarterly** as threats and telemetry evolve  

---

## 📈 4. Visualization Example

Use a **2D matrix** for quick decision-making:

- **X-axis:** Threat Relevance  
- **Y-axis:** Detection Feasibility  
- **Color:** Business Impact  

🟢 *Top-right = high value*  
🔴 *Bottom-left = low priority*

---

## 📚 References
- Palantir — *Detection Opportunity Prioritization Framework*  
- MITRE ATT&CK — *Threat Technique Relevance Mapping*  
- SANS — *Risk-based Detection Planning*
