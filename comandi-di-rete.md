# PRINCIPALI COMANDI DI RETE 



---

### 🔍 **Diagnostica e test della rete**

| Comando      | Descrizione                                                                                                              |
| ------------ | ------------------------------------------------------------------------------------------------------------------------ |
| `ping`       | Verifica la raggiungibilità di un host e misura il tempo di risposta.                                                    |
| `traceroute` | Mostra il percorso seguito dai pacchetti fino a una destinazione.                                                        |
| `tracepath`  | Simile a `traceroute`, ma non richiede privilegi di root.                                                                |
| `nslookup`   | Interroga i server DNS per risolvere nomi di dominio.                                                                    |
| `dig`        | Simile a `nslookup`, più completo per interrogazioni DNS.                                                                |
| `host`       | Semplice comando per la risoluzione DNS.                                                                                 |
| `netstat`    | Mostra le connessioni di rete, le tabelle di routing e le statistiche delle interfacce. *(Obsoleto, sostituito da `ss`)* |
| `ss`         | Visualizza socket e connessioni attive in modo più moderno ed efficiente.                                                |

---

### 🔧 **Configurazione e gestione della rete**

| Comando    | Descrizione                                                                          |
| ---------- | ------------------------------------------------------------------------------------ |
| `ip a`     | Visualizza le interfacce di rete e i relativi indirizzi IP.                          |
| `ip link`  | Mostra o modifica lo stato delle interfacce.                                         |
| `ip route` | Mostra o modifica la tabella di routing.                                             |
| `ifconfig` | Vecchio comando per configurare interfacce di rete. *(Obsoleto, sostituito da `ip`)* |
| `nmcli`    | Gestisce la rete tramite NetworkManager da linea di comando.                         |
| `nmtui`    | Interfaccia testuale interattiva per NetworkManager.                                 |

---

### 🌐 **Connessioni e trasferimenti**

| Comando        | Descrizione                                                               |
| -------------- | ------------------------------------------------------------------------- |
| `wget`         | Scarica file da web via HTTP/HTTPS/FTP.                                   |
| `curl`         | Trasferisce dati da o verso un server (HTTP, FTP, ecc.).                  |
| `scp`          | Copia sicura di file tra host tramite SSH.                                |
| `rsync`        | Sincronizza file e directory in modo efficiente.                          |
| `ftp` / `sftp` | Client per trasferimento file tramite protocollo FTP o SSH.               |
| `telnet`       | Connessione a porte TCP per test. *(In disuso per motivi di sicurezza)*   |
| `nc` (netcat)  | Utilità versatile per test di rete e debug (ascolto, invio, porte, ecc.). |

---

###  **Monitoraggio e sniffing**

| Comando     | Descrizione                                                        |
| ----------- | ------------------------------------------------------------------ |
| `tcpdump`   | Analizza pacchetti di rete in tempo reale.                         |
| `wireshark` | Sniffer grafico avanzato per analisi dei pacchetti (richiede GUI). |
| `iftop`     | Mostra traffico in tempo reale su interfacce di rete.              |
| `nload`     | Mostra graficamente il traffico in entrata e uscita.               |
| `iptraf`    | Statistiche di rete in tempo reale (interfaccia testuale).         |

---

###  **Altri comandi utili**

| Comando      | Descrizione                                             |
| ------------ | ------------------------------------------------------- |
| `hostname`   | Mostra o imposta il nome dell’host.                     |
| `whois`      | Interroga registri di dominio (WHOIS).                  |
| `arp`        | Mostra la cache ARP (mappatura IP <-> MAC).             |
| `ethtool`    | Visualizza o modifica le impostazioni hardware di rete. |
| `macchanger` | Cambia l’indirizzo MAC di una interfaccia.              |

---

