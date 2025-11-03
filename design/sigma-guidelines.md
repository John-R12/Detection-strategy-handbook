# 📝 Sigma Guidelines

Use Sigma rules to standardize detection logic across multiple platforms.

---

## 🧩 Recommended Fields

| Field | Purpose |
|-------|---------|
| title | Human-readable detection name |
| id | Unique identifier (UUID recommended) |
| description | Context and purpose |
| status | experimental / stable / deprecated |
| author | Owner or author |
| references | MITRE ATT&CK, CVEs, advisories |
| logsource | Platform or product for detection |
| detection | Actual detection logic (conditions) |
| level | Severity: low / medium / high |
| tags | Keywords: tactic, technique, business relevance |

---

## 🧠 Best Practices

- Version control all rules.  
- Use consistent naming conventions (`Layer-DetectionName-Tactic`).  
- Include ATT&CK mappings in `tags`.  
- Test in staging before production deployment.  
- Review periodically for tuning and relevance.
