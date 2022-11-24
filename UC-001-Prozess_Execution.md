# Case:  UC-001 – Process execution with command-line arguments

## Generelle Informationen 
Beschreibung 

Adversaries may abuse command and script interpreters to execute commands, scripts, or binaries. These interfaces and languages provide ways of interacting with computer systems and are a common feature across many different platforms. Most systems come with some built-in command-line interface and scripting capabilities, for example, macOS and Linux distributions include some flavor of Unix Shell while Windows installations include the Windows Command Shell and PowerShell.

Mitre Ref: https://attack.mitre.org/techniques/T1059/


## Use Case Documentaion

- Link to ..
- Elastic Rules ..

### Beispiel

- Dashboard
- Typical Allert
- Drilldown, deep dive


## Vorbereitungen, Bemerkungen

### Vorgaben und Prozesse 
- ISMS Datenklassifizierung
- Sec Incident Prozess

### Assets

- Known Systems, 
- Assets - ISMS inventory
- Datenschutz Verzeichnis)
- Netbox ?


### Known Customer Obligations

| Customer   |      UC Variation      |  Comments | SLA | Contract |
|----------|:-------------:|------:|-----:|-----:|
|SVV| Falco Alert 003| Check mit AM | 24h| [Betriebsvertrag SVV](Betriebsvertrag-svv.md)|


### Kontakte (ev. aus Netbox)

John.doe@nowhere.net

## Identifikation 

### Erkennung 

| ID   |      Data Source      |  Data Component | Detects |
|----------|:-------------:|------:|-----:|
| DS0017 |  Command| Command Execution | Monitor command-line arguments for script execution and subsequent behavior. Actions may be related to network and system information Discovery, Collection, or other scriptable post-compromise behaviors and could be used as indicators of detection leading back to the source script. Scripts are likely to perform actions with various effects on a system that may generate events, depending on the types of monitoring used.|
|DS0011	|Module	|Module Load|Monitor for events associated with scripting execution, such as the loading of modules associated with scripting languages (ex: JScript.dll or vbscript.dll).|
|DS0009	|Process	|Process Creation|Monitor log files for process execution through command-line and scripting activities. This information can be useful in gaining additional insight to adversaries' actions through how they use native processes or custom tools. Also monitor for loading of modules associated with specific languages.|
| | |Process Metadata||Monitor contextual data about a running process, which may include information such as environment variables, image name, user/owner, or other information that may reveal abuse of system features. For example, consider monitoring for Windows Event ID (EID) 400, which shows the version of PowerShell executing in the EngineVersion field (which may also be relevant to detecting a potential Downgrade Attack) as well as if PowerShell is running locally or remotely in the HostName field. Furthermore, EID 400 may indicate the start time and EID 403 indicates the end time of a PowerShell session.[48]|
|DS0012	|Script	|Script Execution|Monitor for any attempts to enable scripts running on a system would be considered suspicious. If scripts are not commonly used on a system, but enabled, scripts running out of cycle from patching or other administrator functions are suspicious. Scripts should be captured from the file system when possible to determine their actions and intent.|


Einen nicht erlaubten Datenabfluss zu erkennen ist ....
Valiedierung 
Die Validierung des Vorfalls kann über folgende Datenquellen im SIEM allenfalls Validiert werden: 
      
### Datenquelle 

| Source   |      Systems      |  Data  |
|----------|:-------------:|------:|
|Primary Source	|Windows	|Winlogbeat collecting Events from the Windows Sysmon Service.|
|               |Linux	    |Filebeat collecting information from the Syslog Service|
|Secondary Sources|	AD      |Logs	Correlation of User Accounts to Process Execution on Windows|
|         |	Free IPA Logs	|Correlation of User Accounts to Process Execution on Windows|
| |	Network Connections	|Network Events from Packetbeat Agents. Can be used to track back connections to process execution to find the original Source|

### Analysys

- Check originated prozesse
- Track down source or Source IP of preozess initiation
- [Check Source IP for known bad IP Reputation](IP-Reputation-check.md)
- Check against MISP Sources -> MISP Dashboard



# Triage

### False Positiv

- Kriterien

### Minor Incident

- Kriterien

	Indikation

### Mayor Incident

- Kriterien

	Eskalation

		CSIRT



# Remediation 

- Shut down prozess
- Blacklist origin
- Discover impact on data and systems
.....
