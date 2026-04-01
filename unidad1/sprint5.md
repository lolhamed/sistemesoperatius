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

<img width="512" height="160" alt="image" src="https://github.com/user-attachments/assets/8019a0ad-9f47-4b55-ac8e-e3796a561e5e" />


Podem veure la configuració específica de `rsyslog` per entendre com gestiona els seus propis fitxers:

<img width="593" height="113" alt="image" src="https://github.com/user-attachments/assets/e84d36eb-bbaa-4efe-9f1f-e01d6fc992ca" />

Podem veure la configuració específica de `rsyslog` per entendre com gestiona els seus propis fitxers:

<img width="654" height="492" alt="image" src="https://github.com/user-attachments/assets/b164868c-7b92-4853-8596-df15472fe0d3" />

## 4. Configuració de `rsyslog`

Antigament, tota la configuració es trobava a `/etc/rsyslog.conf`. Actualment, a les distribucions basades en Ubuntu/Debian, la configuració de les regles per defecte es troba a:
`/etc/rsyslog.d/50-default.conf`

<img width="736" height="484" alt="image" src="https://github.com/user-attachments/assets/11214c33-72d6-4cbc-8f5a-33e536744ef3" />

### Proves de funcionament

Per veure els canvis en directe mentre fem proves, executem en una terminal:
`tail -f /var/log/syslog`

1. Kern.notice

<img width="1740" height="733" alt="image" src="https://github.com/user-attachments/assets/221f5af6-be87-4f04-b352-dc88eac87426" />


2. Mail.notice

<img width="1580" height="566" alt="image" src="https://github.com/user-attachments/assets/bc9443ae-0e85-4b50-b3e1-21b5b949d0ed" />


<img width="728" height="388" alt="image" src="https://github.com/user-attachments/assets/d2ee1515-6938-47bc-a235-a393e2127b49" />


Prova 3: Fitxers de log personalitzats

Podem redirigir logs a fitxers propis afegint una línia al fitxer `50-default.conf`. Per exemple, per enviar totes les alertes crítiques a un fitxer nou:
`*crit -/var/log/pau.log`


<img width="725" height="487" alt="image" src="https://github.com/user-attachments/assets/cf9b3bb7-0f42-4a72-9a66-c47ac042581f" />



## 5. El sistema `journalctl`

A més dels fitxers de text tradicionals, els sistemes moderns amb `systemd` utilitzen un log binari gestionat per `journalctl`. Això permet fer cerques molt més ràpides i filtrades.

Per exemple, per veure només els logs de correu:
`journalctl --facility=mail`


<img width="614" height="63" alt="image" src="https://github.com/user-attachments/assets/13bf7c3d-98f5-4929-9d24-18e0df53ef59" />








