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


<h2>FASE 4: GESTOR D'ARRENCADA</h2>

Primer que res, obrim un cmc com administrador:


<img width="449" height="311" alt="image" src="https://github.com/user-attachments/assets/4b984c81-4eda-4660-b137-8180977d9993" />


Executem bcdedit i com podem veure tenim 2 blocs:

<img width="607" height="564" alt="image" src="https://github.com/user-attachments/assets/ce80e1af-5d5d-40c5-a56f-8b8452f4fb6f" />

El primer bloc és l'administrador d'arrencada de Windows:

<img width="560" height="205" alt="image" src="https://github.com/user-attachments/assets/d4a736bb-34c6-43ab-b9d4-35e7fc238989" />

És el primer programa que s'executa. Gestiona el menú d'arrencada (si tens diversos sistemes operatius) i decideix quin carregar.



El segon bloc és el carregador d'arrencada de Windows:

<img width="624" height="283" alt="image" src="https://github.com/user-attachments/assets/1cf4396e-16a9-467e-89ee-a0711ff8cca5" />

És el que realment carrega el nucli (kernel) de Windows, els controladors i el sistema operatiu en si.


--

Una interpretació....

device: Indica en quina partició o disc es troben els fitxers d'arrencada (per exemple, partition=C:).

path: La ruta del fitxer executable (sol ser \Windows\system32\winload.exe).

description: El nom que veus quan s'encén l'ordinador (ex: "Windows 10" o "Windows 11").

locale: L'idioma de l'arrencada (ex: es-ES).

default: L'identificador del sistema que s'arrencarà per defecte si no toques res.


El sistema que s'està arrencant es Windows 10

Està instal·lat a partition=C

Abans d'arrencar, espera 30 segons, es pot veure a la linia timeout a l'apartat de l'administrador d'arrencada.

A a linia path a l'apartat carregador d'arrencada de Windows és veu el fitxer que inicia windows, que es el system32\winload.exe

Qui decideix l'arrencada (Boot Manager): L'Administrador d'arrencada de Windows és el programa que gestiona el menú inicial i decideix quin sistema operatiu o eina de recuperació s'ha d'executar segons la configuració del BCD.

Qui carrega el sistema (Boot Loader): El Carregador d'arrencada és el responsable de preparar l'entorn de programari i carregar el nucli (kernel) de Windows i els controladors crítics a la memòria RAM per iniciar la sessió.


<h2> FASE 5: XARXA BÀSICA</h2>

Si anem a l'apartat de configuració de xarxa i internet podrem veure el nostre estat de red:

<img width="799" height="512" alt="image" src="https://github.com/user-attachments/assets/a53c9d79-e4f4-49be-8be1-7b42391a5d5d" />


Si escrivim la comanda ipconfig al cmd es motra la configuració IP:

<img width="757" height="281" alt="image" src="https://github.com/user-attachments/assets/6f564a4c-43e5-4425-82bc-144837231037" />

Útil per a comprovar la IP


També, si anem a propietats, podrem configurar el DHCP (protocol que assigna les IPs) per defecte està automàtic:

<img width="650" height="488" alt="image" src="https://github.com/user-attachments/assets/b9def138-bf10-423e-8e37-57c119a9b779" />


En cas que sigui manual, ho haurem de configurar nosaltres:

<img width="382" height="632" alt="image" src="https://github.com/user-attachments/assets/0898a9ff-c13b-4557-8e8d-420cc148c54f" />


Ping de prova per comprovar la connexió:

<img width="617" height="242" alt="image" src="https://github.com/user-attachments/assets/cf197351-8fd9-4399-89d3-c46e46f7405f" />



<h2>FASE 6: COMANDES GENERALS</h2>

Tenim 2 tipus de terminals a Windows:


Powershell:

<img width="766" height="306" alt="image" src="https://github.com/user-attachments/assets/c6ca646c-acc5-47a7-90a6-51970b606bd2" />


CMD:

<img width="699" height="291" alt="image" src="https://github.com/user-attachments/assets/eb1a0259-b9da-48d9-9cb7-4044a575f8e6" />



La diferència es que PowerShell és més potent, permetent treballar amb objectes i automatitzar (scripts).


La comanda dir ens permet veure tots els fitxers:

<img width="498" height="410" alt="image" src="https://github.com/user-attachments/assets/3c9e2275-3ad5-4f48-8a91-9840d631f6b2" />


Amb mkdir podem crear una carpeta:

<img width="265" height="49" alt="image" src="https://github.com/user-attachments/assets/cf87566b-963e-4097-bd27-9b7956dea34e" />


Amb echo creem un fitxer:

<img width="348" height="53" alt="image" src="https://github.com/user-attachments/assets/b2f004b5-18a7-44b6-b3c3-681f8a284344" />


I amb del borrem un fitxer:

<img width="265" height="53" alt="image" src="https://github.com/user-attachments/assets/8bf3da00-e422-433b-9a6e-ba75b43d0f04" />


Podem veure els processos actius amb tasklist:

<img width="727" height="706" alt="image" src="https://github.com/user-attachments/assets/5402d947-770c-4908-9c0d-a64ab56e89ff" />


Amb systeminfo podrem veure informació relacionada al dispositiu:

<img width="926" height="598" alt="image" src="https://github.com/user-attachments/assets/a48aabe2-149c-4fc3-ae2f-148e93cbe085" />


Amb hostname podem veure el nom del host:

<img width="250" height="80" alt="image" src="https://github.com/user-attachments/assets/dd2e2930-83ad-4a3f-8699-01ab7a896cd7" />


whoami ens permet veure l'usuari actual:

<img width="227" height="114" alt="image" src="https://github.com/user-attachments/assets/17dbd13b-8dcf-4812-ac7c-106615ed4c8a" />


Amb netstat -an podem veure les connexions obertes:

<img width="750" height="646" alt="image" src="https://github.com/user-attachments/assets/cd45530f-2b44-4fa9-a635-2cddffff50b2" />


tree ens permet veure l'estructura de carpetes:

<img width="421" height="471" alt="image" src="https://github.com/user-attachments/assets/ca45ae74-05c4-40e3-b146-0bf6af596ce0" />


cls és el equvalent a clear a Ubuntu:

<img width="803" height="474" alt="image" src="https://github.com/user-attachments/assets/08bb3a5d-8944-46f4-a2c4-ac2f39b70bf3" />


amb help podem veure les comandes que podem usar:

<img width="763" height="396" alt="image" src="https://github.com/user-attachments/assets/f0f6147b-eab2-4bd2-9b19-786f6b7eabf9" />



tasklist:

Què mostra: Una llista de tots els processos i aplicacions que s'estan executant a l'ordinador en aquest precís moment.

Dades clau: Mostra el nom del fitxer executable, l'identificador del procés (PID) i la quantitat de memòria RAM que està consumint cadascun. És com el "Administrador de tasques" però en format text.

ipconfig:

Què mostra: La configuració de xarxa de l'equip.

Dades clau: Proporciona l'adreça IP de l'ordinador, la màscara de subxarxa i la porta d'enllaç predeterminada (la IP del router). És essencial per saber si estem connectats i com ens veu la xarxa.

systeminfo:

Què mostra: Un resum detallat de les propietats del programari i del maquinari (hardware) de l'equip.

Dades clau: Informació sobre la versió de Windows, el processador, la quantitat de memòria RAM instal·lada, la placa base (BIOS), el nom de l'equip i fins i tot quan es va instal·lar el sistema per primer cop.


<h2> FASE 7: INSTAL·LACIÓ D'APLICACIONS:</h2>


En aquesta fase instal·laré opera, per tant aniré a la pàgina oficial i baixaré el .exe:

<img width="926" height="280" alt="image" src="https://github.com/user-attachments/assets/42e38ffd-0817-4889-a0c6-b7fe1f8592a8" />


Instal·lació en curs

<img width="623" height="384" alt="image" src="https://github.com/user-attachments/assets/4f49a829-a3b3-4856-9d58-ebdd340c13df" />


Instal·lació completada, com podem veure funciona perfectament:

<img width="752" height="538" alt="image" src="https://github.com/user-attachments/assets/a11e9627-2f31-4688-a7d5-86c9f884602e" />




























