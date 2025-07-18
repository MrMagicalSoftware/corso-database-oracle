

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

```

CREATE TABLE ARCHIVIO_FILM (

  CODICE_IDENTIFICATIVO          NUMBER(10) PRIMARY KEY,
  TITOLO                         VARCHAR2(50) NOT NULL,
  NOME_REGISTA                   VARCHAR2(50) NOT NULL,
  ANNO_DI_USCITA                 DATE,
  DURATA                         NUMBER(3),
  GENERE                         VARCHAR2(50),
  PREZZO_NOLEGGIO                NUMBER(5, 2 ) CHECK (PREZZO_NOLEGGIO > 0 ),
  DISPONIBILE                    CHAR(1) DEFAULT 'S' CHECK (DISPONIBILE IN ('S', 'N')),
  COPIE_DISPONIBILI              NUMBER(3),
  LINGUA                         VARCHAR2(40)

);
```



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

```
CREATE TABLE PRENOTAZIONI (
  ID_PRENOTAZIONE      NUMBER(6) PRIMARY KEY,
  NOME_CLIENTE          VARCHAR2(50) NOT NULL,
  COGNOME_CLIENTE       VARCHAR2(50) NOT NULL,
  DATA_ARRIVO           DATE NOT NULL,
  DATA_PARTENZA         DATE NOT NULL,
  NUMERO_OSPITI         NUMBER(2) CHECK (NUMERO_OSPITI > 0),
  TIPO_CAMERA           VARCHAR2(20) CHECK (TIPO_CAMERA IN ('singola', 'doppia', 'tripla', 'suite')),
  COLAZIONE_INCLUSA     CHAR(1) DEFAULT 'N' CHECK (COLAZIONE_INCLUSA IN ('S', 'N')),
  IMPORTO_TOTALE        NUMBER(8,2) CHECK (IMPORTO_TOTALE >= 0),
  EMAIL_CLIENTE         VARCHAR2(100),
  STATO                 VARCHAR2(20) DEFAULT 'in attesa'
    CHECK (STATO IN ('confermato', 'annullato', 'in attesa'))
);

```
---



---

###  **Esercizio – Archivio Veicoli di un’Officina Meccanica**

L’officina “Motori\&Service” vuole creare un archivio per registrare i **veicoli dei clienti** che vengono portati per assistenza o manutenzione.

Per ogni **veicolo** devono essere memorizzate le seguenti informazioni:

* Un **codice identificativo** del veicolo (univoco)
* La **targa**
* La **marca** (es. Fiat, BMW, Toyota, ecc.)
* Il **modello**
* L’**anno di immatricolazione**
* Il **tipo di alimentazione** (benzina, diesel, elettrico, ibrido, GPL)
* Il **chilometraggio attuale**
* Il **nome del proprietario**
* Il **numero di telefono** del proprietario
* L’**indicazione se il veicolo è ancora in riparazione**

---

```
CREATE TABLE VEICOLI (
  ID_VEICOLO            NUMBER(6) PRIMARY KEY,
  TARGA                 VARCHAR2(10) UNIQUE NOT NULL,
  MARCA                 VARCHAR2(30) NOT NULL,
  MODELLO               VARCHAR2(30) NOT NULL,
  ANNO_IMMATRICOLAZIONE NUMBER(4) CHECK (ANNO_IMMATRICOLAZIONE >= 1980),
  ALIMENTAZIONE         VARCHAR2(10)
    CHECK (ALIMENTAZIONE IN ('benzina', 'diesel', 'elettrico', 'ibrido', 'GPL')),
  CHILOMETRAGGIO         NUMBER(7) CHECK (CHILOMETRAGGIO >= 0),
  NOME_PROPRIETARIO      VARCHAR2(60) NOT NULL,
  TELEFONO_PROPRIETARIO  VARCHAR2(15),
  IN_RIPARAZIONE         CHAR(1) DEFAULT 'N' CHECK (IN_RIPARAZIONE IN ('S', 'N'))
);

```
---


















