## Theming

Unter dem Begriff Theming ist in diesem Kontext die Anpassung des Layouts der Webansicht bzw. des PDFs gemeint. Das hier verwendete Theme ist das standarmäßige Theme von Gitbook. Alle dafür notwendigen Dateien sind im Ordner `_layouts/` zu finden. In Besonderem ist dort die Datei `layout.html` gespeichert, welche das grundlegende Layout überschreibt. Weiter unterteilt sich die Struktur in die Ordner `ebook` und `website`, welche weitere spezifischere Anpassungen gegenüber dem Layout vornehmen können. Darin kann über die Dateien `page.html`, `summary.html`, `layout.html`, `languages.html` und `header.html` der Aufbau der einzelnen Komponenten angepasst werden. 

Für das in diesem Projekt umgesetzte Theme wurde nur die Datei `summary.html` angepasst. Sie ist für das Navigationsmenü auf der linken Seite verantwortlich. Darin wurden Gitbook spezifische Informationen herausgenommen und z.B. durch Hinweise auf die Hochschule ersetzt.


!CAPTION Anpassung innerhalb der `summary.html`
```html
    ...

    <li>
        <p>Enstanden im Rahmen einer <br/>Lehrveranstaltung der Hochschule Coburg.</p>
        <a href="https://hs-coburg.de" target="blank" class="gitbook-link">
          <img src="https://www.hs-coburg.de/typo3conf/ext/in2template/Resources/Public/Images/hochschule-coburg_logo.png"/>
        </a>
    </li>
    ...
```