# Sprint 5: Monitoratge, Auditories i Programari Client/Servidor



## 1. Conceptes Fonamentals de Logging

Per gestionar els logs, Linux utilitza dos conceptes principals per classificar la informació:

* **Facility:** Defineix l'origen o el tipus de programa que genera el missatge (ex: `auth`, `cron`, `kern`, `mail`). L'asterisc (`*`) s'utilitza per indicar totes les fonts.
* **Priority (Nivell):** Defineix la gravetat del missatge (ex: `debug`, `info`, `notice`, `warning`, `err`, `crit`, `alert`, `emerg`).
* Si posem un punt (`.`), estem indicant aquest nivell i tots els superiors.
* Si posem un igual (`.=`), indiquem **només** aquell nivell específic.


### L'eina `logger`

