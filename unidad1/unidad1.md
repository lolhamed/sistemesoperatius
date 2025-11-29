---
layout: default
title: "Sprint 1"
---

## Sprint 2








INDEX SPRINT 2

Sistemes de fitxers i particions

Mida sector

La mida del sector es la unitat minima fisica on es guarden les dades en un disco. Per defecte la mida son 512 bytes i no la podem modificar.



<img width="448" height="76" alt="image" src="https://github.com/user-attachments/assets/c069a6c1-f9ce-443c-a618-3242c484bd74" />






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


<img width="451" height="129" alt="image" src="https://github.com/user-attachments/assets/cd41ddcb-2940-491f-bf85-f9d1b42ac7da" />




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






<img width="563" height="116" alt="image" src="https://github.com/user-attachments/assets/73346bd0-3f49-42af-bab8-99a9c187ab3d" />

Si afegim una carpeta anomenada vesper és crearà automàticament pero no sera root a diferencia de l'altra comanda, nosaltres serem el root de vesper. Si volem modificar aixo utilitzem la comanda CHOWN.

<img width="586" height="153" alt="image" src="https://github.com/user-attachments/assets/fd0be1f3-432f-45b6-8c67-8879226b8aa4" />

I d'aquesta manera el root pasa a ser l'usuari vesper






Un altre inconvenient del useradd es que si volem fer un apt update amb l'usuari vesper no podrem per la nostra falta de permisos

<img width="1056" height="147" alt="image" src="https://github.com/user-attachments/assets/aeda4171-dc47-4bce-acf9-f26450601963" />

Resumint, els usuaris creats amb useradd no poden fer sudo




<img width="612" height="156" alt="image" src="https://github.com/user-attachments/assets/959d41d9-764d-4655-b149-112a605512dc" />

Si fem aixó podrem fer ús de sudo.




També si fem deluser seguit del usuari i el grup el borrem pero es important especificar el grup o borrarem l'usuari en general

<img width="546" height="81" alt="image" src="https://github.com/user-attachments/assets/ba71f709-3dd1-40ef-ab4a-fbfe230c8582" />





Una altra manera de ferho és amb usermod per ho llevarà dels altres grups



<img width="586" height="105" alt="image" src="https://github.com/user-attachments/assets/1682937f-f1f2-43a8-b049-577e5dbfd9af" />




























La comanda següent ens permet crear un grup


<img width="471" height="111" alt="image" src="https://github.com/user-attachments/assets/70677f5f-e162-488a-b989-aed5940de570" />



Per borrar el grup:
<img width="480" height="87" alt="image" src="https://github.com/user-attachments/assets/95599446-27f1-45bb-a7ae-fc69003d7f2b" />







<img width="568" height="145" alt="image" src="https://github.com/user-attachments/assets/3131a95b-46d0-4ede-8cf6-fd5912ed06f3" />

En aquesta comanda no hem fet que l'usuari Vesper estigui al grup asix sino que asix té permisos sobre l'usuari vesper.

















<img width="457" height="222" alt="image" src="https://github.com/user-attachments/assets/ac372087-e969-48a6-993c-9bce5d9da708" />


La comanda umask ens permet veure les mascares. La màscara canviarà si som usuari sudo o no







<img width="451" height="248" alt="image" src="https://github.com/user-attachments/assets/76f565cd-8ce7-4c5f-9fde-a62ad6f20162" />
















Després de crear una 3 usuaris i dos grups la comanda ens permet cambiar el grup principal on prèviament estaba l'usuari. En aquest cas l'usuari és alumne1


<img width="534" height="122" alt="image" src="https://github.com/user-attachments/assets/d7ea72ee-348c-4d45-b13e-76316782fceb" />




Modificarem ara la comanda de tal manera que els que formen part del grup colors puguin entrar pero que no pudin ni crear arxius ni esborrar.


<img width="545" height="115" alt="image" src="https://github.com/user-attachments/assets/9e884010-0dc4-4f51-87b4-2634285953e4" />


D'aquesta manera els permisos han canviat. Només a l'usuari alumne1.














