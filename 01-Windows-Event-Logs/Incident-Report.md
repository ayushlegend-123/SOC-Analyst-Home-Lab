# Incident Report

## Incident Summary

A Windows workstation authentication investigation was performed using Splunk Security Logs.

The purpose of the investigation was to verify normal Windows authentication events and ensure no suspicious activity occurred.

---

## Incident Details

| Field | Value |
|--------|-------|
| Incident ID | WIN-001 |
| Severity | Informational |
| Status | Closed |
| Category | Windows Authentication |
| Data Source | Windows Security Logs |
| SIEM | Splunk |

---

## Timeline

| Time | Event |
|------|-------|
| 15:41:10 | Successful Login (4624) |
| 16:00:32 | Failed Login (4625) |

---

## Investigation

### Successful Login

Event ID:
4624

Status:
Successful Authentication

Result:
The user successfully authenticated to the Windows workstation.

---

### Failed Login

Event ID:
4625

Observed User:
LEO

Computer:
DESKTOP-5T5E396

Failure Reason:
Unknown user name or bad password.

Status Code:
0xC000006D

Sub Status:
0xC000006A (Incorrect Password)

Result:
The authentication failed because an incorrect password was entered.

---

## Indicators of Compromise (IOC)

No Indicators of Compromise were identified.

No suspicious IP addresses.

No privilege escalation.

No lateral movement.

No malware execution.

---

## Root Cause

The failed authentication event was caused by an incorrect password entered during an interactive login attempt.

This activity was intentionally generated for lab testing.

---

## Impact

No impact on system availability.

No data loss.

No unauthorized access.

No security breach.

---

## MITRE ATT&CK

Not Applicable

The observed events represent legitimate Windows authentication activities performed in a controlled lab environment.

---

## Conclusion

The investigation confirmed that all observed events were expected and generated during normal user activity for testing purposes.

The failed login was caused by an intentionally incorrect password and does not indicate malicious activity.

Incident Status:
Closed