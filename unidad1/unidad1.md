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

