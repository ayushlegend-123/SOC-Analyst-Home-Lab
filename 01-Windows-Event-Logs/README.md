# Windows Log Investigation (Practical 1)

## Project Overview

This project demonstrates how to investigate Windows Security Logs using Splunk.

The objective is to identify common Windows authentication events and understand how a SOC analyst investigates user activities.

---

## Lab Environment

- Windows 11
- Splunk Enterprise
- Splunk Universal Forwarder
- Windows Security Logs
- Sysmon (Optional)

---

## Objective

Investigate the following Windows events:

- Successful Login
- Failed Login


---

## Windows Event IDs

| Event | Event ID |
|--------|---------:|
| Login | 4624 |
| Failed Login | 4625 |


---

## Splunk Index

```
index=wineventlog
```

---

## SOC Investigation Questions

- Who logged in?
- When did the login occur?
- Was the login successful?
- Was there a failed login attempt?
- Which user failed authentication?
- Was the workstation locked?
- Was the workstation unlocked?
- Was the system restarted?

---

## MITRE ATT&CK

Not Applicable

This project contains only normal Windows user activities.

---

## Skills Learned

- Windows Event Log Analysis
- Splunk SPL
- Windows Authentication Investigation
- Windows Security Event IDs
- SOC Investigation Workflow
- Log Analysis
- Security Monitoring

---

## Screenshots

Screenshots of each investigation are available in the **Screenshots** folder.
