
# COSA MI SERVE ?

Ecco un esempio pratico di come utilizzare Telnet per testare la connettività a porte specifiche su un server.

## 🛠️ Esempio di Diagnostica di Rete con Telnet

### 🔍 Scenario
Immagina di voler verificare se un server web (ad esempio, `example.com`) è raggiungibile sulla porta 80 (HTTP) e sulla porta 443 (HTTPS).

### 🖥️ Comandi Telnet

1. **Aprire il Terminale**: Avvia il terminale sul tuo computer.

2. **Testare la Porta 80 (HTTP)**:
   - Esegui il seguente comando:
     ```
     telnet example.com 80
     ```
   - Se la connessione ha successo, vedrai un messaggio che indica che sei connesso. Puoi anche inviare una richiesta HTTP di base digitando:
     ```
     GET / HTTP/1.1
     Host: example.com
     ```
   - Premi `Invio` due volte per inviare la richiesta. Se ricevi una risposta dal server, significa che la porta 80 è aperta e funzionante.

3. **Testare la Porta 443 (HTTPS)**:
   - Esegui il seguente comando:
     ```
     telnet example.com 443
     ```
   - Se la connessione ha successo, vedrai un messaggio di connessione. Tuttavia, poiché HTTPS utilizza la crittografia, non potrai inviare una richiesta HTTP come nel caso della porta 80. Se non riesci a connetterti, potrebbe significare che la porta 443 è chiusa o che il server non è configurato correttamente.

### 📊 Interpretazione dei Risultati
- **Connessione Riuscita**: Se riesci a connetterti a una porta, significa che il server è attivo e la porta è aperta.
- **Connessione Fallita**: Se ricevi un messaggio di errore come "Connection refused" o "Could not open connection", significa che la porta è chiusa o il server non è raggiungibile.

