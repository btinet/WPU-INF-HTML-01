# Software Life Cycle

[Zurück zur Übersicht](../README.md)

1.  [Einführung](#einfhrung)

## Einführung
SLC steht für Software Life Cycle

1. Produktdefinition, Anforderungen definieren (menschliche Sprache ungenau)
2. Modellierung (Strukturgramme, ERM, UML)
   1. Durch das Modellieren werden die Anforderungsdefinitionen präzisiert
3. Programmieren
4. Implemention, Warten, Erweitern

## Javascript Beispiel
### Anforderungsdefinition
Es soll eine Website erstellt werden.
- Es soll eine Passwortabfrage realisiert werden.
- Das Passwort soll dabei "Traumtaenzer" sein.
- nach der erfolgreichen Eingabe soll der User auf eine geheime Seite weitergeleitet werden.

### Modellierung
1. Kontrollstruktur
   1. Zweiseitig (true/false)

````javascript
(function () {

   // Definiere alle Elemente

   let $buttons = document.querySelectorAll('#age-form .age-button');              // Alle Abfrage-Buttons
   let $passwordInput = document.querySelector('#password-input');                 // Passwort-Division
   let $passwordResult = document.querySelector('#password-result');               // Passwort Warntext
   let $passwordInputField = document.querySelector('#password');                  // Passwort Input
   let $passwordSubmitButton = document.querySelector('.password-submit-button');  // Passwort Submit Button

   let $secret = "traumtaenzer";                                                   // Geheimes Passwort

   Array.prototype.slice.call($buttons)                                    // Alle Buttons verarbeiten
       .forEach(function ($button) {                                       // für jeden Button...
           $button.addEventListener ('click', function (evt) {             // Mausklick abhören
               evt.preventDefault();                                       // Standardverhalten stoppen
               if(JSON.parse($button.value)){                              // Wenn "Ja"...
                   $passwordInput.setAttribute('style','');                // Passwort-Div zeigen
           } else {                                                        // ansonsten...
                   $passwordInput.setAttribute('style','display: none');   // Passwort-Div verbergen
               }
           });
       })

   $passwordSubmitButton.addEventListener ('click', function (evt) {       // Passwort-Submit-Button abhören
       evt.preventDefault();                                               // Standardverhalten unterbinden
       if($passwordInputField.value !== ""){                               // Wenn Eingabe nicht leer
           if($secret === $passwordInputField.value){                      // Wenn Passwort korrekt
               $passwordSubmitButton.innerHTML = "Bitte warten";           // Text auf Submit-Button ändern
               setTimeout(function (){                                     // zwei Sekunden warten
                   document.location.href="./tabellen.html";               // Auf geheime Seite weiterleiten
               },2000);
           } else {                                                        // ...ansonsten...
               $passwordResult.innerHTML =                                 // Auf falsches Passwort hinweisen
                   "Dein Passwort lautet: <span class='text-primary'>"
                   + $passwordInputField.value
                   +"</span>.<br>Dies ist leider falsch!";
           }
       }
   })

})()
````

Zeile 8)
Eine zweiseitige Kontrollstruktur wird begonnen.
Die Bedingung ist dann erfüllt (wahr),
wenn die Variable "Eingabe" ungleich "Passwort" (ohne Typenprüfung).