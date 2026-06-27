# Splunk query language :
To see successful logins: `index=main  EventCode=4624`
To see failed logins: `index=main EventCode=4625`
Dashboard command :

Successful Login Count: 'index=wineventlog EventCode=4624 | stats count AS "Successful Logins"'

Failed Login Count: 'index=wineventlog EventCode=4625 | stats count AS "Failed Logins"'

