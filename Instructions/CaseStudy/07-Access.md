---
casestudy:
  title: Entwerfen von Lösungen für Authentifizierung und Autorisierung
  module: Authentication and authorization solutions
---


# Entwerfen von Lösungen für Authentifizierung und Autorisierung

## Anforderungen

Tailwind Traders geht es sehr gut, und das Unternehmen erweitert seine Belegschaft. Sie haben erfolgreich einen Online-Händler im Sportbekleidungsbereich übernommen. Das Unternehmen hat auch einen Partner zur Auslagerung von Marketingliteratur gefunden. Tailwind Traders verwendet Azure Active Directory für Benutzer- und Gruppenkonten. Hier sind zwei spezifische Initiativen, bei denen die IT-Abteilung gerne Ihre Unterstützung hätte. 

**Neue Benutzerkonten**

  * Durch die Übernahme des Online-Händlers wird Tailwind Traders um 75 Mitarbeiter*innen erweitert. Alle neuen Benutzer*innen haben lokale Active Directory-Domänendienste-Konten in der bestehenden Domäne des Einzelhändlers.

  * Der neue Marketingpartner verfügt zunächst über 15 Mitarbeiter*innen, die Unternehmenszugriff benötigen. Diese Mitarbeiter*innen verfügen bereits über Microsoft Entra-Identitäten im Microsoft Entra-Mandanten des Partners.  

  * Die neuen Mitarbeiter*innen befinden sich an verschiedenen geografischen Standorten und benötigen Kontoberechtigungen für ihre neuen Tätigkeiten. Es werden einige Änderungen an vorhandenen Mitarbeiterrollen erwartet. 

  * Die IT-Abteilung möchte diese Gelegenheit nutzen, um neue Funktionen für die Identitätssicherheit einzuführen. 

**Neuer Anwendungszugang**

  * Das Geschäftsentwicklungsteam verfügt über eine Anwendung, auf der eine Azure-VM ausgeführt wird, sowie über Daten, die in einer Azure SQL-Datenbank gespeichert sind. Es muss einen Weg finden, der VM die sichere Abfrage der Azure SQL-Datenbank zu ermöglichen. 
  * Außerdem benötigen sie einen lokalen Server, um sicher auf die SQL-Datenbank zugreifen zu können, ohne Anmeldedaten im Anwendungscode oder in den Konfigurationsdateien zu speichern.

## Aufgaben

**Neue Benutzerkonten**

  * Skizzieren Sie den Prozess für das Einführen der erworbenen Benutzerkonten.

  * Skizzieren Sie das Verfahren zum Hinzufügen der neuen Partnerkonten. 

  * Achten Sie bei den oben genannten Anforderungen darauf, alle Tools anzugeben, die verwendet werden. Führen Sie mindestens drei Vorteile Ihrer vorgeschlagenen Lösung auf. 

* Geben Sie mindestens drei Empfehlungen zur Verbesserung der Benutzeridentitätslösungen von Tailwind Traders. Bewerten Sie die Empfehlungen in der Reihenfolge der Wichtigkeit. Begründen Sie, warum Sie diese Vorschläge machen. 

**Neuer Anwendungszugang**

  * Stellen Sie eine Zugriffslösung für die Geschäftsentwicklungsanwendung bereit.

  * Stellen Sie eine Zugriffslösung für die lokalen Ressourcen bereit.

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?
