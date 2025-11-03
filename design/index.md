# 🧩 Detection Design Overview

The **Detection Design** folder provides a structured approach to building high-quality, threat-aligned detections.  
It bridges the gap between strategic intent (`strategy/`) and operational implementation (`operations/`).

---

## 📊 Components

| File | Purpose |
|------|---------|
| `attack-mapping.md` | Map each detection to MITRE ATT&CK techniques and tactics. |
| `detection-use-cases.md` | Define concrete detection scenarios based on threat intelligence. |
| `hypothesis-development.md` | Develop testable detection hypotheses for validation. |
| `prioritization-framework.md` | Rank detections by threat relevance, feasibility, and business impact. |
| `detection-architecture.md` | Logical architecture of detection coverage (endpoint, network, cloud). |
| `data-modeling.md` | Standardize telemetry and log normalization for reliable detection. |
| `detection-matrix.md` | Visualize coverage and gaps across ATT&CK tactics and techniques. |
| `detection-playbooks.md` | Link detections to analyst and automated SOC/IR workflows. |
| `sigma-guidelines.md` | Metadata, naming conventions, and YAML structure for Sigma rules. |

---

## 🧩 How to Use

1. Start with **`attack-mapping.md`** to align detections with known adversary behaviors.  
2. Use **`detection-use-cases.md`** and **`hypothesis-development.md`** to define actionable scenarios.  
3. Apply **`prioritization-framework.md`** to focus on high-value detections first.  
4. Build the **architecture** in `detection-architecture.md` and normalize logs in `data-modeling.md`.  
5. Maintain a **detection matrix** to track coverage and gaps.  
6. Link rules to **SOC/IR playbooks** for actionable responses.  
7. Follow **`sigma-guidelines.md`** for consistent, reusable detection implementation.
