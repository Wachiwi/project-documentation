## Styling

Der Bereich Styling orientiert sich an der visuellen Darstellung des Inhaltes. Dazu gehören Werte bzw. Einflussfaktoren wie Schriftart, Schriftgröße, Zeilenabstand etc.. Dazu wurde sich am Coporate Design der Hochschule orientiert, da dies ein modernes Design beinhaltet, welches schon in readktionellen Inhalten erprobt wurde.

Da die im Corporate Design verwendete Schriftart kommerziell ist, wird die Webschriftart des Designsguides verwendet, welche die Schrifart *Roboto* ist. Weiter gibt das Corporate Design die Farben _Rot_, mit dem Hexwert `#E00034`, _Dunkelgrau_, mit dem Hexwert `#4B565E`, und _Hellgrau_, mit dem Hexwert `#EAEBEB`, vor. Die Farbe Rot wird hierbei bei Verknüpfungen zwischen Seiten, die Farbe Dunkelgrau als allgemeine Schriftfarbe und das Hellgrau als Kontrastfarbe. {{ "HSCoburg2018" | cite }}

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

ul.summary li.chapter>a,
ul.summary li.chapter>span {
  margin-left: 1em;
}


ul.summary li.chapter>span {
  padding: 10px 15px;
  padding-top: 20px;
  text-transform: uppercase;
  color: #939da3;
  margin-left: unset;
}

#book-search-results > div.search-noresults > section.normal.markdown-section > p {
  text-align: justify;
}

body > div > div.book-summary > nav > ul > li:last-child {
  max-width: 300px;

}

body > div > div.book-summary > nav > ul > li:last-child > p {
  text-align: justify;
  padding-left: 16px;
  padding-right: 16px;
}

body > div > div.book-summary > nav > ul > li:last-child > a {
  margin-left: 30px;
  margin-right: 30px;
  padding-left: 0;
  padding-right: 0;
}

body > div > div.book-summary > nav > ul > li:last-child > a img {

  width: 240px;
}
```