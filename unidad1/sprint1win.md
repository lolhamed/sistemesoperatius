## SPRINT 1 WINDOWS ##


<H2>FASE 1: INSTAL·LACIÓ DEL SISTEMA OPERATIU</H2>


Creem una màquina virtual amb la ISO de Windows

<img width="877" height="614" alt="image" src="https://github.com/user-attachments/assets/f1e3a2d8-c345-4705-b3ba-81dcdae3ee83" />


Assignem recursos

<img width="876" height="614" alt="image" src="https://github.com/user-attachments/assets/68bc99e7-2b94-4cb5-85b6-76503dcf1616" />

Editem el hostname:

<img width="880" height="616" alt="image" src="https://github.com/user-attachments/assets/b9c9fe10-00ed-4b56-afb6-4a52facf8960" />

Començem amb la instal·lació de Windows:

<img width="638" height="480" alt="image" src="https://github.com/user-attachments/assets/234b718d-7f63-44af-b2cf-a75590672002" />


Com podem veure funciona la màquina:

<img width="977" height="741" alt="image" src="https://github.com/user-attachments/assets/b09c0f43-7431-42b3-8ed8-79296ef9e1e8" />

<img width="1012" height="770" alt="image" src="https://github.com/user-attachments/assets/649346a3-c97d-429f-be93-4cf39c6b81ff" />




<H2>FASE 2:PUNTS DE RESTAURACIÓ:</H2>

Anem a la barra de Windows i escrivim "restauració":

<img width="748" height="673" alt="image" src="https://github.com/user-attachments/assets/0fab16c5-9ac3-4db6-8750-e0136c1ec350" />

Després fem click al nostre disc local i anem a l'apartat de configurar:

<img width="407" height="487" alt="image" src="https://github.com/user-attachments/assets/fe861e57-08ce-4aba-a8cb-48da02c447d3" />

Posteriorment, activem la protecció del sistema al disc:


<img width="399" height="203" alt="image" src="https://github.com/user-attachments/assets/117b958c-a945-441d-95db-a7d162a2a065" />

I asignem un 5% a l'espai del disc:


<img width="405" height="282" alt="image" src="https://github.com/user-attachments/assets/02f320de-11fe-451c-af04-61e92ddb8b07" />


A la mateixa ventana de propietats ens sortirà al final una opció que ens diu "crea...·:


<img width="397" height="105" alt="image" src="https://github.com/user-attachments/assets/09c4d437-316b-42d1-a76b-64785081aed7" />


Creem un punt de restauració i jo personalment li he donat el nom de sprint 1:


<img width="397" height="217" alt="image" src="https://github.com/user-attachments/assets/7a96f45f-152e-4d71-9b17-d014f6fdcaca" />


Fet!


<img width="350" height="121" alt="image" src="https://github.com/user-attachments/assets/4d30e213-2f0f-4359-aeb9-85eaf4fb0fb0" />


Ara farem un canvi i després farem una restauració, jo instal·laré Chrome:


<img width="1005" height="560" alt="image" src="https://github.com/user-attachments/assets/aadea19d-e4b8-4af1-8bc2-fa5ded2fb424" />



Al mateix menú fem click a restaurar sistema:


<img width="410" height="234" alt="image" src="https://github.com/user-attachments/assets/05da9a72-7c15-471a-bcbc-2bc54f68393c" />


Seleccionem la restauració que hem creat anteriorment:


<img width="562" height="455" alt="image" src="https://github.com/user-attachments/assets/ad9c9798-6c30-4120-aaa7-48126b6b2969" />


I fem click a si:


<img width="520" height="192" alt="image" src="https://github.com/user-attachments/assets/7f669e96-d775-4582-ad95-18a9cdfbb83f" />


La restauració esta en procés:

<img width="994" height="702" alt="image" src="https://github.com/user-attachments/assets/54abfe99-f273-43bf-98e9-370d1e295dc0" />


Després d'una estona, s'ha acabat de reiniciar i al entrar a la màquina m'ha sortit aquest missatge:

<img width="1013" height="735" alt="image" src="https://github.com/user-attachments/assets/2fd6fad3-3dd8-41af-b823-c53a0f8d0396" />


Com podem veure Google Chrome no està instal·lat, ja que és el canvi que hem fet després de configurar el punt de restauració


<h2>FASE 3:LLICÈNCIES DE WINDOWS</h2>

Si anem a configuració podem veure que la llicència no està activada:

<img width="795" height="283" alt="image" src="https://github.com/user-attachments/assets/b3248ec7-9da7-442b-881c-0d234c952665" />


Si executem al cmd slmgr /xpr podrem veure que Windows està en mode notificació, al fer la comanda al cmd em surt que tinc la versió core ( equivalent a Windows Home) indicant que Windows no està activat:

<img width="892" height="503" alt="image" src="https://github.com/user-attachments/assets/a22e64b8-8155-4da3-935d-53a63757a676" />

Quan Windows està en aquest mode, significa que el sistema ha detectat que no té una llicència vàlida o que el període de gràcia ha expirat. L'usuari rebrà avisos constants (notificacions) i tindrà limitacions, com no poder personalitzar el fons de pantalla o els colors del sistema.


N'hi han 3 tipus de llicenciament:

OEM (Original Equipment Manufacturer): Són les que venen preinstal·lades quan compres un ordinador (HP, Dell, Lenovo). Queden lligades a la placa base de l'ordinador i no es poden transferir a un altre PC.

Retail (Retail/FPP): Són les que compres a la botiga de Microsoft o en format físic. Es poden transferir d'un ordinador a un altre (sempre que només estigui activa en un a la vegada).

Voleme (VLC/KMS): Són llicències per a empreses o centres educatius que permeten activar molts ordinadors simultàniament amb una sola clau o un servidor local.


En quant al preu...

Tipus de Llicència,Web Oficial (Microsoft),Botigues Digitals (Amazon/PC Componentes),"Mercat de ""Claus"" (OEM barates)"
Windows 11 Home,~145 €,~110 € - 130 €,~10 € - 20 €
Windows 11 Pro,~259 €,~150 € - 200 €,~15 € - 25 €


