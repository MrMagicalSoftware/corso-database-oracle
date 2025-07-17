

 principali **data type (tipi di dato)** in **Oracle Database**

---

### 1. **Numerici**

| Tipo          | Descrizione                           | Esempio di dichiarazione         |
| ------------- | ------------------------------------- | -------------------------------- |
| `NUMBER(p,s)` | Numero con precisione `p` e scala `s` | `SALARIO NUMBER(8,2)` → 12345.67 |
| `INTEGER`     | Alias per `NUMBER(38)`                | `ETA INTEGER`                    |
| `FLOAT(p)`    | Numero in virgola mobile              | `PERCENTUALE FLOAT(10)`          |

**Esempio d’uso**:

```sql
CREATE TABLE dipendenti (
  id NUMBER(5),
  stipendio NUMBER(10,2),
  eta INTEGER
);
```

---

###  2. **Caratteri (stringhe)**

| Tipo           | Descrizione                                | Esempio di dichiarazione |
| -------------- | ------------------------------------------ | ------------------------ |
| `CHAR(n)`      | Stringa a lunghezza **fissa**              | `SESSO CHAR(1)`          |
| `VARCHAR2(n)`  | Stringa a lunghezza **variabile**          | `NOME VARCHAR2(50)`      |
| `NCHAR(n)`     | Come `CHAR`, ma supporta caratteri Unicode | `LINGUA NCHAR(2)`        |
| `NVARCHAR2(n)` | Come `VARCHAR2`, ma con Unicode            | `NAZIONE NVARCHAR2(30)`  |

**Esempio d’uso**:

```sql
CREATE TABLE clienti (
  nome VARCHAR2(100),
  codice CHAR(5),
  lingua NCHAR(2)
);
```

---

###  3. **Data e ora**

| Tipo                       | Descrizione                            | Esempio di dichiarazione            |
| -------------------------- | -------------------------------------- | ----------------------------------- |
| `DATE`                     | Data e ora (fino al secondo)           | `DATA_NASCITA DATE`                 |
| `TIMESTAMP`                | Data e ora con frazione di secondo     | `CREATO_IL TIMESTAMP`               |
| `TIMESTAMP WITH TIME ZONE` | Con fuso orario                        | `LOGIN_TS TIMESTAMP WITH TIME ZONE` |
| `INTERVAL`                 | Durata (es. giorni, ore, minuti, ecc.) | `DURATA INTERVAL DAY TO SECOND`     |

 **Esempio d’uso**:

```sql
CREATE TABLE eventi (
  nome VARCHAR2(100),
  data_inizio DATE,
  durata INTERVAL DAY TO SECOND
);
```

---

###  4. **Booleani** (non nativi, ma simulabili)

Oracle **non ha un tipo BOOLEAN** nelle tabelle SQL standard, ma si può simulare con `CHAR(1)` o `NUMBER(1)`:

 **Esempio d’uso simulato**:

```sql
CREATE TABLE utenti (
  id NUMBER,
  attivo CHAR(1)  -- 'S' o 'N'
);
```

---

###  5. **LOB (Large Objects)**

| Tipo    | Descrizione                           | Esempio di dichiarazione |
| ------- | ------------------------------------- | ------------------------ |
| `CLOB`  | Testo di grandi dimensioni            | `TESTO CLOB`             |
| `BLOB`  | Dati binari (es. immagini, PDF, ecc.) | `IMMAGINE BLOB`          |
| `NCLOB` | Come `CLOB`, ma per Unicode           | `DESCRIZIONE NCLOB`      |
| `BFILE` | File binari esterni                   | `ALLEGATO BFILE`         |

 **Esempio d’uso**:

```sql
CREATE TABLE documenti (
  id NUMBER,
  contenuto CLOB,
  immagine BLOB
);
```

---

###  6. **Tipo ROWID e UROWID**

| Tipo     | Descrizione                                              |
| -------- | -------------------------------------------------------- |
| `ROWID`  | Indirizzo fisico di una riga in una tabella              |
| `UROWID` | Indirizzo logico (utile con tabelle con index-organized) |

 **Esempio**:

```sql
SELECT ROWID, nome FROM clienti;
```

---

