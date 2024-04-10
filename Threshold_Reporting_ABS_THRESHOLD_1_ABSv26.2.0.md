# Case:  UC-001 – Threshold AZCH ABS THRESHOLD 1 ABS 

## Generelle Informationen 
Beschreibung 

In the attachment you will find the generated report of today. In this report you will see which users opened at least 30 records (Akten) within an hour in ABS. 



Mitre Ref: Data Exfiltration https://attack.mitre.org/tactics/TA0010/


## Use Case Documentaion

- Link to ..
- SIEM Rules ..

### Beispiel

- Dashboard
- Typical Allert  (Reported as Excel File)

ABSUSERID	STARTZEITPUNKT	ENDZEITPUNKT	ANZAHL_GEOEFFNETE_AKTEN
C8021xxx	2024-04-09-16	2024-04-09-16	256
S8026xxx	2024-04-09-13	2024-04-09-13	92
C8021xxx	2024-04-09-17	2024-04-09-17	88
S8017xxx	2024-04-09-07	2024-04-09-07	86
S8036xxx	2024-04-09-16	2024-04-09-16	79

- Drilldown, deep dive

### Vorgaben und Prozesse 
- AFRIS / ISP
- Datenklassifizierung  / PIA -> Callification -> Notification Rules
- Sec Incident Prozess

### Assets

- Service Provider
- Environment (E1)
- Application ABS
    ADOIT-ID
    Archer ID
- Datenschutz Verzeichnis (ID ?)

### Notification / Escalation Rules

- FINMA Reporting required
    - Notification Instructions
- GDPR / Datenschutz Report 
    - Notification Instructions


### Kontakte 

Business Owner - John.doe@nowhere.net
Application O=wner - 
Service Manager -
IT Security
CISO
DPO

## Identifikation - False Positive Stage 1

Anzahl Akten Zugriffe > Threshold -> Indicates Data Exfiltration
Compare historic Data

### Erkennung 

Far bejond Threshold
.....
      
### Datenquelle 

ABS Logs

### Analysys - Stage 2

Anzahl Akten Zugriffe > Threshold -> Indicates Data Exfiltration
Check USER -> Special ABS User (Technical  User, Massendaten, Call-Center, Help Desk, Admoin=
Check User Orga -> Required for Work
Compare historic Data
Check with Line Manager

- Additional -> Check Client ID
- Check Source IP
- Check Timestamp
....

### Minor Incident

- Kriterien

	Singel Occurence

### Mayor Incident

- Kriterien

	Multiple Occurences
    No regular ABS User
    Mascaraded Client ID ....
    

# Remediation 

- Shut down prozess
- Blacklist client-ID
- Discover impact on data and systems
.....
