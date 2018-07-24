# Gitbook

Gitbook ist eine auf JavaScript basierende Software, welche es ermöglicht mit Hilfe von Markdown, HTML, CSS und JavaScript eine Online-Dokumentation, PDFs oder epubs zu erstellen. Sie ist unter der Apache 2.0 Lizenz veröffentlicht und Open Source auf Github einzusehen. Die Software selbst ist eine Software ohne grafische Benutzeroberfläche und wird über die Kommandozeile bedient.

Der Name der Software besteht aus zwei Teilen, welche auch die besonderen Merkmale der Software kennzeichnen. Einerseits ist da der erste Teil des Namens, welcher _Git_ lautet. Dieser steht dafür das die erstellte Dokumentation mit dem Versionskontrollsystem Git verwaltet werden kann. Diese ermöglicht ein vereinfachtes arbeiten von mehreren Personen an einem Projekt, sowie eine Versionierung der Dokumentation. Dadurch kann im Falle eines Fehlers bzw. aus anderen Gründen eine bestimmte Version der Dokumentation bzw. eines ihrer Abschnitte wiederhergestellt werden.

Andererseits verwaltet Gitbook, wie der zweite Teil des Namens andeutet, sogenannte _books_. Deren Struktur bzw. Aufbau ist über eine vorgegebene Ordnerstruktur bzw. Dateien vorgegeben, jedoch wird eine Konfiguration bzw. Individualisierung über entsprechende Dateien ermöglicht.

## Funktionen

Der in einem _book_ enthaltene Text kann entweder über Markdown bzw. AsciiDoc geschrieben werden. Diese ermöglichen ein Einfaches schreiben des Textes ohne sich währenddessen um eine entsprechende Formatierung zu kümmern. Weiter kann Gitbook Bücher verwalten, welche in mehreren Sprachen geschrieben sind. Diese Funktionalität ist im Besonderen für die Online-Dokumentation interessant, da die Benutzer interaktiv die Sprache wechseln können bzw. falls ein Abschnitt noch nicht übersetzt wurde, kann auf eine Standardsprache zurückgefallen werden. Die oben angesprochene Formatierung des Textes kann über sogenanntes Theming bzw. Templating angepasst werden. Das Templating wird im folgenden Kapitel genauer erklärt bzw. beides wurde im Laufe des Projektes verwendet und wird im Zuge dessen im Hauptteil genauer beschrieben. Zusätzlich zu den genannten Funktionen kann die Software über Plugins erweitert werden, wie beispielsweise, um eine Zitatfunktion bzw. eine Funktion für UML-Diagramme hinzuzufügen.

## Veröffentlichung

Wie oben schon angesprochen kann das geschriebene Gitbook über verschiedene Wege bzw. Varianten veröffentlicht werden. Entweder kann es als statische Webseite, als Epub-, PDF- oder Mobi-Datei veröffentlicht werden. Als vierte Variante gäbe es noch den kostenpflichtigen bzw. kommerziellen SaaS-Dienst von Gitbook selbst, jedoch ist dieser nicht beschrieben, da er aus Kostengründen nicht entsprechend betrachtet wurde. Über entsprechende Kommandos in der Kommandozeile können die einzelnen Varianten generiert werden. Nach der Erstellung durch die Software sind die entstandenen Artefakte ohne Abhängigkeiten und können z.B. in der Variante der statischen Website auf einem eigenen Webspace bereitgestellt werden. Die Bereitstellung für dieses Projekt wird im Hauptteil genauer erläutert.

{{"Gitbook2018" | cite}}
