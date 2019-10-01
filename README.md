


    - Diese Seite ist "work in progress" - 


# Hands on - Open Data

*Unterlagen zum Workshop "Hands on - Open Data"*

# Ressourcen / Links

* TBD:
* Wollen wir hier auf einzelne Open Data Portale verlinken? Besser auf fertige Linklisten zu Open Data Portalen. Aber welches ist die ultimative „Open-Data-Startseite bzw Linkliste?“?
* Folien verlinken
* Folien "Was ist Open Data": [https://codeformuenster.org/codeforosna-opendata-slides/](https://codeformuenster.org/codeforosna-opendata-slides/). Quelltext: [https://github.com/codeformuenster/codeforosna-opendata-slides](https://github.com/codeformuenster/codeforosna-opendata-slides)


# Workshop-Inhalte

Wir wollen an Beispielen zeigen, wie man „kleine“ Datensätze visualisieren kann. Dazu nutzen wir „komfortable“, frei im Internet verfügbare, interaktive Werkzeuge. Es werden keine Programmierkenntnisse benötigt. 

## Datenaufbereitung

Im Workshop wollen wir eher „kleine“ Datensätze visualisieren, d.h. konkret: Tabellen mit weniger als 10 Spalten, und maximal 5000 Zeilen.

Die meisten Online-Tools benötigen einen „sauberen“ tabellarischen Datensatz: In der ersten Zeile stehen die Titel, und in den restlichen Zeilen stehen die Daten. 

Zum Aufbereiten der zu visualisierenden Daten kann man gut LibreOffice oder Excel verwenden. Die Daten sollten dann z.B. folgendermaßen aussehen: 

| Code        | Name          | Betrag |
| ----------- | ------------- | ------ |
| 501305      | right-aligned |   1600 |
| 502030      | centered      |    122 |
| 500331      | are neat      |    500 |
| ...         | ...etc...     |    ... |

## Teil 1: Statistische Daten aus Deutschland visualisieren

Im ersten Schritt wollen wir mit Daten aus der **Regionaldatenbank Deutschland** arbeiten: \
www.regionalstatistik.de

Dort gibt es viele statistische Informationen aus den unterschiedlihsten Themenbereichen.
regionalstatistik.de kann z.B. über den Menüpunkt "Themen" (linke Seite) durchsucht werden. 

Alternativ nutzen Sie den Regio-Stat-Katalog: \
https://www.statistikportal.de/sites/default/files/2019-02/Regio-Stat-Katalog2019.pdf \
Nutzen Sie dort jeweils den "Link zur Regionaldatenbank" um zum Datenabruf zu gelangen.

Hinweise zu Regionalstatistik.de:
 * Auf keinen Fall den "zurück"-Button vom Browser verwenden! :( Die Seite vergisst sonst, wo man gerade war, und man muss wieder von vorne starten.
  
Hinweise zum Datenabruf: 
 * Daten sind generell auf Kreis-Ebene abrufbar
 * "regionale Tiefe: Kreise und krfr. Städte" => Enthält auch die aggregierten Daten (Regionen, Bundesländer). Wenn man Daten nur eines Bundeslandes (z.B. NRW) visualisieren möchte, dann kann man hier das Bundesland auswählen, um Daten zu allen Kreise in diesem Bundesland zu erhalten.
 * "regionale Ebenen" => Enthält nur die Kreisebene, Filtern nach Bundesland ist hier nicht so einfach.
 * Filtern kann man über das Feld "Code", dort kann gesucht werden per AGS (Amtlicher Gemeindeschlüssel): Siehe z.B. https://de.wikipedia.org/wiki/Amtlicher_Gemeindeschl%C3%BCssel
 
## Teil 2: Visualisierung von Daten mit interaktiven Online-Tools

Es gibt einige Online- bzw. Cloud-Tools, die das Erstellen von einfachen Visualisierungen ohne Programmierkenntnisse ermöglichen (Choropleten-Karten, Balkendiagramme, etc).

Wir empfehlen derzeit folgende Tools:
* https://plot.ly – Benutzung komplett ohne Registrierung möglich. Auf der Webseite oben auf „Products → Chart Studio“ und dann den Button „Try open source“. Man kann sein Diagramm komfortabel online erstellen, und entweder online teilen und z.B. in Webseiten einbetten, oder man kann die Metadaten des Diagramms herunterladen, und dann u.a. mit der Bibliothek für Python weiterverwenden (https://github.com/plotly/plotly.py)
* https://datawrapper.de - Eignet sich inbesondere für Datensätze von Regionalstatistik.de, da es eine Visualisierung anhand des amtlichen Gemeindeschlüssels (AGS) unterstützt. Dazu muss man sich allerdings erst bei datawrapper.de online registrieren, ansonsten ist die Funktion zum Erstellen von Kartenbasierten Visualisierungen deaktiviert.

Eine sehr gute Übersicht visueller Tools gibt es unter: 
* https://dataviz.tools/category/interactive-charting/ <- Dort sind jedoch auch einige dabei, für die man programmieren muss.
* https://datentaeter.de/cheatsheet-programmierlose-ddj-tools/

## Teil 3: Komplexere Online-Tools zum Erstellen von Diagrammen

* TBD


## Teil 4: Darstellung anderer Datenformate (keine Excel/CSV Tabellen)

**GEOJSON**
* Man nehme eine geojson Datei (z.B. vom Open-Data-Portal der Stadt Münster)
* Geojson anschauen: http://geojson.io
  (einfach geojson per „copy und paste“ einfügen)
* Wenn man die Geojson-Punkte filtern möchte: http://www.jsonquerytool.com
* Die gefilterten Ergebnisse dann wieder anschauen mit (2.)
  * Man kann zusätzlich bei einzelnen Punkten als „properties“ dazuschreiben: 
    marker-color: #B1AB1A
    ..dann wird der Marker in einer anderen Farbe dargestellt (Ist Teil vom geojson standard)
* Veröffentlichen: Als Github gist einfach das geojson reinkopieren. Github zeigt geojson automatisch als Karte an und man kann auf die Punkte draufklicken und bekommt die Properties als popup angezeigt.

