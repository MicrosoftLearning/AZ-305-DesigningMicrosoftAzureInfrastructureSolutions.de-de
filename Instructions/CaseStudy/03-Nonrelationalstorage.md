---
casestudy:
  title: Entwerfen einer nicht relationalen Speicherlösung
  module: Non-relational storage solutions
---
# Entwerfen einer nicht relationalen Speicherlösung (Fallstudie)

## Anforderungen

Tailwind Traders möchte die Speicherkosten senken, indem doppelte Inhalte reduziert und ggf. in die Cloud migriert werden. Sie wünschen sich eine Lösung, die die Wartung zentralisiert und gleichzeitig weltweiten Zugang für Kund*innen bietet, die Mediendateien und Marketingmaterialien durchsehen. Darüber hinaus möchten sie die Speicherung von Unternehmensdatendateien adressieren. 

![Nicht relationale Speicherarchitektur](media/Nonrelational%20storage.png)

 

* **Mediendateien**. Zu den Mediendateien gehören Produktfotos und Videos, die auf der öffentlichen Website des Unternehmens gezeigt werden, die von uns selbst entwickelt und gepflegt wird. Wenn die Kundschaft einen Artikel aufruft, werden die entsprechenden Mediendateien angezeigt. Die Mediendateien liegen in verschiedenen Formaten vor, wobei JPEG und MP4 die gängigsten sind. 

* **Marketingliteratur**. Die Marketingliteratur umfasst Kundenberichte, Verkaufsflyer, Größentabellen und Informationen zur umweltfreundlichen Herstellung. Interne Marketingbenutzer*innen greifen über ein zugeordnetes Laufwerk auf ihren Windows-Arbeitsstationen auf die Literatur zu. Kund*innen greifen direkt über die öffentliche Website des Unternehmens auf die Literatur zu.

* **Unternehmensdokumente**. Dies sind interne Dokumente für Abteilungen wie Personalwesen und Finanzen. Diese Dokumente werden über eine intern entwickelte Webanwendung abgerufen und verwaltet. Die gesetzlichen Bestimmungen verlangen, dass verschiedene Dokumente für einen bestimmten Zeitraum aufbewahrt werden. Gelegentlich müssen Dokumente länger aufbewahrt werden, wenn rechtliche oder personalwirtschaftliche Fragen untersucht werden. Die meisten Unternehmensdokumente, die älter als ein Jahr sind, werden nur aus Gründen der Einhaltung von Vorschriften aufbewahrt und es wird nur selten auf sie zugegriffen.

* **Dateispeicherort**. Alle Dateien werden lokal im Rechenzentrum des Hauptsitzes gespeichert. Es gibt zahlreiche Dateifreigaben nach Abteilung oder Produktlinie organisiert. Die Datenserver haben Schwierigkeiten, Dateien für die Website bereitzustellen. Während der Stoßzeiten werden die Seiten der Website nur langsam dargestellt. 

* **Häufigkeit des Dateizugriffs**. Einige Produkte sind beliebter und auf diese Daten wird häufiger zugegriffen. Einige Produkte, wie z. B. Skiausrüstung, sind jedoch nur während der jeweiligen Saison zugänglich. Verkaufsveranstaltungen wecken ein großes Interesse an bestimmten Aktionsartikeln. 

## Aufgaben

1. Entwerfen Sie eine Speicherlösung für Tailwind Traders. 

      * Welche Art von Daten wird dargestellt? 

      * Welche Faktoren werden Sie in Ihrem Design berücksichtigen?

      * Verwenden Sie Blobzugriffsebenen?

      * Verwenden Sie unveränderlichen Speicher?

      * Wie wird sicher auf die Inhalte zugegriffen?

2.  Ihre Lösung sollte die Medien, Marketingliteratur und Unternehmensdokumente berücksichtigen. Ihre Empfehlungen können je nach Datenlage unterschiedlich ausfallen. Seien Sie bereit, Ihre Entscheidungen zu besprechen. 

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?
