# PowerShell Attack Investigation (Ubuntu + Splunk)

## Scenario
A suspicious PowerShell command was detected in simulated Windows logs.  
This lab demonstrates detecting encoded PowerShell commands using Splunk on Ubuntu.

## Tools
- Splunk Enterprise (Ubuntu)
- Simulated Windows PowerShell logs

## Detection Queries
- Search all events: `index=main`
- Detect PowerShell process creation: `index=main EventCode=4688`
- Detect encoded commands: `index=main "*-enc*"`

## Findings
- Event detected where `powershell.exe` was executed by `Administrator`.
- Encoded command detected:  
