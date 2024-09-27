# NLP_Project_Animes

Die Dateien folgen der Benennungskonvention, dass alle mit OP oder op sich auf One Piece, alle mit NA bzw. na auf Naruto und alle mit DC oder dc auf Detective Conan beziehen.

## Scraper
In den Scraper genannten Dateien sind die Serien-spezifischen Scraper enthalten. Jeder dieser Dateien folgt dem gleichen Aufbau.
Zuächst wird das fandom-py-package und das io-package importiert. Ersters von beiden ist das Schlüsselelement für den Scraper, da es sich dabei um ein fertiges Package handelt, dessen Funktion es ist, Fandom-Wiki-Seiten zu scrapen.

Im ersten Schritt werden die Titel aller Seiten gescrapet indem sie in 500-er Schritten durchgegangen und einem Dictionary hinzugefügt werden. Die Begrenzung auf 500 ist von dem fandom-package vorgegeben: es können immer nur 500 zufällige Seiten gescrapet werden. Um sicherzustellen, dass alle Seiten gescrapet werden, werden diese Titel einem Dictionary hinzugefügt, um damit zu garantieren, dass jeder Titel nur einmal aufgenommen wird. Dieser Scraper und das Hinzufügen zum Dictionary wird so lange durchlaufen (durch eine While-Schleife) bis das Dictionary so lang ist wie es Seiten im Wiki gibt. Die genaue Anzahl konnte in der Regel der Statistik-Seite des Wikis entnommen werden.
Um mit den Titeln weiterarbeiten zu können wurden das Dictionary Zeile für Zeile ineine txt-Datei geschrieben, sodass diese Datei dann Zeile für Zeile abgearbeitet werden kann.
Im nächsten Schritt werden tatsächlich die Seiteninhalte gescrapet und nicht nur deren Titel. Dafür wird für jede Zeile der Dictionary-Datei der Inhalt der Seite, die zum aktuellen Titel gehört, gescrapet und in eine neue txt-Datei, welche dump genannt wird, geschrieben. Somit wird für jede Serie eine eigene Dictionay- und eine Dump-Datei erstellt.

## Datengrundlage
In den Dateien mit dump am Anfang sind die gescrapeten Daten zu finden. Sie enthalten den Titel der Seite sowie den Inhalt und nach einer Leerzeile den Titel der nächsten Seite.

## Ground Truth
In den Antworten_Bewertungen-Excel Mappen sind die verwendeten Ground Truth-Frage-Antworten-Paare und deren Quellen enthalten. Darüber hinaus enthalten sie auch die Antworten aller drei Modelle (Basis, ChatGPT, erweitertes Modell), ihre Similarity Scores, ihr Ranking sowie Kommentare zur Qualität der Antworten.






