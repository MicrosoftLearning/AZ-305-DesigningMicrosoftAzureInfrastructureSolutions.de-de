---
casestudy:
  title: Entwerfen einer App-Architekturlösung
  module: App architecture solutions
---
# Entwerfen einer App-Architekturlösung

## Anforderungen

Tailwind Traders plant, seine Website zu aktualisieren, um kundengelieferte Produktbilder zusätzlich zu den bereits vorhandenen, vom Marketing bereitgestellten Fotos einzubeziehen. Sie sind der Meinung, dass mehr Fotos von Produkten im Gebrauch potenziellen Kund*innen ein besseres Gefühl dafür vermitteln, wie frühere Kund*innen ihre Produkte nach dem Kauf geliebt haben. Sie haben einige Anforderungen, wie unten beschrieben:

* Hochgeladene Bilder müssen überprüft werden, bevor sie auf der Website veröffentlicht werden. Sowohl die Rechtsabteilung als auch die Marketingabteilung fordern, dass die Bilder nach dem ersten Hochladen auf Probleme geprüft werden, die ein schlechtes Licht auf das Unternehmen werfen oder rechtliche Probleme verursachen könnten. Eine interne API wurde bereits entwickelt und bereitgestellt, die die erforderliche Überprüfung durchführen kann. 

* Basierend auf vorhandenen Mustern erwartet Tailwind Traders, dass die Bilduploads im Laufe des Tages sehr ungleichmäßig stattfinden. In bestimmten Zeiträumen kann es mehr Uploads geben, als die Scansoftware verarbeiten kann, während in anderen Zeiträumen nur sehr wenige oder gar keine Uploads stattfinden.

* Nachdem ein hochgeladenes Bild vom System gescannt und genehmigt wurde, möchte Tailwind Traders der Kundschaft eine E-Mail senden, die ihnen für die Übermittlung ihres Bilds danken soll.

* Die Kosten und die Verwaltung der Lösung sind ein Problem, zumal Tailwind Traders nicht sicher ist, wie beliebt diese Funktion anfangs sein wird. Die Kosten sollen minimiert und serverlose Lösungen genutzt werden, wo immer dies möglich ist.

 

![App-Architektur](media/Apparchitecture.png)

 

## Aufgabe

Entwerfen Sie eine Architektur für die Bilder der Kundschaft, die zur Unternehmenswebsite hinzugefügt werden sollen. 

* Wo sollen die Bilder gespeichert werden?

* Wie stellen Sie sicher, dass alle Bilder gescannt werden, selbst wenn die Anzahl der Uploads die Scankapazität übersteigt?

* Sobald Bilder genehmigt wurden und die Katalogdatenbank aktualisiert wird, wie wird die Kundschaft benachrichtigt? 

Wie setzen Sie die Säulen des Well-Architected Framework ein, um eine qualitativ hochwertige, stabile und effiziente Cloudarchitektur zu schaffen?

 
