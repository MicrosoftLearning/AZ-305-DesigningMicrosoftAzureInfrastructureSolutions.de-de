---
casestudy:
  title: Entwerfen einer relationalen Speicherlösung
  module: Relational storage solutions
---
# Entwerfen einer relationalen Speicherlösung (Fallstudie)

## Anforderungen

Tailwind Traders möchte seine bestehende Datenbank für die öffentliche Website nach Azure verlagern, da auch das Front-End der Website dorthin verlagert werden soll.  Das Front-End der Website wird anfänglich nur in zwei Regionen für Redundanz bereitgestellt.  Es ist jedoch davon auszugehen, dass die Website bei steigendem Besucheraufkommen auf andere Regionen der Welt ausgedehnt werden wird. Die Datenbank, die Sie migrieren möchten, enthält den Produktkatalog und alle Onlinebestellungen.  Derzeit wird die Datenbank auf einer einzelnen lokalen Microsoft SQL Server Always On-Verfügbarkeitsgruppe ausgeführt.

![Nicht relationale Speicherarchitektur](media/relational%20storage.png)

Hauptanliegen von Tailwind Traders:

-   **Hochverfügbarkeit:**  Ein Hauptanliegen von Tailwind Traders ist es, dass diese Datenbank hochverfügbar ist, da sie für das Geschäft entscheidend ist.  Ausfälle können zu Umsatzeinbußen oder zum Verlust des Kundenvertrauens führen.

-   **Leistung der Website.**  Während die Leistung beim Aufgeben von Bestellungen normalerweise zufriedenstellend ist, wird das Durchsuchen von Seiten mit vielen aufgelisteten Artikeln als „träge“ bezeichnet.

-   **Sicherheit:**  Tailwind Traders ist sehr besorgt darüber, dass persönliche oder finanzielle Informationen, die in der Datenbank gespeichert sind, offengelegt werden könnten.  Neben der Implementierung geeigneter Sicherheitsmaßnahmen muss das Sicherheitsteam auch sicherstellen, dass nach Möglichkeit branchenübliche Best Practices angewendet werden.


## Aufgaben

1.  Entwerfen Sie die Datenbanklösung. Ihr Entwurf sollte Autorisierung, Authentifizierung, Preisgestaltung, Leistung und hohe Verfügbarkeit berücksichtigen. 
2.  Skizzieren Sie Ihre Entscheidung und erläutern Sie Ihre Lösung. 

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?
