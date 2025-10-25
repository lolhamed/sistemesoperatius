---
layout: default
title: "Sprint 1"
---

## Sprint 1

Primer de tot, començarem amb la instal·lació de la màquina virtual d'Ubuntu.

<img width="951" height="674" alt="image" src="https://github.com/user-attachments/assets/924d6c7e-fc87-4b04-852e-7f79d9fc562d" />


<img width="952" height="671" alt="image" src="https://github.com/user-attachments/assets/5c6dc660-84f0-4ca5-91bb-bd6b37090578" />

He posat per defecte la configuració.




Després de fer la instal·lació, actualitzem la llista de paquets disponibles.




<img width="811" height="110" alt="image" src="https://github.com/user-attachments/assets/1ac0255a-bc2a-4780-b283-44ad3b43e5d6" />

Instal·lem totes les actualitzacions disponibles que tenim al sistema,

<img width="783" height="156" alt="image" src="https://github.com/user-attachments/assets/dacebcfc-affd-4d32-b0bd-c3d5fc5a648d" />


Si volem veure informació del sistema escrivim la comanda hostnamectl



<img width="717" height="325" alt="image" src="https://github.com/user-attachments/assets/c977c930-86c7-4977-96bd-2a3ed7b8f005" />

Per mostrar els dispositius d'emmagatzematge:
<img width="729" height="396" alt="image" src="https://github.com/user-attachments/assets/a28c3a98-f21c-4f81-afc6-48b9372233da" />



<img width="478" height="50" alt="image" src="https://github.com/user-attachments/assets/211d5964-9e0f-48ba-a313-0bd7b2b562c1" />

Obre el fitxer de configuració del GRUB per modificar-lo (per exemple, canviar el temps d’espera o el sistema predeterminat).

Per a fer servir punts de restauració utilitzarem l'eina timeshift 
<img width="796" height="154" alt="image" src="https://github.com/user-attachments/assets/34a874fd-24ee-46a9-8cd8-ee7837708473" />



La comanda mostra els punts de restauració existents.
<img width="793" height="215" alt="image" src="https://github.com/user-attachments/assets/fd99bf51-2308-418a-b5a1-af7829f9890c" />


Per crear un punt de restauració en aquest moment.
<img width="811" height="190" alt="image" src="https://github.com/user-attachments/assets/def382da-219a-42a8-81cb-5b2f7597c49a" />

Per eliminar un punt de restauració en aquest moment:
<img width="688" height="167" alt="image" src="https://github.com/user-attachments/assets/2f894412-bd8f-431e-bd80-651bbf9dee99" />


Per borrar tots els punts de restauració:
<img width="690" height="186" alt="image" src="https://github.com/user-attachments/assets/e926e9fa-4315-4866-a158-b6bf7877d797" />

Per obrir la interficie gràfica:
<img width="813" height="95" alt="image" src="https://github.com/user-attachments/assets/b697588c-dd12-46ac-9496-7d5066d795de" />



<img width="592" height="257" alt="image" src="https://github.com/user-attachments/assets/1cb6c0c9-8437-48f4-8e1f-885fa9a76c23" />

















dpkg és el gestor de paquets bàsic de Debian i sistemes derivats com Ubuntu. S’encarrega de instal·lar, eliminar i gestionar paquets .deb al teu sistema.

Un paquet .deb és un fitxer que conté programari precompilat, juntament amb informació sobre dependències i fitxers que s’han d’instal·lar.

dpkg treballa a nivell individual de paquet, a diferència d’apt o apt-get, que gestionen repositoris sencers i les dependències automàticament.

