# Projektstruktur

Die Projektstruktur baut auf der standardmäßigen Struktur von Gitbook auf. Dabei sind relevante Dateien und Ordner die Dateien _book.json, SUMMARY.md, README.md _und GLOSSARY.md._ _Diese geben die Grundstruktur vor, welche durch die Ordner_ Einleitung, Grundlagen, Hauptteil_ und _Fazit_ wird. Diese erfüllen einen organisatorischen und logischen Zweck um die Übersichtlichkeit der Kapitel zu ermöglichen. Eine Übersicht über die Dateistruktur wird im folgenden Quellcodeabschnitt aufgezeigt. Weiter soll im folgenden auf die Bedeutung der einzelnen Komponenten  eingegangen werden.

!CAPTION Übersicht über die Projektstruktur

```
$ tree -L 1 .                                                                                                                                                                     ‹2.5.0›  09:15:45
.
├── GLOSSARY.md
├── Literature.md
├── Notes.md
├── README.md
├── SUMMARY.md
├── _assets
├── _book
├── _layouts
├── book.json
├── einleitung
├── fazit
├── grundlagen
├── hauptteil
├── literature.bib
└── node_modules

8 directories, 7 files
```

## Vorgegebene Struktur

Wie oben schon erwähnt, sind die Dateien _book.json, SUMMARY.md, README.md _und GLOSSARY.md und deren Bedeutung durch Gitbook vorgegeben. Jede dieser Dateien hat eine spezielle Bedeutung in einem Gitbook, welche nun erläutert werden soll.

### _SUMMARY.md_

Die Datei _SUMMARY.md_ hat die Funktion des Inhaltsverzeichnisses und spiegelt dieses in einer textuellen Beschreibung wieder. Darin werden die Namen der Einträge des Inhaltsverzeichnisses auf Dateien mit dem entsprechenden Inhalt abgebildet. Eine beispielsweise Datei für den Inhalt ist im folgenden Ausschnitt dargestellt.

### _README.md_



### _GLOSSARY.md_



### _book.json_

## Eigene Struktur



