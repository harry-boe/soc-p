# Case:  Information Leakage 

## Generelle Informationen 
Beschreibung 

Interne Informationen sind bewusst oder unbewusst abgeflossen oder der Öffentlichkeit zugänglich gemacht worden. 




### Beispiel

- Alert Dashboard (link to Elastic Dashboard)


## Vorbereitungen, Bemerkungen

### Vorgaben und Prozesse 
•	ISMS Datenklassifizierung
•	Sec Incident Prozess

### Assets

•	Known Systems, 
•	Assets - ISMS inventory
•	Datenschutz Verzeichnis)
•	Netbox ? (link to Netbox)


### Kontakte (ev. aus Netbox)

John.doe@nowhere.net

## Identifikation 

### Erkennung 

Einen nicht erlaubten Datenabfluss zu erkennen ist ....
Valiedierung 
Die Validierung des Vorfalls kann über folgende Datenquellen im SIEM allenfalls Validiert werden: 
      
### Datenquelle 

E-Mail
Empfänger,Subject oder Emailgrösse können Hinweise auf einen Datenabfluss liefern

Proxy Firewall Server
Allenfalls kann aufgrund von Verbindungen zu Online Storage Anbietern (oder ähnlichen Dienstleistungen) auf einen Datenabfluss 
Ermöglichen allenfalls einen Verbindungsnachweis auf 
Ermöglich die Suche nach Spuren von einem Datenabfluss auf dem Quellsystem

Abhängig vom Fall ist der Austausch mit Beteiligten sinnvoll oder auch eine weitergehende Analyse mit Toriaji, Google/Facebook/Twitter/Pastebin suchen oder ext. Partnern 3 Containment 
Die Kommunikationsabteilung (Team Shakespeare) ist zu informieren da eine Veröffentlichung/Bekanntmachung der Daten zu erwarten ist. Abhängig von der Art des Informationsabflusses kann dieser bei der Quelle oder den Empfängern gestoppt werden indem: 
Ein Account gesperrt wird (vorgängig mit HR klären)
Ein Workplace isoliert wird (um später eine forensische Analyse vorzunehmen) Der Zugang zu einem Drucker verhindert/überwacht wird
Eine Webseite offline genommen wird 


# Triage

### False Positiv

### Minor Incident

	Indikation

### Mayor Incident

	Eskalation

		CSIRT



# Remediation 

Falls möglich Daten von öffentlich zugänglichen Diensten löschen lassen: 
Dienstleister Beschreibung Link 






Google Daten aus dem Google Cache löschen. https://developers.google.com/search/docs/advanced/crawling/remove-information 

Falls das nicht möglich ist, dies dem CISO Office, Datenschutzbeauftragtem  mit allen vorhandenen Information melden.
Recovery 
Falls ein oder mehrere Systeme kompromittiert wurden soll es wieder hergestellt/neu installiert werden
Information an Mitarbeitende um Awareness zu erhöhen und Fragen zum Vorfall zu klären
Nach dem Übergang zum Normalbetrieb sollen allfällig getroffene Kommunikationsmassnahmen (Infobanner) rückgängig gemacht werden. 
Aftermath 
Falls Sinnvoll bei der nächsten cyberART Grosswetterlage/Systemdemo über den Incident informieren, was lief gut, wo gibt es noch potential. Abschliessende Dokumentation des Incidents im SNOW unter berücksichtigung folgender Aspekte: 
Wie wurde der Vorfall entdeckt
Was wurde wann gemacht (ergänzen falls nötig)
Was lief gut/nicht gut
Was war die Auswirkung (Aufwand innerhalb cyberART, Auswirkungen auf weitere Teile der SBB) 
Kontinuirliche Verbesserung bei folgenden Themen: 
Erkennung: müssen neue Datenquellen an das SIEM angeschlossen werden um Use Cases zu verbessern/erweitern? Kommunikation: müssen weitere/andere Stellen informiert und involviert werden? 
Bemerkungen 
s