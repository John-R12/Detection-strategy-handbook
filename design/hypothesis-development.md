# 🧠 Hypothesis Development

Detection begins with a **hypothesis** — a reasoned assumption about adversary behavior that can be tested through data.

---

## 🎯 1. What is a Detection Hypothesis?

A **Detection Hypothesis** expresses an idea that:
- Can be **observed** through available telemetry,  
- Can be **tested** with real data or simulation, and  
- Has **value** in detecting or preventing real threats.

> Example: “If an attacker performs credential dumping, then we will observe access to LSASS memory from a non-system process.”

---

## 🧩 2. Hypothesis Template

| Field | Description | Example |
|--------|--------------|----------|
| **Hypothesis** | Behavior to test | Adversaries may use `reg save HKLM\SAM` to dump credentials |
| **Associated Technique** | MITRE ATT&CK reference | T1003.002 – Security Account Manager |
| **Data Requirements** | Needed telemetry | Process creation logs, command-line arguments |
| **Assumptions** | What must be true for this to occur | System allows registry export with admin privileges |
| **Validation Approach** | How to test | Simulate with Atomic Red Team |
| **Expected Output** | Observable artifacts | `reg.exe` process with `save` and `HKLM\SAM` arguments |
| **Detection Idea** | How to detect | Query for those command-line patterns |

---

## 🔁 3. Hypothesis Lifecycle

1. **Define** — articulate a clear, testable statement.  
2. **Validate** — collect evidence, simulate behavior.  
3. **Convert** — translate validated hypotheses into detections.  
4. **Measure** — evaluate detection accuracy and coverage.  
5. **Iterate** — refine or discard based on findings.

---

## 📊 4. Sources for Hypothesis Generation

| Source | Example |
|--------|----------|
| Threat Intelligence | Reports on new ransomware TTPs |
| Incident Reports | Missed detections from real intrusions |
| Threat Hunting | Observed anomalies during hunts |
| Purple Team | Gaps identified during ATT&CK emulations |
| Security Research | Exploit or malware analysis findings |

---

## 📚 References
- MITRE ATT&CK – *Detection Hypothesis Framework*  
- Red Canary – *Threat Detection Hypothesis Examples*  
- SANS – *Hypothesis-Driven Threat Hunting*
