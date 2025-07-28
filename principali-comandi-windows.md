
---

### 🔍 **Diagnostica e test**

| Comando         | Descrizione                                                  |
| --------------- | ------------------------------------------------------------ |
| `ping`          | Verifica la raggiungibilità di un host.                      |
| `tracert`       | Traccia il percorso dei pacchetti verso una destinazione.    |
| `nslookup`      | Interroga i server DNS per risolvere nomi.                   |
| `pathping`      | Combina `ping` e `tracert` con statistiche avanzate.         |
| `netstat`       | Mostra connessioni attive, porte in ascolto e statistiche.   |
| `arp -a`        | Visualizza la tabella ARP (IP ↔ MAC).                        |
| `ipconfig`      | Mostra la configurazione IP delle interfacce.                |
| `ipconfig /all` | Mostra tutti i dettagli della rete (inclusi DNS, MAC, DHCP). |

---

### 🔧 **Configurazione rete**

| Comando                          | Descrizione                                   |
| -------------------------------- | --------------------------------------------- |
| `ipconfig /release`              | Rilascia l’indirizzo IP assegnato (DHCP).     |
| `ipconfig /renew`                | Richiede un nuovo indirizzo IP.               |
| `ipconfig /flushdns`             | Svuota la cache DNS.                          |
| `netsh interface ip show config` | Mostra configurazioni IP per le interfacce.   |
| `netsh wlan show profiles`       | Mostra i profili Wi-Fi salvati.               |
| `netsh wlan show interfaces`     | Mostra lo stato della connessione Wi-Fi.      |
| `netsh wlan export profile`      | Esporta profili Wi-Fi (con o senza password). |

---

### 🌐 **Connettività e strumenti di rete**

| Comando                 | Descrizione                                                     |
| ----------------------- | --------------------------------------------------------------- |
| `telnet [host] [porta]` | Testa una porta TCP (es. `telnet smtp.gmail.com 587`).          |
| `ftp`                   | Client FTP (antiquato).                                         |
| `powershell`            | Consente script e comandi avanzati (es. `Test-NetConnection`).  |
| `Test-NetConnection`    | (PowerShell) Alternativa moderna a `ping`, `tracert`, `telnet`. |

---

### 📊 **Monitoraggio**

| Comando        | Descrizione                                      |
| -------------- | ------------------------------------------------ |
| `tasklist`     | Elenca i processi in esecuzione.                 |
| `netstat -ano` | Mostra connessioni con PID dei processi.         |
| `resmon`       | Apre il monitoraggio risorse (con sezione rete). |
| `perfmon`      | Apre il monitoraggio delle prestazioni.          |

---

### 📁 **Condivisione e rete locale**

| Comando      | Descrizione                                                 |
| ------------ | ----------------------------------------------------------- |
| `net view`   | Mostra i computer nella rete locale.                        |
| `net use`    | Gestisce le unità di rete (es. montare cartelle condivise). |
| `net share`  | Mostra le cartelle condivise locali.                        |
| `netstat -r` | Mostra la tabella di routing.                               |

---

