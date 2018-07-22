## Gitbook Struktur

Wie oben schon erwähnt, sind die Dateien _book.json_, _SUMMARY.md_, _README.md_ und _GLOSSARY.md_ und deren Bedeutung durch Gitbook vorgegeben. Jede dieser Dateien hat eine spezielle Bedeutung in einem Gitbook, welche nun erläutert werden soll {{ "Gitbook2018b" | cite }}.

**SUMMARY.md**

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

Hierbei können die einzelnen Hierarchieebenen durch eine eingerückte Liste oder durch Markdown-Überschriften in Abschnitte und Kapitel unterteilt werden. Dabei entsprechen Listen unter den entsprechenden Überschriften Kapiteln der zweiten Hierarchieebene. Die Form der Menüpunkte ist dabei in Form von Links dargestellt. Das Format \`\* \[Titel\]\(Datei\)\` ist so aufgebaut, dass in den eckigen Klammern der Titel steht, welcher in dem Inhaltsverzeichnis angezeigt werden soll. Darauf kommt in den runden Klammern der relative Pfad zur Datei, in der der Inhalt zu dem entsprechenden Inhaltsverzeichnis gespeichert ist.

**README.md**

Die Datei README.md erfüllt nach Gitbook die Funktion der Kurzübersicht über den Inhalt zu geben. Daher eignet sich diese Datei besonders für Abstracts.

**GLOSSARY.md**

Die GLOSSARY.md Datei ist eine Hilfsdatei, die einen Glossar beinhaltet und die Verwendung der Glossarbegriffe in allen Inhalten verknüpft. Hierbei ist zu beachten, dass die Glossarbegriffe in einer entsprechenden Form notiert werden müssen. Die Glossarbegriffe müssen in Markdown mit einer Überschrift der zweiten Ebene beschrieben werden. Der darauf folgende Absatz ist dann die Beschreibung des Glossarbegriffs. Wie dieser Glossarbegriff dann im Text beispielsweise der Webansicht verwendet wird ist in der unten dargestellten Grafik dargestellt. Der Glossarbegriff wird unterstrichen und verlinkt. Bewegt man die Maus über den Begriff wird die Bedeutung angezeigt bzw. man kann darauf klicken und wird zum Glossar weitergeleitet.

![](/img/glossar-use.png)

_**book.json**_

Dies ist die wichtigste Datei in einem Gitbook, da sie alle Konfigurationsinformationen enthält, die für die Erstellung des Gitbooks notwendig sind. Die Konfigurationsinformationen unterscheiden sich hierbei in Meta- und Plugininformationen. An sich kann auch über eine Konfigurationsoption, die Bedeutung der vorher genannten Dateien, wie SUMMARY.md überschrieben werden. Die Konfiguration selbst ist im JSON-Format abgespeichert und muss darin editiert werden.
{{ "Gitbook2018b" | cite }}

!CAPTION Beispielhafter Inhalt einer _book.json_-Datei

```
{
  "root": ".",
  "title": "Lebendige Projektdokumentationen mit Hilfe von GitBook",
  "description": "",
  "author": "David Schwarzmann",
  "isbn": "",
  "language": "de",
  "direction": "ltr",
  "gitbook": "^3.2.3",
  "plugins": [
    "-fontsettings",
    "-sharing",
    "pretty-term",
    "bibtex-indexed-cite",
    "plantuml-svg",
    "code-captions"
  ],
  "pluginsConfig": {
    "bibtex-indexed-cite": {
      "path": "./literature.bib"
    }
  },
  "structure": {},
  "pdf": {
    "pageNumbers": true,
    "fontSize": 12,
    "fontFamily": "Roboto",
    "paperSize": "a4",
    "margin": {
      "top": 56,
      "bottom": 56,
      "right": 62,
      "left": 62
    }
  }
}
```

Die erste Option ist die Konfigurationsvariable `root`, welche beschreibt, welches Verzeichnis das Wurzelverzeichnis des Gitbooks ist. Dies ist relevant, damit Gitbook notwendige Dateien bzw. Verzeichnisse automatisch finden bzw. anlegen kann. 

Darauf folgen die Konfigurationsvariablen `title`, `description` und `author`. Diese geben, wie der Name der Variablen andeutet, die Mögichkeit den Titel und die Beschreibung zu setzen. Das Feld des Autors ist an sich nur für eine Person gedacht, kann jedoch auch für mehrere Autoren verwendet werden, die dann beispielsweise durch ein Komma getrennt werden. Als nächstes folgen die Konfigurationsfelder `isbn`, `language`, `direction` und `gitbook`. Das Feld `isbn` ist ein optionales Feld, welches ermöglicht die ISBN des Dokuments zu setzen, fall es veröffentlicht wurde. Das `language`-Feld gibt an, in welcher Sprache das Dokument geschrieben wurde. Sollte diese Feld nicht gestzt sein, ist der Standardwert die Sprache Englisch mit dem Wert `en`. Das Feld `direction` gibt die Schreibt- und Leserichtung des Dokumentes an, in der es geschrieben wurde. Es existieren hierfür die Werte `rtl` und `ltr`, welche bedeuten von links nach rechts (`ltr`) oder von rechts nach links (`rtl`). Das vorerst letzte einfache Feld ist das Feld `gitbook`, welches die Version von Gitbook angibt, in der das Dokument erstellt wurde und auch veröffentlicht wurde.

Die  darauf folgenden Felder `plugins`, `pluginsConfig`, `structure` und `pdf` sind dahingehend komplizierter, dass sie weitere Konfigrationsvariablen beinhalten können. In dem Feld `plugins` ist die Liste der aktivierten und deaktivierten Plugins beinhaltet. Hierbei ist das Feld eine Auflistung aller Plugins, welche wiederum als Zeichenkette in `"` dargestellt sind. Das `-` vor einem Plugin ist eine Besonderheit, da es bedeutet, dass das genannte Plugin deaktiviert ist. Deaktiviert können nur die standardmäßig aktivierten Plugins werden. Erweitert wird das `plugins` Feld durch das Feld der `pluginsConfig`, welches ermöglicht die aktivierten Plugins zu konfigurieren. Eine mögliche Konfiguration ist wiederum vom Plugin selbst abhängig, ob diese möglich ist. Sollte eine Konfiguration möglich sein, dann kann diese erfolgen, indem der Name des Plugins eingetragen wird und darin die spezifischen Konfigurationsparameter angepasst werden. 




