# 🏗️ Detection Architecture

A well-structured detection architecture ensures coverage, scalability, and maintainability.

---

## 🧩 Layers of Detection

| Layer | Description | Example Tools / Data Sources |
|-------|------------|-----------------------------|
| Endpoint | Host-based detection (process, registry, memory) | EDR, Sysmon, OS logs |
| Network | Network traffic and flow-based detection | IDS/NSM, NetFlow, Zeek, packet captures |
| Cloud / SaaS | Cloud platform events and SaaS telemetry | CloudTrail, Office365 logs, GCP/AWS logs |
| Application | Application-specific behavior | Web server logs, API logs, custom telemetry |
| Threat Intelligence | External feeds for IOC correlation | STIX/TAXII feeds, MISP |

---

## 🧠 Principles

1. **Separation of concerns** – keep rules modular per layer.  
2. **Centralized logging** – aggregate telemetry for correlation.  
3. **Coverage mapping** – align each detection to tactics/techniques.  
4. **Reusability** – leverage shared building blocks for multiple rules.  
