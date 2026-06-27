# Attack (Simulation) Steps

This lab simulates common Windows user authentication activities to generate Windows Security Event Logs for analysis in Splunk.

## Step 1 - Successful Login

- Locked the Windows workstation.
- Logged in using the correct password.
- Verified Event ID 4624 in Splunk.

Expected Event:
4624 - Successful Logon

---

## Step 2 - Failed Login

- Locked the workstation.
- Entered an incorrect password.
- Repeated the incorrect password two times.
- Verified Event ID 4625.

Expected Event:
4625 - Failed Logon

---

