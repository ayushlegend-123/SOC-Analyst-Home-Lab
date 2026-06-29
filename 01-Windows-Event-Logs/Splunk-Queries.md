# Splunk query language :
To see successful logins: `index=main  EventCode=4624`
To see failed logins: `index=main EventCode=4625`
Dashboard command :

Successful Login Count: 'index=wineventlog EventCode=4624 | stats count AS "Successful Logins"'

Failed Login Count: 'index=wineventlog EventCode=4625 | stats count AS "Failed Logins"'

Authentication Timeline : 'index=wineventlog (EventCode=4624 OR EventCode=4625)
| timechart count by EventCode'

Event Distribution: 'index=wineventlog (EventCode=4624 OR EventCode=4625)
| stats count by EventCode'

Failed Login by User: 'index=wineventlog EventCode=4625 | stats count by Account_Name'

Successful Login by User: 'index=wineventlog EventCode=4624 | stats count by Account_Name'

Recent Authentication Events: 'index=wineventlog (EventCode=4624 OR EventCode=4625) | table _time EventCode Account_Name ComputerName Message | sort - _time'