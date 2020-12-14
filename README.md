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

![use cases](UML/UseCaseDiagram1.jpg)

## **Scenari**

| Caso d'uso : Prendere medicine |
| :----------------------------- |
| **Attori**: Paziente, Hardware, Server |
| **Precondizioni**  <ol><li>Il caso d'uso inizia quando l'orario è prossimo all'ora dell'assunzione del medicinale</ol>|
| **Sequenza degli eventi** <ol><li>Il paziente clicca il pulsante per aprire il cassetto e prendere la medicina</ol>|
| **Post condizioni** <ol><li> L'assunzione è stata registrata sul server</ol>|
| **Sequenza alternativa 1** <ol><li>Il paziente non clicca il pulsante per prendere la medicina</ol>|
| **Post condizioni**  <ol><li>La non assunzione è stata registrata sul server</li><li>Il familiare viene notificato della non assunzione</ol>|
| **Sequenza alternativa 2** <ol><li>La medicina non è presente</li><li>Clicca pulsante emergenza</ol>|
| **Post condizioni** <ol><li>La non assunzione è stata registrata sul server</li><li>Il familiare viene avvisato con una notifica di urgenza</ol>|


| Caso d'uso : Rifornimento medicinali |
| :----------- |
| **Attori**: Farmacia, Familiare, Hardware, Server  |
| **Precondizioni**  <ol><li>Notifica di manutenzione da parte dell'app</ol>|
| **Sequenza degli eventi** <ol><li>Il familiare apre il cassetto tramite app</li><li>Conferma il rifornimento dei medicinali tramite app</ol>|
| **Post condizioni** <ol><li> Aggiornamento inventario da parte del server</ol>|
| **Sequenza alternativa 1** <ol><li>Prenotazione medicinali</li><li>Il familiare apre il cassetto tramite app</li><li>Conferma il rifornimento dei medicinali tramite app</ol>|
| **Post condizioni**  <ol><li>Aggiornamento inventario da parte del server</ol>|

| Caso d'uso : Aggiunta di una ricetta medica | 
| :----------- |
|**Attori**: Medico, Server, Familiare,     |
|**Precondizioni** <ol><li>Login nell'applicazione da parte del medico</ol> |
|**Sequenza degli eventi** <ol><li>Il dottore crea la ricetta</li><li>Il server carica la ricetta</li><li>Il server fa un controllo sull'inventario</li><li>Se necessario il server aggiorna l'inventario</li></ol>|
|**Post condizioni** <ol><li>Al familiare del paziente viene notificato il caricamento della ricetta</li><li>Il familiare decide se esportare la ricetta in pdf o mandarla via mail alla farmacia</li><li>Si passa al caso d'uso in cui viene effettuata la prenotazione dei medicinali</li></ol>|
|**Sequenza alternativa 1** <ol><li>Il dottore crea la ricetta</li><li>Il server carica la ricetta</li><li>Il server fa un controllo sull'inventario</li><li>Se necessario il server aggiorna l'inventario</li><li>il familiare non vede la notifica della ricetta</li></ol>|
|**Post condizioni** <ol><li>Al familiare viene ripetuta la notifica ogni 5 minuti finché non la visulizza</li><li>Il familiare decide se esportare la ricetta in pdf o mandarla via mail alla farmacia</li><li>Si passa al caso d'uso in cui viene effettuata la prenotazione dei medicinali</li></ol>|

## **Diagramma delle classi**

![DC](UML/ClassDiagram1.jpg)

 <!---
 Manca cio che ha detto il committente
 scarno di informazioni
 dettagliare meglio

 ricetta/farmaco come classe e attributi

 iniziare a fare sequenza 
-->


## **Sequence diagrams**

### *Rifornimento medicinali*

![sd rifornimento medicinale](UML/rifornimentomedicinali.jpg)