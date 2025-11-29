---
layout: default
title: "Sprint 1"
---

## Sprint 2








INDEX SPRINT 2

Sistemes de fitxers i particions

Mida sector

La mida del sector es la unitat minima fisica on es guarden les dades en un disco. Per defecte la mida son 512 bytes i no la podem modificar.









Mida block
La mida de block o cluster es la unitat minima logica on es guarden les dades a nivell de sistema operatiu. Per defecte son 2096 bytes. I aquesta mida si la podem modificar.
Quan? quan es formateja la partició. I cada particio del disc pot tenir una mida de bloc i un sistema de fitxers diferent.

Fragmentació interna
Els blocs son massa grans del que es vol guardar i es desaprofita espai al disc

Fragmentació externa
Es quan un arxiu no esta guardat en blocs consecutius de la memoria i els seus accesos son més lents i per tant baixa el rendiment.

Sistemes de fitxers
El sistema de fitxers condiciona moltes coses i cada sistema de fitxers esta optimitzat per a unes coses o unes altres i cada sistema de fitxer té unes limitacions.

Tipus de formateig
Baix nivell
Esborra tot (fitxers, sistemes de fitxers i intenta arreglar sectors defectuosos) pero necesitem programes especifics. No es possible a través de sistemes operatius.

Mig nivell
No esborra arxius només esborra el sistema de fitxers.
Sectors defectuosos ignorats totalment
Més lent que el d’alt nivell

Alt nivell
No esborra els arxius només esborra el sistema de fitxers. 
Els sectors defectuosos son ignorats totalment

Gestió particions






GPARTED

Particio: tros fisic del disc dur
Amb elk gparted podem gestionar particions pero no podem cambiar la mida del block. S’ha de fer amb comandes.

Un volum és una capa d’abstraccio que es posa damunt de les particions i/o discos


Comaneds

Gestio procesos
GEstio d’usuaris i grups i permisos
Copies de seguretat i atomatitzacio de tasques
Quotes d’usuari




















La mida del sector es la unitat minima fisica on es guarden les dades en un disco. Per defecte la mida son 512 bytes i no la podem modificar.

La mida de block o cluster es la unitat minima logica on es guarden les dades a nivell de sistema operatiu. Per defecte son 2096 bytes. I aquesta mida si la podem modificar. Quan? quan es formateja la partició. I cada particio del disc pot tenir una mida de bloc i un sistema de fitxers diferent.




















COMANDES



<img width="754" height="549" alt="image" src="https://github.com/user-attachments/assets/b5323c46-3314-4ca5-ab74-a28f2c875155" />
La comanda adduser ens permet crear un usuari. Com podem veure podem afegir al usuari més informació com ara contrasenya cosa que de moment omitirem





<img width="865" height="313" alt="image" src="https://github.com/user-attachments/assets/faeffdbb-9d5e-466e-8a35-f1dbee3e712e" />
Al fer un cat etc passwd podem confirmar el usuari creat






<img width="636" height="155" alt="image" src="https://github.com/user-attachments/assets/295cdc5e-1473-4c1b-a61e-aedd3ffbb418" />

Si anem a la carpeta home i fem un ls -l podrem veure que es crea una carpeta home i donen els permisos que toquen.




<img width="414" height="113" alt="image" src="https://github.com/user-attachments/assets/9840f08a-c25a-4d4d-8cf8-38461fce1763" />

Ara entrem a l'usuari Vesper





<img width="275" height="66" alt="image" src="https://github.com/user-attachments/assets/9c99614e-8894-468a-b0d6-e85534182d92" />

I sortim de l'usuari Vesper







<img width="615" height="114" alt="image" src="https://github.com/user-attachments/assets/171f42c7-80b8-42f5-bbaf-dd8d35091ef9" />

La comanda ens permet borrar l'usuari, la grub i el home amb -r.







<img width="409" height="46" alt="image" src="https://github.com/user-attachments/assets/c879b700-e00f-47c6-a2d3-d16fb2a050f4" />

La comanda useradd també crea un usuari, si fem cat està. La comanda useradd no demana contrasenya i si creem un usuari amb aquesta comanda si o si hem de configurar l'usuari i afegir més coses.










Com per exemple, la contrasenya:

<img width="597" height="135" alt="image" src="https://github.com/user-attachments/assets/7a032277-7985-4dd4-a183-76ac56e9b71b" />









