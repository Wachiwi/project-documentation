# Projektstruktur

Die Projektstruktur baut auf der standardmäßigen Struktur von Gitbook auf. Dabei sind relevante Dateien und Ordner die Dateien _book.json, SUMMARY.md, README.md \_und GLOSSARY.md._ _Diese geben die Grundstruktur vor, welche durch die Ordner_ Einleitung, Grundlagen, Hauptteil_ und \_Fazit_ wird. Diese erfüllen einen organisatorischen und logischen Zweck um die Übersichtlichkeit der Kapitel zu ermöglichen. Eine Übersicht über die Dateistruktur wird im folgenden Quellcodeabschnitt aufgezeigt. Weiter soll im folgenden auf die Bedeutung der einzelnen Komponenten  eingegangen werden.

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

Wie oben schon erwähnt, sind die Dateien \_book.json, SUMMARY.md, README.md \_und GLOSSARY.md und deren Bedeutung durch Gitbook vorgegeben. Jede dieser Dateien hat eine spezielle Bedeutung in einem Gitbook, welche nun erläutert werden soll.

### _SUMMARY.md_

Die Datei _SUMMARY.md_ hat die Funktion des Inhaltsverzeichnisses und spiegelt dieses in einer textuellen Beschreibung wieder. Darin werden die Namen der Einträge des Inhaltsverzeichnisses auf Dateien mit dem entsprechenden Inhalt abgebildet. Eine beispielsweise Datei für den Inhalt ist im folgenden Ausschnitt dargestellt. Wie alle anderen Dokumente werden die

!CAPTION Beispielhafte SUMMARY.md

```
# Summary

* [Abstract](README.md#abstract_en)
* [Abstrakt](README.md#abstract_de)

## Einleitung

  * [Hintergrund](einleitung/hintergrund.md)
  * [Projektkontext](einleitung/projektkontext.md)
  * [Relevanz und Abgrenzung](einleitung/relevanz.md)
  * [Dokumentstruktur](einleitung/struktur.md)

## Grundlagen

  * [Markdown](grundlagen/markdown.md)
  * [HTML, CSS & JavaScript](grundlagen/html_js.md)
  * [Git](grundlagen/git.md)
  * [Gitbook](grundlagen/gitbook.md)

## Kern

  * [Projektstruktur](hauptteil/projektstruktur.md)
  * [Bewertungskriterien](hauptteil/bewertungskriterien.md)
  * [Styling](hauptteil/styling.md)
  * [Theming](hauptteil/theming.md)
  * [Infrastruktur](hauptteil/infrastruktur.md)

## Fazit & Ausblick

  * [Fazit](fazit/fazit.md)
  * [Ausblick](fazit/ausblick.md)

---

* [Literaturverzeichnis](Literature.md)

## Anhang

* [Anhang 1](Anhang/a1.md)
* [Anhang 2](Anhang/a2.md)
* [Anhang 3](Anhang/a3.md)
```

Hierbei können die einzelnen Hierarchieebenen durch eine eingerückte Liste oder durch Markdown-Überschriften in Abschnitte und Kapitel unterteilt werden. Dabei entsprechen Listen unter den entsprechenden Überschriften Kapiteln der zweiten Hierarchieebene. Die Form der Menüpunkte ist dabei in Form von Links dargestellt. Das Format \`\* \[Titel\]\(Datei\)\` ist so aufgebaut, dass in den eckigen Klammern der Titel 

### _README.md_

### _GLOSSARY.md_

### _book.json_

## Eigene Struktur



