\# Windows Event Log Threat Hunting Lab



\## Overview



This project demonstrates how a security analyst can investigate authentication activity using \*\*Windows Security Event Logs\*\*.



Windows logs contain valuable forensic data that helps analysts detect suspicious behavior such as \*\*failed login attempts, brute-force activity, and unauthorized access attempts\*\*.



In this lab environment, multiple failed login attempts were intentionally generated in order to simulate suspicious authentication activity. These events were then analyzed using \*\*Event Viewer\*\* to identify failed and successful logon events.



The objective of this project was to demonstrate how analysts can detect suspicious authentication patterns and extract evidence from Windows security logs.



\---



\## Objectives



• Generate suspicious authentication activity

• Investigate Windows Security logs

• Identify failed login attempts

• Analyze authentication events

• Export logs as forensic evidence

• Document findings like a security analyst



\---



\## Tools Used



• Windows 11 (Virtual Machine)

• Event Viewer

• Windows Security Logs

• VirtualBox



\---



\## Key Event IDs Investigated



| Event ID | Description          |

| -------- | -------------------- |

| 4625     | Failed Logon Attempt |

| 4624     | Successful Logon     |



These events are commonly monitored by \*\*SOC analysts\*\* to detect suspicious login activity.



\---



\## Project Structure



```

windows-event-log-threat-hunting

│

├── README.md

├── screenshots

│   ├── 01-project-folder.png

│   ├── 02-security-log-overview.png

│   ├── 03-failed-logons-4625.png

│   ├── 04-failed-logon-details.png

│   ├── 05-successful-logons-4624.png

│   ├── 06-export-security-log.png

│   └── 07-findings-summary.png

│

├── evidence

│   └── security-log.evtx

│

└── analysis

&#x20;   └── findings.txt

```



\---



\## Step 1 – Project Folder Structure



A structured project directory was created to organize screenshots, evidence files, and analysis documentation.



!\[Project Folder](screenshots/01-project-folder.png)



\---



\## Step 2 – Reviewing Windows Security Logs



Event Viewer was used to inspect authentication activity stored within Windows Security logs.



```

Event Viewer → Windows Logs → Security

```



!\[Security Log Overview](screenshots/02-security-log-overview.png)



\---



\## Step 3 – Identifying Failed Login Attempts



Event Viewer was filtered for \*\*Event ID 4625\*\*, which represents failed authentication attempts.



Multiple failed login attempts were generated to simulate suspicious activity.



!\[Failed Logins](screenshots/03-failed-logons-4625.png)



\---



\## Step 4 – Investigating Event Details



One of the failed login events was opened to inspect the detailed information available within the event log.



Important fields analyzed included:



• Account Name

• Logon Type

• Timestamp

• Event ID



!\[Event Details](screenshots/04-failed-logon-details.png)



\---



\## Step 5 – Identifying Successful Logins



Event Viewer was filtered for \*\*Event ID 4624\*\*, which represents successful authentication events.



This allows analysts to determine whether successful access occurred after multiple failed login attempts.



!\[Successful Logins](screenshots/05-successful-logons-4624.png)



\---



\## Step 6 – Exporting Security Logs as Evidence



The Windows Security log was exported as an \*\*EVTX file\*\* to preserve forensic evidence for further investigation.



!\[Export Security Log](screenshots/06-export-security-log.png)



\---



\## Step 7 – Investigation Findings



The investigation findings were documented to summarize the observed authentication activity.



!\[Findings Summary](screenshots/07-findings-summary.png)



\---



\## Key Findings



• Multiple failed authentication attempts were detected

• Failed login attempts were logged under \*\*Event ID 4625\*\*

• Successful authentication events appeared under \*\*Event ID 4624\*\*

• Windows Event Viewer provides detailed authentication logs useful for detecting suspicious activity



This investigation demonstrates how analysts can detect potential brute-force login activity using Windows security logs.



\---



\## Skills Demonstrated



• Security log analysis

• Threat hunting techniques

• Authentication event investigation

• Evidence collection

• Security documentation



\---



\## Conclusion



Windows Security Event Logs provide critical visibility into authentication activity across systems.



By monitoring failed and successful login events, security analysts can quickly identify suspicious login behavior and respond to potential security incidents.



This project demonstrates a practical approach to investigating authentication activity using Windows Event Viewer in a controlled lab environment.



