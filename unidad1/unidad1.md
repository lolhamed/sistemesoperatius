Virtualizacio i instalacio del SO Ubuntu


Primer de tot selecionarem la memoria ram de la maquina virtual el minim son 4 GB i com a el ordinador host de 32GB introduirem 8GB despres com sera dual introduirem 80 GB de disc 40 GB per a ubuntu i 40 GB per a windows el minim de ubuntu son 25 GB i a la xarxa selecionarem xarxa NAT la diferencia amb el NAT es que els dos poden accedir a internet pero la xarxa nat poden veures varies maquines entre si la maquina anfitrió fa de router

<img width="579" height="619" alt="image" src="https://github.com/user-attachments/assets/bb6ec185-c8c2-4450-90e5-f7c23b8bbccd" />


Després procedim amb la instal·lació de la màquina virtual de Ubuntu:

<img width="804" height="515" alt="image" src="https://github.com/user-attachments/assets/5e75c7ba-748d-4b1c-a82a-2ce24d628516" />

<img width="804" height="385" alt="image" src="https://github.com/user-attachments/assets/4901dd04-67a1-44de-9f2d-cff8c4aed61c" />


Després inserim el dvd de les guest additions i executem autorun.sh

# Llicenciament

## Ubuntu

Ubuntu es una distribució de Linux basada en codi obert. La seva filosofia és permetre l'ús, modificació i redistribució del programari, tot respectant les condicions de les llicències corresponents. A continuació es detallen els principals tipus de llicències que trobem a Ubuntu.

## 1. Kernel Linux

- **Llicència:** GPLv2 (GNU General Public License versió 2)  
- **Descripció:** Permet l’ús, modificació i distribució del codi font del nucli Linux. Qualsevol modificació distribuïda ha de mantenir la mateixa llicència.

## 2. Programari lliure i codi obert

La majoria de les aplicacions incloses a Ubuntu estan sota llicencies de codi obert, com per exemple:

- **GPL (General Public License):** Ex. GNU Core Utilities, Bash.  
- **LGPL (Lesser General Public License):** Ex. biblioteques compartides com GTK.  
- **MIT / BSD:** Ex. moltes utilitats de desenvolupament i biblioteques gràfiques.  
- **Apache License:** Ex. alguns serveis i aplicacions web.


  ## GESTORS D'ARRENCADA PER A INSTAL·LACIONS DUALS
  
En una instal·lació dual boot amb Ubuntu i Windows, el gestor d’arrencada s’encarrega de permetre escollir quin sistema operatiu iniciar.
Ubuntu utilitza GRUB (GRand Unified Bootloader) com a gestor d’arrencada principal, mentre que Windows fa servir el seu propi gestor (Windows Boot Manager).

Quan s’instal·la Windows després d’Ubuntu, el seu instal·lador sobreescriu el sector d’arrencada (MBR o EFI), i això fa que el GRUB quedi eliminat o inactiu.

  Una vegada acabada la instal·lació de la màquina virtual d'Ubuntu i configurada la partició, farem un gestor d'arrencada instal·lant Windows:

  <img width="525" height="381" alt="image" src="https://github.com/user-attachments/assets/16805853-028b-4b28-a8ce-e8636a1fed7c" />


  Escollim la partició prèviament configurada:

  <img width="640" height="480" alt="image" src="https://github.com/user-attachments/assets/04f1385d-fb82-4dad-b0d7-5ace8c040a53" />


  Windows instal·lat!

  <img width="1008" height="672" alt="image" src="https://github.com/user-attachments/assets/7149116e-3a7a-42f5-b137-e288f871a1a7" />


  Una vegada Windows està instal·lat inserim la ISO al supergrub:

  <img width="474" height="133" alt="image" src="https://github.com/user-attachments/assets/eaf0c899-17c7-42da-955f-438007ca7aab" />


  Després engegem la màquina i entrem al boot manager:

  <img width="639" height="385" alt="image" src="https://github.com/user-attachments/assets/f8426b6c-66fe-4780-a4e3-7127edb038b4" />


  Seleccionem "detect and show boot methods":

  <img width="604" height="278" alt="image" src="https://github.com/user-attachments/assets/d110c71d-0bbb-435a-940e-336c1b79d20b" />

  IMPORTANT, escollir Ubuntu

  <img width="602" height="274" alt="image" src="https://github.com/user-attachments/assets/9d9de665-50b0-48a4-8033-d103c81f2407" />

  

  Una vegada fem aixó tornem a la màquina de Ubuntu, i posteriorment montem el EFI

  <img width="622" height="84" alt="image" src="https://github.com/user-attachments/assets/2c9b1d31-70a5-45ef-b756-6b65390686c3" />



  A posteriori, haurem de reinstallar el GRUB

  <img width="644" height="77" alt="image" src="https://github.com/user-attachments/assets/4c57f309-e63d-4ec2-9b68-1c66d7af1b42" />



  Una vegada el GRUB està instal·lat una altra vegada, hem d'escriure "GRUB_DISABLE_OS_PROBER=false


  <img width="754" height="478" alt="image" src="https://github.com/user-attachments/assets/5a04345c-35f9-4e7b-8048-ff92ebff62a2" />


  El següent pas a fer és actualitzar el GRUB mitjançant la comanda "sudo update-grub":

  <img width="825" height="233" alt="image" src="https://github.com/user-attachments/assets/03425b62-a177-44be-867a-bd9b45f72c71" />

  

  #  Punts de restauració

Amb Fdisk crearem la particio amb la opcio n (afegeix una nova partico) unica de 15GB

<img width="832" height="405" alt="image" src="https://github.com/user-attachments/assets/4d5717d8-925c-41ba-9445-65435c6ba8fc" />

Li donem format a la partició que anteriorment hem fet:

<img width="749" height="251" alt="image" src="https://github.com/user-attachments/assets/4566b891-d077-49e0-8255-a8a259853c20" />


Posteriorment instal·larem el programa Timeshift

<img width="633" height="96" alt="image" src="https://github.com/user-attachments/assets/353d5cda-7b25-4c2f-8ddb-0695f5493f59" />

IMPORTANT escollir el tipus d'instantanea que volem fer (RSYNC):

<img width="597" height="184" alt="image" src="https://github.com/user-attachments/assets/075fbdf2-f4d0-4ece-b6e7-64537d3adbd6" />


Hem d'escollir també la ubicació de la instantànea de la partició que hem fet:


<img width="573" height="35" alt="image" src="https://github.com/user-attachments/assets/3d6fb2e6-3038-45dd-b3d5-f3f3e0dfa2fd" />


Aqui escollim el temps que volem per a que cada instantanea es completi:

<img width="575" height="367" alt="image" src="https://github.com/user-attachments/assets/4f0208c6-3813-462a-9aef-8bf5adba8c42" />

Després seleccionem la carpeta (root no):


<img width="809" height="210" alt="image" src="https://github.com/user-attachments/assets/59c46491-de0d-4108-8231-427465047eda" />


Configurem una instantànea:


<img width="795" height="335" alt="image" src="https://github.com/user-attachments/assets/5940968a-f826-4f1b-a591-a7dd0ded1403" />

























  







