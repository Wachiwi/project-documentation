## Theming

Unter dem Begriff Theming ist in diesem Kontext die Anpassung des Layouts der Webansicht bzw. des PDFs gemeint. Das hier verwendete Theme ist das standarmäßige Theme von Gitbook. Alle dafür notwendigen Dateien sind im Ordner `_layouts/` zu finden. In Besonderem ist dort die Datei `layout.html` gespeichert, welche das grundlegende Layout überschreibt. Weiter unterteilt sich die Struktur in die Ordner `ebook` und `website`, welche weitere spezifischere Anpassungen gegenüber dem Layout vornehmen können. Darin kann über die Dateien `page.html`, `summary.html`, `layout.html`, `languages.html` und `header.html` der Aufbau der einzelnen Komponenten angepasst werden. 

Für das in diesem Projekt umgesetzte Theme wurde nur die Datei `summary.html` angepasst. Sie ist für das Navigationsmenü auf der linken Seite verantwortlich.


```html
{% macro articles(_articles) %}
    {% for article in _articles %}
        <li class="chapter {% if article.path == file.path and not article.anchor %}active{% endif %}" data-level="{{ article.level }}" {% if article.path %}data-path="{{ article.path|resolveFile }}"{% endif %}>
            {% if article.path and getPageByPath(article.path) %}
                <a href="{{ article.path|resolveFile }}{{ article.anchor }}">
            {% elif article.url %}
                <a target="_blank" href="{{ article.url }}">
            {% else %}
                <span>
            {% endif %}
                    {% if article.level != "0" and config.pluginsConfig['theme-default'].showLevel %}
                        <b>{{ article.level }}.</b>
                    {% endif %}
                    {{ article.title }}
            {% if article.path  or article.url %}
                </a>
            {% else %}
                </span>
            {% endif %}

            {% if article.articles.length > 0 %}
            <ul class="articles">
                {{ articles(article.articles, file, config) }}
            </ul>
            {% endif %}
        </li>
    {% endfor %}
{% endmacro %}

<ul class="summary">
    {% set _divider = false %}
    {% if config.links.sidebar  %}
    {% for linkTitle, link in config.links.sidebar  %}
        {% set _divider = true %}
        <li>
            <a href="{{ link }}" target="_blank" class="custom-link">{{ linkTitle }}</a>
        </li>
    {% endfor %}
    {% endif %}

    {% if _divider %}
    <li class="divider"></li>
    {% endif %}

    {% for part in summary.parts %}
        {% if part.title %}
        <li class="header">{{ part.title }}</li>
        {% elif not loop.first %}
        <li class="divider"></li>
        {% endif %}
        {{ articles(part.articles, file, config) }}
    {% endfor %}

    <li class="divider"></li>

    <li>
        <p>Enstanden im Rahmen einer <br/>Lehrveranstaltung der Hochschule Coburg.</p>
        <a href="https://hs-coburg.de" target="blank" class="gitbook-link">
          <img src="https://www.hs-coburg.de/typo3conf/ext/in2template/Resources/Public/Images/hochschule-coburg_logo.png"/>
        </a>
    </li>
</ul>
```