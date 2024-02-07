---
casestudy:
  title: Entwerfen einer Computelösung
  module: Compute solutions
---

# Entwerfen einer Computelösung

## Anforderungen

Tailwind Traders möchte seine Produktkataloganwendung zur Cloud migrieren. Diese Anwendung verfügt über eine herkömmliche 3-stufige Konfiguration mit SQL Server als Datenspeicher. Das IT-Team hofft, dass Sie dabei helfen können, die Anwendung zu modernisieren. Sie haben dieses Diagramm und mehrere Bereiche bereitgestellt, die verbessert werden könnten. 

![Computearchitektur](media/compute.png)

* Die Front-End-Anwendung ist eine .NET Core-basierte Web-App. In Spitzenzeiten besuchen 1.750 Kund*innen pro Stunde die Website. 

* Die Anwendung wird auf IIS-Webservern auf einer Front-End-Ebene ausgeführt. Diese Ebene verarbeitet alle Kundenanfragen für den Kauf von Produkten. Während des letzten Feiertagsangebots erreichten die Front-End-Server ihre Leistungsbeschränkungen und Seitenladevorgänge waren langwierig. Das IT-Team hat in Erwägung gezogen, weitere Server hinzuzufügen, aber außerhalb der Geschäftszeiten sind die Server oft im Leerlauf.

* Auf der mittleren Ebene befindet sich die Geschäftslogik, die Kundenanfragen verarbeitet. Diese Anfragen sind häufig für Helpdesk-Support vorgesehen. Supportanfragen werden in eine Warteschlange gestellt, und in letzter Zeit waren die Wartezeiten sehr lang. Den Kund*innen wird der Kontakt per E-Mail angeboten, anstatt auf eine Kundenbetreuerin bzw. einen Kundenbetreuer zu warten. Viele Kund*innen scheinen jedoch frustriert zu sein und trennen die Verbindung lieber, als zu warten. Die Anzahl der Kundenanfragen beträgt 75-125 pro Stunde. 

* Die Back-End-Ebene verwendet eine SQL Server-Datenbank, um Kundenbestellungen zu speichern. Derzeit sind die Back-End-Datenbankserver gut leistungsfähig.

* Die hohe Verfügbarkeit ist zwar ein Anliegen, aber aufgrund gesetzlicher Bestimmungen muss das Unternehmen alle Ressourcen in einer einzigen Region aufbewahren.

## Aufgaben

* **Front-End-Ebene**. Welchen Azure-Computedienst würden Sie für die Front-End-Ebene empfehlen? Erläutern Sie, warum Sie sich für Ihre Lösung entschieden haben. 

* **Mittlere Ebene**. Welchen Azure-Computedienst würden Sie für die mittlere Ebene empfehlen? Erläutern Sie, warum Sie sich für Ihre Lösung entschieden haben. 

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?
