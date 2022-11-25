# SOC Playbooks


## Use Cases

- [UC-001 – Process execution with command-line arguments
](./UC-001-Prozess_Execution.md)
- [UC-024 - Information Leakage ](./UC-0024-Infoleak.md)

## Daily Routines


### SVV

| UseCase | Dashboard   |  Check for |  Data Sources | Escalation time window |
|----------|----------|:-------------:|------:|-----:|
| Invalid Logins | Elastic Link| All Alerts | Falco Alert Stream | max 24h|
| Outbound Connections | Elastic Link| Non whitelisted Connections | Falco Alert Stream | max 24h|

#### Evidenzen

Update AOD Jira Ticket for SVV

### BGAG

| UseCase | Dashboard   |  Check for |  Data Sources | Escalation time window |
|----------|----------|:-------------:|------:|-----:|
| Invalid Logins | Elastic Link| All Alerts | Falco Alert Stream | max 24h|
| Outbound Connections | Elastic Link| Non whitelisted Connections | Falco Alert Stream | max 24h|

#### Evidenzen

Update Jira Ticket at Customer Jira instance

## Frequent Routines

Vulnerability Scan Report ....

#### Evidenzen

Update Jira ..

## Important Contacts

CISO Office  
CIO  
MOD

## Usefull Links

- https://talosintelligence.com/reputation_center/
- https://attack.mitre.org
- https://cve.mitre.org
- https://cwe.mitre.org
- https://www.virustotal.com/gui/home/upload


