
# Entwerfen einer Netzwerkinfrastrukturlösung  

## Anforderungen

Während sich das IT-Team von Tailwind Traders Enterprise darauf vorbereitet, die Strategie für die Migration einiger Unternehmensworkloads zu Azure zu definieren, muss es die erforderlichen Netzwerkkomponenten identifizieren und eine Netzwerkinfrastruktur entwerfen, die für deren Unterstützung erforderlich ist. Da Tailwind Traders global tätig ist, wird das Unternehmen mehrere Azure-Regionen für das Hosting seiner Anwendungen nutzen. Die meisten dieser Anwendungen sind von Infrastruktur- und Datendiensten abhängig, die ebenfalls in Azure angesiedelt sein werden. Interne Anwendungen, die zu Azure migriert werden, müssen für Tailwind Traders-Benutzer zugänglich bleiben. Anwendungen mit Internetanbindung, die zu Azure migriert werden, müssen für externe Kunden zugänglich bleiben. 

Für die Erstellung des ersten Netzwerkdesigns wählte das IT-Team von Tailwind Traders Enterprise zwei Hauptanwendungen aus, die repräsentativ für die gängigsten Kategorien von Workloads sind, die zu Azure migriert werden sollen.  

### Entwurf – Produktkatalog-Unternehmensanwendung

![Produktkatalogarchitektur](media/catalog.png)

- Eine Windows-basierte, zweistufige Webanwendung auf Basis von .NET Core, die Zugriff auf den Produktkatalog bietet und in einer SQL Server Always On-Verfügbarkeitsgruppen-Datenbank gehostet wird. Diese Anwendung wird als unternehmenskritisch eingestuft, mit einem Verfügbarkeits-SLA von 99,99 %, einem RPO von 10 Minuten und einem RTO von 2 Stunden. 

-   Business-Leads betonen, wie wichtig ein optimales Kundenerlebnis beim Zugriff auf internetbasierte Anwendungen ist. Daher ist es von entscheidender Bedeutung, dass die Zeit, die zum Laden von Webseiten und zum Herunterladen statischer Inhalte benötigt wird, minimiert wird. Ebenso sollte ein Ausfall einzelner Server, auf denen Komponenten der Webanwendung und ihre Abhängigkeiten gehostet werden, vernachlässigbare Auswirkungen auf die von den Kund*innen wahrgenommene Verfügbarkeit der Webanwendung haben. Es ist zwar klar, dass ein regionaler Ausfall zu einer Unterbrechung bestehender Web-Sitzungen führen kann, doch sollte der Failover zu einem Notfallwiederherstellungsstandort automatisch erfolgen.

- Um die Vorteile von Azure PaaS-Diensten nutzen zu können, hat sich das Enterprise-IT-Team entschieden, die Datenbank der Produktkatalog-Unternehmensanwendung mithilfe von Azure SQL-Datenbank zu implementieren. 

- Die Informationssicherheits- und Risikoteams von Tailwind Traders verlangen, dass die gesamte Kommunikation zwischen Azure-VMs und PaaS-Diensten, die Teil der gleichen Anwendung sind, über den Azure-Backbone und nicht über einen öffentlichen Endpunkt der PaaS-Dienste erfolgt. 

## Aufgaben – Produktkatalog-Unternehmensanwendung

1. Entwerfen Sie eine zweistufige Netzwerklösung für den Produktkatalog. Gegebenenfalls kann Ihr Design Azure Front Door, WAF, Azure Firewall und einen Azure-Lastenausgleich umfassen. Ihre Netzwerkkomponenten sollten in virtuelle Netzwerke gruppiert werden, und Netzwerksicherheitsgruppen sollten berücksichtigt werden. Seien Sie darauf vorbereitet, zu erläutern, warum Sie die einzelnen Komponenten des Designs ausgewählt haben. 

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?

