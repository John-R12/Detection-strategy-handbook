# 📊 Data Modeling for Detection

Structured telemetry ensures that detections are reliable, consistent, and testable.

---

## 🧩 Standard Fields

| Field | Description |
|-------|-------------|
| timestamp | Event timestamp in ISO 8601 |
| source.ip | Source IP of activity |
| dest.ip | Destination IP |
| user.name | Username or account identifier |
| host.name | Hostname or asset identifier |
| process.name | Executed process or binary |
| file.hash | SHA256 hash of files |
| url | Full URL if applicable |
| action | Observed action (create, delete, connect, etc.) |

---

## 🧠 Best Practices

- Normalize all log sources to the same field names.  
- Include **context enrichment**: asset tags, geolocation, threat score.  
- Timestamp conversion to UTC.  
- Maintain versioned schemas for auditability.  
- Use structured formats (JSON, ECS, CEF) for ingestion consistency.
