# Progetto ingegneria del software - pilly

## **Idea del progetto**

Il sistema consiste in un applicazione che ha l'obiettivo di monitorare e aiutare pazienti anziani che hanno bisogno di assumere quantità precise e in maniera regolare di farmaci.
Il sistema dovrà notificare al paziente quando assumere i medicinali in base alla ricetta caricata sul server da parte del medico curante.
La notifica avviene tramite un sistema hardware composto da led, display e vani contenenti medicinali che si apriranno automaticamente, o manualmente dal paziente oppure da un qualsiasi utente, tramite applicazione.
L'applicazione interagisce con un server che hai il compito di memorizzare la quantità e la frequenza riguardo le assunzioni dei medicinali.
Il sistema può interagire con una farmacia con lo scopo di prenotare i medicinali per il rifornimento.

<!---
Tabella per descrivere i requisiti funzionali, descrizione non troppo dettagliata
-->

<!---### **Specifica dei requisiti**

| requisiti funzionali | Descrizione |
| ---------------------| ----------- |
| esempio | prova |
| a | b |

-->

<!---
Qui andrà l'uml dei casi d'uso
-->

<!---
TODO: aprire cassetto dall'app
-->

## **Use cases diagram**

![use cases](https://raw.githubusercontent.com/piconepaolo/pilly/main/UML/UseCaseDiagram1.jpg?token=AI3QDBQZYOXC66AWGNVJDCC73CXZK)

## **Scenari**

| Caso d'uso : Prendere medicine |
| :----------------------------- |
| **Attori**: Paziente, Hardware, Server |
| **Precondizioni**  <ol><li>Il caso d'uso inizia quando l'orario è prossimo all'ora dell'assunzione del medicinale</ol>|
| **Sequenza degli eventi** <ol><li>Il paziente clicca il pulsante per aprire il cassetto e prendere la medicina</ol>|
| **Post condizioni** <ol><li> L'assunzione è stata registrata sul server</ol>|
| **Sequenza alternativa 1** <ol><li>Il paziente non clicca il pulsante per prendere la medicina</ol>|
| **Post condizioni**  <ol><li>La non assunzione è stata registrata sul server</li><li>Il familiare viene notificato della non assunzione</ol>|
| **Sequenza alternativa 2** <ol><li>La medicina non è presente</li><li>clicca pulsante emergenza</ol>|
| **Post condizioni** <ol><li>La non assunzione è stata registrata sul server</li><li>Il familiare viene avvisato con una notifica di urgenza</ol>|


| Caso d'uso : Prenotazione medicinali |
| :----------- |
| **Attori**: Farmacia, Familiare, Hardware, Server  |
| **Precondizioni**  <ol><li>Notifica di manutenzione da parte dell'app</ol>|
| **Sequenza degli eventi** <ol><li>Il familiare apre il cassetto tramite app</li><li>Conferma il rifornimento dei medicinali tramite app</ol>|
| **Post condizioni** <ol><li> Aggiornamento inventario da parte del server</ol>|
| **Sequenza alternativa 1** <ol><li>Clicca il pulsante sull'app per il rifornimento dei medicinali da parte della farmacia</li><li>Il familiare apre il cassetto tramite app</li><li>Conferma il rifornimento dei medicinali tramite app</ol>|
| **Post condizioni**  <ol><li>Aggiornamento inventario da parte del server</ol>|




 