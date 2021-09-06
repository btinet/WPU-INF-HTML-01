# CSS

[Zurück zur Übersicht](../README.md)

1.  [Entstehung](#entstehung)
2.  [Trennung von Inhalt und Design](#trennung-von-inhalt-und-design)
3.  [Aufbau von CSS](#aufbau-von-css)
4.  [CSS in HTML einbinden](#css-in-html-einbinden)

## Entstehung
Das World Wide Web Konsortium (W3C) entwickelte CSS, um zum ursprünglichen
Grundgedanken von HTML zurückzukehren: die Trennung der Informationen von der
Präsentation. Ohne CSS ist HTML für Inhalt, Struktur und Aussehen zuständig. Ein
aufgeblähter und unübersichtlicher Code entsteht.

## Trennung von Inhalt und Design
Ein extrem großer Vorteil von CSS ist die Trennung des eigentlichen Inhalts vom
Design. Das Design wird in eine eigene Datei ausgelagert und kann für alle Seiten
eines Internetauftritts verwendet werden. Werden Änderungen am Design gemacht,
sind durch eine Datei sofort alle Einzelseiten up to date.

## Aufbau von CSS
CSS-Dokumente stellen eine Art Liste dar, in der definiert ist, welche HTML-Elemente wie aussehen sollen.
Dies geschieht nach folgendem Muster:

**Selector { Eigenschaft1:Wert; Eigenschaft2: Wert; }**

Beispiel:

````css
h1 { color:red; font-size:48px; }
````
Im obigen Beispiel haben alle Überschriften **h1** eine **rote Textfarbe** und eine **Schriftgröße von 48px**.

### Selektor:

Als **Selektoren** wird das bezeichnet, was vor den geschweiften Klammern steht. Ein
Selektor wählt aus, wofür die folgenden Definitionen gelten sollen. Im obigen Beispiel
gelten die Formate für alle Überschriften 1. Ordnung (h1-Elemente). Es sind jedoch
auch komplexere Selektoren möglich sowie mehrere, durch Komma getrennte
Selektoren.

### Definitionen:

Die eigentlichen Definitionen zum Format stehen stets in geschweiften Klammern
``{`` und ``}``. Sie bestehen darin, dass eine oder mehrere CSS-Eigenschaften notiert
werden und einen Wert erhalten. Im obigen Beispiel werden etwa die CSS-Eigenschaften
color (Schriftfarbe) und font-size (Schriftgröße) verwendet. Der
Eigenschaft color wird der Wert red zugewiesen, und der Eigenschaft font-size der Wert
48px. Zwischen Eigenschaft und Wertzuweisung muss stets ein Doppelpunkt stehen.
Abgeschlossen wird eine Definition mit einem Strichpunkt ``;``. Nur bei der letzten
Definition vor der schließenden geschweiften Klammer darf der Strichpunkt auch
entfallen.

##  CSS in HTML einbinden

### Direkt im Quellcode

### Im HTML-Kopf

### Ausgelagert