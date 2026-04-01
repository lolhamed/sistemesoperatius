# Sprint 5: Monitoratge, Auditories i Programari Client/Servidor



## 1. Conceptes Fonamentals de Logging

Per gestionar els logs, Linux utilitza dos conceptes principals per classificar la informació:

* **Facility:** Defineix l'origen o el tipus de programa que genera el missatge (ex: `auth`, `cron`, `kern`, `mail`). L'asterisc (`*`) s'utilitza per indicar totes les fonts.
* **Priority (Nivell):** Defineix la gravetat del missatge (ex: `debug`, `info`, `notice`, `warning`, `err`, `crit`, `alert`, `emerg`).
* Si posem un punt (`.`), estem indicant aquest nivell i tots els superiors.
* Si posem un igual (`.=`), indiquem **només** aquell nivell específic.


### L'eina `logger`

La comanda `logger` permet afegir entrades al log del sistema manualment des de la terminal.

> **Exemple:** `logger -i -s -p mail.err "Missatge d'error"`
> * `-i`: Afegeix el PID del procés.
> * `-s`: Mostra el missatge també per la sortida d'error estàndard.
> * `-p`: Especifica la *facility* i la *prioritat*.
---

## 2. Directoris i Fitxers Importants

La majoria dels logs del sistema s'emmagatzemen a `/var/log`. Tot i que molts serveis escriuen al fitxer general `syslog`, alguns paquets instal·lats creen les seves pròpies carpetes per gestionar les seves dades de manera independent.


<img width="680" height="230" alt="image" src="https://github.com/user-attachments/assets/ae9f6d30-7574-4b36-89f5-96a090daeab5" />

## 3. Rotació de Logs (`logrotate`)

Per evitar que els fitxers de log omplin tot el disc dur, el sistema utilitza **logrotate**. Aquesta eina:

1. Comprimeix els logs antics (sovint en format `.gz`).
2. Els reanomena (ex: `syslog.1`, `syslog.2.gz`).
3. Elimina els fitxers més vells segons una configuració de dies o mida.

La configuració es troba a `/etc/logrotate.d/`.

