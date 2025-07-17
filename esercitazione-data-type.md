

La biblioteca comunale di “Città Libera” vuole creare un sistema per catalogare i libri presenti nei suoi archivi.

Per ogni libro, devono essere memorizzate le seguenti informazioni:


Il titolo del libro
Il nome dell’autore e il cognome dell’autore
Il codice ISBN, che è un identificativo univoco per ogni edizione del libro
La data di pubblicazione
La categoria del libro (es. romanzo, saggio, manuale, ecc.)
Il numero di pagine
Il prezzo di copertina
La lingua in cui è scritto il libro
L’editore
L’indicazione se è disponibile al prestito oppure solo consultazione in sede


identificare i tipi corretti e le informazioni rilevanti , costuire la tabella opportuna


Identifica i campi necessari per rappresentare un libro.

scegliere  per ciascun campo un data type appropriato in Oracle.

Progetta la tabella LIBRI, specificando:

I nomi dei campi

I tipi di dato Oracle

La chiave primaria

Eventuali vincoli utili (es. NOT NULL, CHECK, ecc.) cercare su google o con ia cosa significa not null , check ecc 






___________



---

### **Esercizio – Registro Dipendenti Azienda Tech**

L’azienda tecnologica “NextFuture S.p.A.” vuole creare una base dati per gestire le informazioni anagrafiche dei propri **dipendenti**.

Per ogni dipendente devono essere registrate le seguenti informazioni:

* Il **codice identificativo** del dipendente (univoco all’interno dell’azienda)
* Il **nome** e il **cognome**
* Il **codice fiscale**
* La **data di assunzione**
* Il **ruolo aziendale** (es. sviluppatore, analista, sistemista, HR, manager, ecc.)
* Il **dipartimento di appartenenza** (es. IT, Risorse Umane, Amministrazione, ecc.)
* Il **numero di telefono aziendale**
* L’**indirizzo email aziendale**
* Lo **stipendio mensile lordo**
* L’**indicazione se è attualmente in servizio** o meno

---

###  

1. Individuare i **campi** da inserire nella tabella `DIPENDENTI`.
2. Associare a ciascun campo un **tipo di dato Oracle** adeguato (`VARCHAR2`, `DATE`, `NUMBER`, `CHAR`, ecc.).
3. Progettare la **struttura della tabella**:

   * Nominare i campi in modo significativo
   * Definire la **chiave primaria**
   * Aggiungiungere eventuali **vincoli utili** (`NOT NULL`, `UNIQUE`, `CHECK`, ecc.)

---

```
 CREATE TABLE DIPENDENTI (
  ID_DIPENDENTE        NUMBER(5) PRIMARY KEY,
  NOME                 VARCHAR2(50) NOT NULL,
  COGNOME              VARCHAR2(50) NOT NULL,
  CODICE_FISCALE       CHAR(16) UNIQUE NOT NULL,
  DATA_ASSUNZIONE      DATE NOT NULL,
  RUOLO                VARCHAR2(40),
  DIPARTIMENTO         VARCHAR2(40),
  TELEFONO_AZIENDALE   VARCHAR2(15),
  EMAIL_AZIENDALE      VARCHAR2(100) UNIQUE,
  STIPENDIO_LORDO      NUMBER(8,2) CHECK (STIPENDIO_LORDO >= 0),
  IN_SERVIZIO          CHAR(1) DEFAULT 'S' CHECK (IN_SERVIZIO IN ('S', 'N'))
);
```



---


###  **Esercizio – Archivio Film di una Videoteca**

La videoteca “CineMania” vuole creare un database per gestire l’archivio dei **film** disponibili per il noleggio.

Per ogni film devono essere memorizzate le seguenti informazioni:

* Un **codice identificativo** univoco del film
* Il **titolo del film**
* Il **nome del regista**
* L’**anno di uscita**
* La **durata** del film in minuti
* Il **genere** (es. commedia, azione, drammatico, horror, ecc.)
* Il **prezzo di noleggio**
* L’**indicazione se è disponibile o no**
* Il **numero di copie disponibili**
* La **lingua originale**

---




---






###  **Esercizio – Registro Prenotazioni Alberghiere**

L’hotel “Stella Marina” vuole creare un sistema per registrare le **prenotazioni** effettuate dai clienti.

Per ogni **prenotazione** si vogliono memorizzare le seguenti informazioni:

* Un **codice identificativo** della prenotazione (univoco)
* Il **nome** e il **cognome** del cliente
* La **data di arrivo**
* La **data di partenza**
* Il **numero di ospiti**
* Il **tipo di camera** richiesta (singola, doppia, tripla, suite)
* Se il cliente ha richiesto la **colazione inclusa** (sì/no)
* L’**importo totale della prenotazione**
* L’**email di contatto** del cliente
* Lo **stato della prenotazione** (confermato, annullato, in attesa)

---



---























