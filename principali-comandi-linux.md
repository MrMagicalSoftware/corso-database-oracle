
---

### **Navigazione e gestione file**

| Comando                         | Descrizione                           |
| ------------------------------- | ------------------------------------- |
| `ls`                            | Elenca i file in una directory        |
| `cd`                            | Cambia directory                      |
| `pwd`                           | Mostra il percorso corrente           |
| `mkdir nome_cartella`           | Crea una nuova cartella               |
| `rm file`                       | Rimuove un file                       |
| `rm -r cartella`                | Rimuove una cartella (ricorsivamente) |
| `cp file1 file2`                | Copia file1 in file2                  |
| `mv file1 file2`                | Sposta o rinomina un file             |
| `touch nome_file`               | Crea un nuovo file vuoto              |
| `cat file`                      | Mostra il contenuto di un file        |
| `less file` / `more file`       | Visualizza file a scorrimento         |
| `find /percorso -name nomefile` | Cerca un file per nome                |
| `file nomefile`                 | Mostra il tipo di file                |

---

###  **Permessi e proprietà**

| Comando | Descrizione                         |
| ------- | ----------------------------------- |
| `chmod` | Cambia i permessi di file/cartelle  |
| `chown` | Cambia il proprietario di un file   |
| `ls -l` | Elenca file con dettagli e permessi |

---

###  **Gestione pacchetti**

(Variano in base alla distribuzione)

| Comando                                 | Descrizione                           |
| --------------------------------------- | ------------------------------------- |
| `apt update` / `apt upgrade`            | (Debian/Ubuntu) Aggiorna pacchetti    |
| `apt install nome`                      | Installa un pacchetto                 |
| `dnf install nome` / `yum install nome` | (Fedora/RedHat) Installa un pacchetto |
| `pacman -S nome`                        | (Arch Linux) Installa un pacchetto    |

---

###  **Compressione e archivi**

| Comando                              | Descrizione                |
| ------------------------------------ | -------------------------- |
| `tar -czf archivio.tar.gz cartella/` | Crea un archivio compresso |
| `tar -xzf archivio.tar.gz`           | Estrae un archivio         |
| `zip -r archivio.zip cartella/`      | Crea un file zip           |
| `unzip archivio.zip`                 | Estrae un file zip         |

---

###  **Gestione utenti e processi**

| Comando        | Descrizione                                   |
| -------------- | --------------------------------------------- |
| `whoami`       | Mostra l'utente corrente                      |
| `adduser nome` | Aggiunge un nuovo utente                      |
| `passwd nome`  | Cambia password utente                        |
| `ps aux`       | Mostra i processi attivi                      |
| `top` / `htop` | Visualizza l’uso delle risorse in tempo reale |
| `kill PID`     | Termina un processo per ID                    |
| `killall nome` | Termina tutti i processi con quel nome        |

---

###  **Rete**

| Comando             | Descrizione                   |
| ------------------- | ----------------------------- |
| `ping indirizzo`    | Verifica la connettività      |
| `ifconfig` / `ip a` | Mostra configurazione di rete |
| `netstat -tulnp`    | Mostra le porte in ascolto    |
| `ss -tuln`          | Alternativa moderna a netstat |
| `curl` / `wget`     | Scarica dati da internet      |
| `scp`               | Copia file tramite SSH        |
| `ssh utente@host`   | Connessione a un altro host   |

---

###  **Sistema**

| Comando           | Descrizione                          |
| ----------------- | ------------------------------------ |
| `df -h`           | Mostra spazio su disco               |
| `du -sh cartella` | Mostra dimensione di una cartella    |
| `free -h`         | Mostra uso della memoria RAM         |
| `uptime`          | Mostra da quanto è acceso il sistema |
| `reboot`          | Riavvia il sistema                   |
| `shutdown now`    | Spegne il sistema subito             |
| `history`         | Elenca comandi precedenti            |

---

