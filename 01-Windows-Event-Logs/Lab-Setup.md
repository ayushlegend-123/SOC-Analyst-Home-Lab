# Lab Setup

## Environment

| Component | Details |
|------------|---------|
| Operating System | Windows 11 |
| SIEM | Splunk Enterprise |
| Log Forwarder | Splunk Universal Forwarder |
| Log Source | Windows Security Logs |
| Optional | Sysmon |

---

## Log Sources

- Windows Security
- Windows System
- Sysmon Operational

---

## Splunk Index

```
index=wineventlog
```

---

## Data Collection

The Splunk Universal Forwarder was configured to collect the following logs:

- Security
- System
- Microsoft-Windows-Sysmon/Operational

These logs were forwarded to the Splunk Enterprise server for investigation.

---

## Objective

Generate Windows authentication events and investigate them using Splunk.

The following Event IDs were analyzed:

- 4624
- 4625
