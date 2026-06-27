# Investigation Report

## Scenario

An employee logged into a Windows workstation.

The SOC team investigated Windows Security Logs to verify authentication events.

---

# Investigation Summary

| Event | Status |
|--------|---------|
| Successful Login | Verified |
| Failed Login | Verified |


---

# Successful Login (Event ID 4624)

### Splunk Query

```spl
index=wineventlog EventCode=4624
```

### Findings

Computer Name:
DESKTOP-5T5E396

Login Status:
Successful

Event ID:
4624

Time:
27 June 2026 15:41:10

Log Source:
Windows Security Log

Result:
User successfully authenticated to the Windows workstation.

---

# Failed Login (Event ID 4625)

### Splunk Query

```spl
index=wineventlog EventCode=4625
```

### Findings

Computer Name:
DESKTOP-5T5E396

Attempted User:
LEO

Logon Type:
2 (Interactive)

Failure Reason:
Unknown username or bad password

Status:
0xC000006D

Sub Status:
0xC000006A

Time:
27 June 2026 16:00:32

Result:
Authentication failed because an incorrect password was entered.

---



# Conclusion

The investigation identified only legitimate Windows authentication events.

No malicious activity or indicators of compromise were found.

This activity represents normal user behavior.