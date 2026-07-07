# Scheda Misurazioni Serramenti

Applicazione web semplice per registrare misurazioni di serramenti, porte, balconi e avvolgibili.

Il programma funziona direttamente da browser e salva i dati in locale sul dispositivo tramite `localStorage`, senza bisogno di server, database o account utente.

## Funzionalità principali

* Gestione di più clienti.
* Inserimento dei dati del cliente:

  * nome e cognome;
  * data sopralluogo;
  * telefono;
  * email;
  * note.
* Gestione delle stanze, ad esempio cucina, soggiorno, camera, bagno.
* Inserimento di misurazioni per:

  * serramenti;
  * porte;
  * balconi;
  * avvolgibili.
* Misure espresse in millimetri.
* Campo quantità per indicare più elementi uguali.
* Possibilità di duplicare una misurazione già inserita.
* Esportazione e importazione backup in formato JSON.
* Generazione di una scheda stampabile / PDF tramite la funzione di stampa del browser.

## Tipologie di misurazione

### Serramenti

Per i serramenti è possibile indicare:

* larghezza;
* altezza;
* profondità;
* quantità;
* numero di ante:

  * 1 anta;
  * 2 ante;
* senso di apertura:

  * sinistra;
  * destra;
  * non specificato;
* presenza del cassonetto;
* misure del cassonetto:

  * larghezza;
  * altezza;
  * profondità;
* note relative al cassonetto;
* note generali.

### Porte

Per le porte è possibile indicare:

* larghezza;
* altezza;
* profondità;
* quantità;
* senso di apertura;
* note.

### Balconi

Per i balconi è possibile indicare:

* larghezza;
* altezza;
* profondità;
* quantità;
* tipo:

  * finestra;
  * porta-finestra;
* tipologia:

  * Vicentina;
  * Padovana;
  * Vic. Rovescia;
* senso di apertura;
* note.

### Avvolgibili

Per gli avvolgibili è possibile indicare:

* larghezza;
* altezza;
* profondità;
* quantità;
* note.

## Disegno apertura

Ogni misurazione può mostrare un disegno stilizzato del senso di apertura.

Il simbolo utilizzato è:

* `|>|` per apertura verso sinistra;
* `|<|` per apertura verso destra.

Le stanghette verticali rappresentano i bordi del serramento o della porta, mentre il simbolo centrale rappresenta il verso di apertura.

## Salvataggio dei dati

I dati vengono salvati nel browser tramite `localStorage`.

Questo significa che:

* i dati rimangono salvati sul dispositivo usato;
* non serve una connessione a internet dopo il caricamento della pagina;
* non viene usato un server esterno;
* se si cambia browser o dispositivo, i dati non vengono trasferiti automaticamente;
* cancellando i dati del browser si possono perdere le misurazioni salvate.

Per sicurezza è consigliato usare periodicamente la funzione **Esporta backup**.

## Backup

L’app permette di esportare tutti i dati in un file `.json`.

Il backup può essere successivamente importato per ripristinare clienti, stanze e misurazioni.

### Esportazione

Premere il pulsante:

```text
Esporta backup
```

Verrà scaricato un file JSON contenente tutti i dati salvati.

### Importazione

Premere il pulsante:

```text
Importa backup
```

e selezionare un file JSON precedentemente esportato.

Attenzione: importando un backup, i dati presenti nel browser vengono sostituiti.

## Stampa e PDF

Per ogni cliente è possibile generare una scheda riepilogativa tramite il pulsante:

```text
Scarica PDF
```

Il programma apre la schermata di stampa del browser. Da lì è possibile:

* stampare fisicamente la scheda;
* salvarla come PDF.

## Utilizzo con GitHub Pages

L’app è composta da un singolo file HTML.

Per pubblicarla con GitHub Pages:

1. Caricare il file `index.html` nella repository GitHub.
2. Attivare GitHub Pages dalle impostazioni della repository.
3. Selezionare il branch corretto, ad esempio `main`.
4. Aprire il link generato da GitHub Pages.

Quando si modifica il file `index.html`, il link rimane lo stesso. È sufficiente caricare la nuova versione del file nella repository.

Se le modifiche non compaiono subito, provare a:

* aggiornare la pagina con `Ctrl + F5`;
* aprire il sito in modalità incognito;
* aggiungere `?v=2` alla fine del link;
* verificare che il file modificato sia stato caricato nella repository corretta.

## Struttura del progetto

Il progetto può essere composto anche solo da:

```text
index.html
README.md
```

Non sono richieste installazioni, dipendenze o compilazioni.

## Requisiti

Per usare l’app è sufficiente un browser moderno, ad esempio:

* Google Chrome;
* Microsoft Edge;
* Safari;
* Firefox.

L’app può essere usata sia da PC che da smartphone o tablet.

## Note tecniche

L’applicazione è sviluppata con:

* HTML;
* CSS;
* JavaScript vanilla.

Non utilizza framework esterni per la logica principale e non richiede backend.

I dati vengono gestiti lato client e salvati nel browser dell’utente.

## Limitazioni

L’app non sincronizza automaticamente i dati tra dispositivi diversi.

Per spostare i dati da un dispositivo a un altro è necessario:

1. esportare il backup JSON dal primo dispositivo;
2. importare il backup JSON sul secondo dispositivo.

Inoltre, cancellando cache o dati del sito dal browser, le misurazioni salvate localmente potrebbero essere eliminate.

## Licenza

Progetto privato / personale.

L’utilizzo, la modifica e la distribuzione dipendono dalle esigenze del proprietario della repository.
