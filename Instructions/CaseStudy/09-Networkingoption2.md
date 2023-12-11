---
casestudy:
  title: Entwerfen einer Netzwerklösung – BI-Unternehmensanwendung
  module: Network infrastructure solutions
---
# Entwerfen einer Netzwerkinfrastrukturlösung  

## Anforderungen

Während sich das IT-Team von Tailwind Traders Enterprise darauf vorbereitet, die Strategie für die Migration einiger Unternehmensworkloads zu Azure zu definieren, muss es die erforderlichen Netzwerkkomponenten identifizieren und eine Netzwerkinfrastruktur entwerfen, die für deren Unterstützung erforderlich ist. Da Tailwind Traders global tätig ist, wird das Unternehmen mehrere Azure-Regionen für das Hosting seiner Anwendungen nutzen. Die meisten dieser Anwendungen sind von Infrastruktur- und Datendiensten abhängig, die ebenfalls in Azure angesiedelt sein werden. Interne Anwendungen, die zu Azure migriert werden, müssen für Tailwind Traders-Benutzer zugänglich bleiben. Anwendungen mit Internetanbindung, die zu Azure migriert werden, müssen für externe Kunden zugänglich bleiben. 

Für die Erstellung des ersten Netzwerkdesigns wählte das IT-Team von Tailwind Traders Enterprise zwei Hauptanwendungen aus, die repräsentativ für die gängigsten Kategorien von Workloads sind, die zu Azure migriert werden sollen.  

## Design – BI-Unternehmensanwendung 

![BI-Unternehmensanwendungs-Architektur](media/compute.png)

-   Eine interne, Windows-basierte, dreistufige Business Intelligence (BI)-Unternehmensanwendung, bei der auf der Front-End-Ebene IIS-Webserver laufen, auf der mittleren Ebene .NET Framework-basierte Geschäftslogik gehostet wird und die Back-End-Ebene als SQL Server Always On-Verfügbarkeitsgruppen-Datenbank implementiert ist. 

-   Diese Anwendung wird als unternehmenskritisch kategorisiert und erfordert Hochverfügbarkeitsbereitstellungen mit einer Verfügbarkeits-SLA von 99,99 % und Notfallwiederherstellungs-Bereitstellungen mit einem RPO von 10 Minuten und einem RTO von 2 Stunden.

-   Um die Konnektivität zu den zu Azure migrierten internen Anwendungen herzustellen, muss Tailwind Traders eine hybride Verbindung von seinen lokalen Rechenzentren aus aufbauen. Die IT-Gruppe des Unternehmens hat bereits festgelegt, dass diese Konnektivität über eine ExpressRoute-Verbindung von ihrem Hauptrechenzentrum in Seattle aus realisiert wird, allerdings ist zum jetzigen Zeitpunkt noch nicht klar, welche Ausweichlösung für den Fall vorgesehen ist, dass diese Leitung nicht mehr verfügbar ist. Der CFO von Tailwind Traders möchte die Kosten für eine weitere, redundante ExpressRoute-Verbindung vermeiden. 

- Es gibt zusätzliche Überlegungen, die für die lokale Konnektivität zu internen Anwendungen gelten, die zu Azure migriert wurden. Da die Azure-Umgebung von Tailwind Traders aus mehreren Abonnements und effektiv aus mehreren virtuellen Netzwerken bestehen wird, ist es zur Kostenminimierung wichtig, die Anzahl der Azure-Ressourcen zu minimieren, die für die Implementierung der zentralen Netzwerkfunktionen erforderlich sind. Zu diesen Funktionen gehören Hybridkonnektivität zu lokalen Standorten sowie das Filtern von Datenverkehr. Diese Notwendigkeit, die Kosten zu minimieren, steht übrigens im Einklang mit den Anforderungen an die Informationssicherheit und das Risiko. Sie besagen, dass der gesamte Datenverkehr zwischen lokalen Standorten und virtuellen Azure-Netzwerken über ein einziges virtuelles Netzwerk fließen muss, in dem die für die Hybridkonnektivität und das Filtern von Datenverkehr zuständigen Komponenten untergebracht sind. 

-   Gemäß den von den Informationssicherheits- und Risikoteams von Tailwind Traders definierten Anforderungen muss die gesamte Kommunikation zwischen Azure-VMs auf verschiedenen Ebenen, die Teil derselben Anwendung sind, nur die Ports zulassen, die für die Ausführung und Wartung der Anwendung erforderlich sind. Aufgrund des begrenzten IP-Adressraums ist es jedoch unter Umständen nicht möglich, jeder Ebene dedizierte Subnetze zuzuweisen. Die IT-Abteilung eines Unternehmens muss die optimale Methode zur Konfiguration von Quelle und Ziel für das Filtern von Datenverkehr ermitteln, die keine direkte Bezugnahme auf IP-Adressen oder IP-Adressbereiche erfordert.


## Aufgaben – BI-Unternehmensanwendung 

1. Entwerfen Sie eine 3-stufige Netzwerklösung für die BI-Anwendung. Ihr Design könnte Azure ExpressRoute, VPN-Gateways, Anwendungsgateways, Azure Firewall und Azure-Lastenausgleiche umfassen. Ihre Netzwerkkomponenten sollten in virtuelle Netzwerke gruppiert werden, und Netzwerksicherheitsgruppen sollten berücksichtigt werden. Bereiten Sie sich darauf vor, zu erklären, warum Sie die einzelnen Komponente der Lösung gewählt haben. 

2. Wie würde sich dies auf der Grundlage Ihrer Architektenlösung aus der Compute-Fallstudie auf das Netzwerkdesign auswirken? Benötigen Sie zusätzliche Netzwerkressourcen, um den Zugriff auf die modernisierte Anwendung zu sichern? Würden Sie einige der empfohlenen Lösungen, die in Ihrem ursprünglichen Netzwerkdesign implementiert waren, nicht mehr benötigen? 

3. Wie würden Sie auf der Grundlage Ihrer speicherbezogenen (relationalen) Fallstudie das Netzwerkdesign aktualisieren, um den Zugriff auf das Speicherkonto zu sichern und sicherzustellen, dass nur ausgewählte Benutzer*innen Zugriff auf das Speicherkonto haben?

4. Wie wollen Sie auf der Grundlage der Modernisierung des SQL-Back-Ends einen pragmatischen Zugriff auf die Datenbank ermöglichen, sodass das Front-End keine hartcodierten Geheimnisse in seiner Codebasis hat?

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?
