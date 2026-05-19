
# SPRINT 4: RAIDS

## Introduccio:

El RAID (Redundant Array of Independent Disks) és una tecnologia que combina diversos discs durs per millorar el rendiment i/o la seguretat de les dades.
En aquest cas utilitzarem RAID 1. Funciona per mirroring, és a dir, duplica exactament la informació en dos discs.
Això permet que, si un disc falla, les dades continuïn disponibles a l’altre.
És una solució senzilla i molt utilitzada per augmentar la tolerància a errors.



En una màquina virtual Ubuntu, afegim 2 discs amb la mateixa mida:

<img width="613" height="368" alt="image" src="https://github.com/user-attachments/assets/7099f0df-4af4-41b6-8e58-ff8dde7fdb42" />


Ja ho tenim:

<img width="1054" height="612" alt="image" src="https://github.com/user-attachments/assets/07745177-d5d3-45eb-a703-426aaf4bb94f" />


Ara preparem el sistema:

fem un apt update:

<img width="722" height="267" alt="image" src="https://github.com/user-attachments/assets/53bbc98d-e5fd-4b68-beab-de7c6be7bb49" />


Fem un fdisk -l i identifiquem els nostres discos:

<img width="614" height="246" alt="image" src="https://github.com/user-attachments/assets/b8c162fd-9d64-4fbb-b5ec-89b19e25ed9b" />

Creem una partició a cada disc:

<img width="780" height="544" alt="image" src="https://github.com/user-attachments/assets/e65f0e13-b06f-4089-b411-30fad8d41da3" />


<img width="754" height="510" alt="image" src="https://github.com/user-attachments/assets/11e71978-cd44-48f5-8fe5-38c5cbe257f7" />

Ara crearem el punt de muntatge:

<img width="497" height="143" alt="image" src="https://github.com/user-attachments/assets/3be696b5-cecd-4060-a920-1e11a0d54a56" />

Creem el raid1 ara:
<img width="858" height="238" alt="image" src="https://github.com/user-attachments/assets/cb6ba450-3743-4a84-bd42-55561e1fe280" />


Ara el formatem:
<img width="823" height="234" alt="image" src="https://github.com/user-attachments/assets/89aca13d-47c4-47b6-8403-d7b1ea368635" />

Comprovem el seu estat:

<img width="838" height="505" alt="image" src="https://github.com/user-attachments/assets/6e7137b0-865f-42d6-9e03-a764d0638f38" />

Guardem la configuració
<img width="839" height="62" alt="image" src="https://github.com/user-attachments/assets/7bcf8496-3946-4d4a-9c6f-25591d2973d4" />

FEM UN nano /etc/mdadm/mdadm.conf I Afegim la linia DEVICE /dev/sdb1 /dev/sdc1 :

<img width="850" height="113" alt="image" src="https://github.com/user-attachments/assets/f76b40e0-5167-4cbc-93e5-827e4a1724f2" />



Hem de configurar el muntatge automàtic:

Fem nano /etc/fstab

Afegim aquesta linia:

<img width="838" height="270" alt="image" src="https://github.com/user-attachments/assets/9f5e8360-ad67-474f-979f-80d76acb46ed" />


Ara farem proves de funcionament:

Creem un fitxer de prova:

<img width="538" height="113" alt="image" src="https://github.com/user-attachments/assets/0f41b7b9-0def-4a78-89db-d97ed1d91643" />


Simulem la fallada d'un disc:

<img width="734" height="545" alt="image" src="https://github.com/user-attachments/assets/972afd5a-06ab-47ec-b772-acb4e23377af" />

El RAID continuarà funcionant.


Eliminem el disc fallat:
<img width="560" height="45" alt="image" src="https://github.com/user-attachments/assets/feb9143d-b036-4dc4-887d-5a28a55b3502" />

El tornem a afegir i verifiquem l'estat una altra vegada:

<img width="612" height="115" alt="image" src="https://github.com/user-attachments/assets/a258c110-512c-4974-9577-66009de71c90" />


Per a borrar un raid fem un nano /etc/fstab:

<img width="846" height="316" alt="image" src="https://github.com/user-attachments/assets/b2df9d2c-e61f-417e-9fe9-df3a4088f254" />

I borrem la última linia:
<img width="846" height="311" alt="image" src="https://github.com/user-attachments/assets/43e59704-c8fd-44fd-96b3-830794c989e8" />

Ara aturem el raid:
<img width="469" height="61" alt="image" src="https://github.com/user-attachments/assets/ee648b21-d88e-46f2-ad97-29bcad3f1f95" />

Eliminem el punt de muntatge:

<img width="823" height="127" alt="image" src="https://github.com/user-attachments/assets/c9faaf12-eecf-4d96-9f63-c991623239f3" />

Netejem els discos:
<img width="739" height="41" alt="image" src="https://github.com/user-attachments/assets/f2aef3e5-de46-4d92-82b6-dc259c1c3b6a" />


