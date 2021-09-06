# HTML

[Zurück zur Übersicht](../README.md)

1. [HTML Grundlagen](#html-grundlagen)
2. [Head](#head)
3. Body

## HTML Grundlagen
HTML steht für ``Hypertext Markup Language`` und stellt damit eine grundlegende Auszeichnungssprache für die formatierte Darstellung von textbasierten Inhalten in Webbrowsern dar.

Im Folgenden beschäftigen wir uns mit dem grundlegenden Aufbau einer [HTML-Datei](../index.html):
```html
<!-- index.html /-->
<html>
    <head>
        <meta charset="UTF-8">
        <title>Dokumententitel</title>
    </head>
    <body>
        <h1>Tabellenüberschrift</h1>
        <p>Absatz</p>
    </body>
</html>
```
Das Beispiel zeigt das minimal erforderliche Gerüst einer HTML-Datei. Grundsätzlich ist der Aufbau recht simpel. Schauen wir uns zunächst die erste Zeile an:

```html
<!DOCTYPE html>
```
Dies teilt dem Browser oder Server lediglich mit, das es sich um den Dokumententyp ``html`` handelt. Denkbar wären hier auch noch andere Formate wie ``xml``.

Alle weiteren Elemente einer html-Datei werden innerhalb des ``<html>``-Tags geschrieben.
````html
<!DOCTYPE html>
<html lang="de">

Hier landet der Inhalt.

</html>
````
Ein HTML-Tag besteht immer aus zwei Teilen, dem ``öffnenden`` und dem ``schließenden`` Teil. Allerdings gibt es auch hier Ausnahmen. Das ``<meta>``-Tag stellt eine davon dar. Wie du gesehen hast, hat es nämlich kein schließendes Tag ``</meta>``, sondern folgendes Schema: ``<meta />``

Allerdings darf das /-Zeichen auch weggelassen werden, also ``<meta name="a" content="b">``

Zwischen ``<html>`` und ``</html>`` (Innerhalb des <html>-Tags), werden wir zwei Bereiche erstellen:

1. Head - Die "Meta-Ebene"
2. Body - Die "visuelle Ebene"

Wir schauen uns zuerst den ``HTML-Kopf`` an.

## Head
