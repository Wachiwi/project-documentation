## Styling

Der Bereich Styling orientiert sich an der visuellen Darstellung des Inhaltes. Dazu gehören Werte bzw. Einflussfaktoren wie Schriftart, Schriftgröße, Zeilenabstand etc., welche auch im Richtliniendokument vorgegeben sind. Jedoch sind diese nur als Empfehlung zu sehen und deshalb wurde sich am Coporate Design der Hochschule orientiert. Dies repräsentiert ein modernes Design, welches schon in redaktionellen Inhalten erprobt wurde. Dadurch ist sichergestellt, dass es gut lesbar ist und eine Zugehörigkeit zur Hochschule ansetzt.

Da die im Corporate Design verwendete Schriftart kommerziell ist, wird die Webschriftart des Designguides verwendet, welche die Schriftart Roboto ist. Weiter gibt das Corporate Design die Farben Rot, mit dem Hexwert #E00034, Dunkelgrau, mit dem Hexwert #4B565E, und Hellgrau, mit dem Hexwert #EAEBEB, vor. Die Farbe Rot wird hierbei bei Verknüpfungen zwischen Seiten, die Farbe Dunkelgrau als allgemeine Schriftfarbe und das Hellgrau als Kontrastfarbe.  {{ "HSCoburg2018" | cite }}

Das Design wurde über ein CSS-Stylesheet auf das Gitbook angewendet, dessen relevante Inhalte in dem unten dargestellten Quellcodeausschnnitt dargestellt sind. Für die verschiedenen Formatvarianten Web und PDF, müssen auch unterschiedliche Arten von CSS geschrieben werden.

!CAPTION Stylesheet für das Corporate Design
```
* {
  color: #4B565E;

}

.book.font-family-1,
.book-summary {
  font-family: 'Roboto', sans-serif;
}

.book-summary ul.summary li.active>a {color: #E00034;}

ul.summary li.chapter>span {
  padding: 10px 15px;
  padding-top: 20px;
  text-transform: uppercase;
  color: #939da3;
  margin-left: unset;
}
```
