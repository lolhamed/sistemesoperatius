## Sprint 2

# Sistema de fitxers i particions

Mida sector

Unitat mínima on és guarden les dades en un disc:

<img width="696" height="288" alt="image" src="https://github.com/user-attachments/assets/ca94c944-1a31-4f0e-841f-541ba1c28826" />


Clúster

Unitat lógica on es guarden les dades a nivell de sistema operatiu. La mida predeterminada, és de 4096 bytes, modificable en cas que la partició és formateji.

<h4>La fragmentació interna</h4>
<p>és l'espai no utilitzat dins del darrer bloc assignat a un fitxer. És l'espai perdut dins de les unitats d'emmagatzematge del disc.
Aquest concepte s'origina per la manera com els sistemes operatius gestionen l'espai del disc dur.</p>

<h4>La fragmentació externa</h4>

Es refereix a l'espai lliure d'emmagatzematge que no és contigu, sinó que es troba dispers en molts petits forats separats per fitxers que s'han mantingut al disc.
A diferència de la fragmentació interna (que és espai perdut dins d'un bloc), la fragmentació externa és espai lliure totalment utilitzable, però està tan segmentat que pot ser massa petit per allotjar eficaçment fitxers nous i grans.

<img width="370" height="86" alt="image" src="https://github.com/user-attachments/assets/c13ac422-74e5-42ef-85b5-ab691b763381" />


<h4>Sistemes de fitxers</h4> 

Sistemes Robustos i Moderns (Linux/Unix)
ext4 (Fourth Extended Filesystem): És l'estàndard de facto actual en la majoria de distribucions Linux. Ofereix un excel·lent rendiment i és molt fiable. La seva característica principal és el journaling (registre per diari), que prevé la corrupció de dades en cas de fallada del sistema.

Btrfs (B-Tree Filesystem): Considerat el futur de Linux. És un sistema Copy-on-Write (CoW), el que significa que cada vegada que es modifica una dada, s'escriu en una nova ubicació, mantenint la versió antiga intacta. Això permet la creació de snapshots (instantànies) molt ràpides i la autocuració d'errors.

XFS: Destaca per la seva escalabilitat i alt rendiment, especialment amb fitxers i volums de dades molt grans. És molt utilitzat en entorns de servidors on es treballa amb arxius massius.

ZFS: Un sistema de fitxers i un gestor de volums integrats que es caracteritza per una gran integritat de dades gràcies a l'ús de sumes de comprovació (checksumming) per detectar i corregir errors de dades. També utilitza el principi CoW.

Sistemes Propietaris (Windows/Mac)

NTFS (New Technology Filesystem): L'estàndard utilitzat per Windows. Incorpora journaling, suport per a ACLs (Llistes de Control d'Accés) per a permisos de seguretat detallats i la capacitat d'encriptació de fitxers.

APFS (Apple File System): El sistema modern d'Apple (macOS, iOS), optimitzat per a dispositius amb memòria flash (SSDs). Està centrat en l'eficiència i la creació d'instantànies ràpides i lleugeres.

Sistemes per a Compatibilitat (Transferència)
<p>exFAT (Extended File Allocation Table): Creat per Microsoft, és l'opció preferida per a memòries USB i targetes SD. El seu avantatge és la compatibilitat universal entre Windows, Linux i macOS, a més d'eliminar la limitació de mida de fitxer de 4 GB que tenia el seu predecessor (FAT32).</p>

FAT32 (File Allocation Table 32): Un sistema antic, però encara utilitzat per la seva compatibilitat amb gairebé qualsevol dispositiu (càmeres, consoles, reproductors). La seva limitació clau és que no pot emmagatzemar fitxers individuals de més de 4 GB.



<h4>Baix Nivell</h4>

Aquest procés realitza una neteja total del disc.</p>
Borra sistema de fitxers, borra formateig, etc, eliminant totes les dades i totes les estructures lògiques prèvies. El disc queda en un estat de fàbrica, "com a nou", sense cap mena d'organització lògica (sense particions ni sistemes de fitxers).

IMPORTANT: No es pot fer des del sistema operatiu (SO) operatiu normal. Requereix programes adients i especialitzats, ja que treballa directament amb el firmware del disc dur.

<h4>Mig Nivell</h4>

S'hi centra en la capa lògica i la integritat del disc.</p>
Només borra el sistema de fitxers (igual que el format d'Alt Nivell Ràpid), deixant les dades antigues presents però irrellevants per al SO. La funció distintiva és la comprovació de la integritat: si hi ha sectors defectuosos, els marca per evitar que el sistema operatiu els utilitzi en el futur.

<h4>Alt Nivell</h4>

Aquesta és l'operació més comuna i ràpida.
Només borra el sistema de fitxers. El disc es prepara amb la creació del sistema de fitxers nou (p. ex., ext4 o NTFS) i el directori arrel. El contingut de les dades antigues roman al disc fins que es sobreescriu, cosa que permet la seva recuperació.



## Gestió de processos

Un procés és un programa que se està executant en un determinant moment.

Si utilitzem la comanda pstree podrem veure tots els processos que están en funcionament, en forma d'arbre, per veure quin es el pare i quin es el fill en cada procés
<img width="816" height="531" alt="image" src="https://github.com/user-attachments/assets/4ec4f271-054b-418b-ad68-6f846ea6aed6" />
<img width="817" height="532" alt="image" src="https://github.com/user-attachments/assets/667f6788-3ff4-4374-a01d-c9941ec7c1f8" />
<img width="805" height="529" alt="image" src="https://github.com/user-attachments/assets/156c07fd-bacd-4a8e-88af-5b66c180b7d5" />


<h4>top</h4>

Top serveix per mostrar en temps real els processos que s’estan executant i els recursos que utilitzen.</p>
Quan executes top, veuràs informació com:

PID → identificador del procés

USER → usuari que executa el procés

%CPU → percentatge de CPU que està utilitzant

%MEM → percentatge de memòria RAM que utilitza

COMMAND → nom del procés

<h3>Control de procesos</h3>


<h4>CTRL C</h4>

Ctrl c serveix per interrompre un procés que s’està executant.

Exemple:
<img width="983" height="157" alt="image" src="https://github.com/user-attachments/assets/14418c79-5798-4002-bae5-03d2c927b882" />

<h4>CTRL Z</h4>  
Ctrl z serveix per aturar temporalment un procés

Mateix exemple diferent comanda i resultat:

<img width="983" height="181" alt="image" src="https://github.com/user-attachments/assets/46a18033-566f-4ca9-b6f6-bfee6aa2f9fd" />

<h4>Jobs</h4>

Ens mostra els processos en segon pla:

<img width="802" height="324" alt="image" src="https://github.com/user-attachments/assets/1cdf20df-51dd-4434-8c3c-4eb3d0909f41" />

<h4>FG</h4>

El que fa FG és tornar el primer pla el procés:

<img width="783" height="292" alt="image" src="https://github.com/user-attachments/assets/61292965-1b7a-4fa7-9117-733d87dabe6b" />

<h4>HTOP</h4>

Mostra els processos en temps real:

<img width="800" height="526" alt="image" src="https://github.com/user-attachments/assets/dc984986-34ac-48bd-9325-d8d854792ee3" />


<h4>BTOP</h4>

Versió moderna d'HTOP amb una interficie acolorida:

<img width="795" height="518" alt="image" src="https://github.com/user-attachments/assets/aa71d608-dd9c-43cd-919a-aa119516d054" />

<h4>PS AUX</h4>

PS AUX el que fa és veure tots els processos que s'estan executant al sistema, de manera detallada, com podem veure a la captura n'hi han molts:

<img width="935" height="975" alt="image" src="https://github.com/user-attachments/assets/0704e8c7-8e65-4e0c-9ee9-51aa50933a22" />

<h4>KILL</h4>

Kill serveix per enviar senyals a processos, no només matar-lo (com el nom indica) sino també suspendre'l. Cada procés té un identificador únic, anomenat PID. Aquest PID per procés ho podem veure amb les comandes mostrades anteriorment (ps aux, htop, btop, etc...) i la comanda per a matar o suspendre un procés seria kill opció i la PID. És a dir, senyal, número, efecte. 

Respecte als números, el número 15 demana al procés que es tanqui de manera neta, el número 9 mata inmediatament el procés, el número 19 suspén el procés, i el número 18 torna a activar un procés que prèviament s'havia suspés:

Exemple:
<img width="1812" height="939" alt="image" src="https://github.com/user-attachments/assets/7a99de26-7fd0-4db7-bb3a-28b8b8ef672b" />

Si escribim kill -9 seguit de la PDI de firefox (en aquest cas era 6589) veurem que s'ha tancat el Firefox.

<img width="1516" height="816" alt="image" src="https://github.com/user-attachments/assets/9f0f1899-65fe-4d91-88f5-725fa4db5fe9" />

## Gestió d'usuaris, grups i permisos

Començem amb la gestió d'usuaris utilitzant gnome-system tools i primer que tot hem d'instal·lar-lo:

<img width="788" height="349" alt="image" src="https://github.com/user-attachments/assets/a8afdb3f-d1c6-4bce-b10f-a00c7e20894e" />

<h4>Fitxers implicats</h4>

nano /etc/passwd: aquest arxiu guarda informació bàsica per a cada usuari del sistema

<img width="820" height="531" alt="image" src="https://github.com/user-attachments/assets/1440efa0-b27f-406b-891e-8b9636ef9a90" />

nano /etc/group: aquest arxiu gestiona els grup d'usuaris:
<img width="812" height="525" alt="image" src="https://github.com/user-attachments/assets/e4ce6dbd-544e-4c14-a731-4ff77399eb00" />

nano /etc/shadow: aquest arxiu emmagatzema les contrasenyes xifrades dels usuaris i a més, informació adicional de seguretat:
<img width="810" height="532" alt="image" src="https://github.com/user-attachments/assets/89f23b4e-c7fa-4881-b0ac-33addc610c29" />

nano /etc/gshadow: aquest arxiu és el mateix que el shadow, pero la diferència és que gshadow és per als grups d'usuaris:
<img width="811" height="466" alt="image" src="https://github.com/user-attachments/assets/0d1bfeae-b122-42ff-9e0c-665df52bac22" />



<h4>Comandes bàsiques</h4>

Crear un usuari amb adduser:

<img width="832" height="560" alt="image" src="https://github.com/user-attachments/assets/8b5a77e5-2394-45dc-846d-b309cbb97100" />

Ara iniciem sessió amb gina:

<img width="391" height="110" alt="image" src="https://github.com/user-attachments/assets/2c7d661d-ce49-4f9b-befe-4dfcc9863c23" />

Comanda useradd:

<img width="387" height="43" alt="image" src="https://github.com/user-attachments/assets/b69f6117-6905-4a70-979a-340c4f2961fd" />

Eliminem el usuari gina amb deluser que borra tot alló relacionat amb l'usuari i eliminarem gina2 amb userdel que borra només l'usuari i no les carpetes relacionades amb l'usuari:

<img width="474" height="134" alt="image" src="https://github.com/user-attachments/assets/357379e7-29e0-446a-b0e5-8a94eeea71bc" />

Per a bloquejar i desbloquejar a un usuari:

<img width="976" height="328" alt="image" src="https://github.com/user-attachments/assets/88426d44-d8b2-4665-9e57-616d5ebb71fe" />


Crear un grup:

<img width="607" height="107" alt="image" src="https://github.com/user-attachments/assets/ef19cc67-6dfa-46f8-82dd-a3efe4f83ef0" />

Modificar i eliminar un grup:

<img width="678" height="334" alt="image" src="https://github.com/user-attachments/assets/c46f8b85-ed84-46a2-a801-cd73460fc005" />

Afegir un usuari a un grup:

<img width="589" height="62" alt="image" src="https://github.com/user-attachments/assets/14ab7220-9291-4065-81d2-410d1516b0d1" />

Afegir usuari admin a un grup:

<img width="509" height="48" alt="image" src="https://github.com/user-attachments/assets/d7fbf818-5002-4e0a-b439-80735cc82b50" />


Farem un experiment i crearem els usuaris roig, blau, groc i verd:

<img width="398" height="72" alt="image" src="https://github.com/user-attachments/assets/2b75cb64-a89a-41d3-a529-4b1dcdece3ba" />


Creem el grup dames:

<img width="395" height="39" alt="image" src="https://github.com/user-attachments/assets/8c16dbe6-83db-405b-a20f-aeb1099bf1d6" />

Cambiem el nom del grup:

<img width="237" height="46" alt="image" src="https://github.com/user-attachments/assets/5f94a65c-8934-4756-bfba-5cd95eaf2f89" />

Afegim a groc i roig com a grup principal al grup de parchis:

<img width="368" height="37" alt="image" src="https://github.com/user-attachments/assets/658ce1f1-f91c-49e7-be00-34c95df33aef" />


I si provem d'eliminar el grup parchis no podrem ja que té un usuari principal.


Despres entrarem a cd /etc/skel i veurem que tenim varios arxius mos centrarem en 3 de ells .bash_logout,bashrc i .profile:

<img width="523" height="91" alt="image" src="https://github.com/user-attachments/assets/03a100e6-2dfd-48c6-976b-830d8b9d588e" />


Ara entrarem a l'arxiu adduser.conf que son els parametres de la comanda adduser que serveix per crear usuaris introduirem que la Shell la volem en bash i que la carpeta home la volem a /var:

<img width="623" height="189" alt="image" src="https://github.com/user-attachments/assets/19efe0d0-2c59-40ea-962d-69e2fa8c1ea6" />

A partir de 3000 crearà ID dels usuaris.

<img width="747" height="522" alt="image" src="https://github.com/user-attachments/assets/16e45a69-faef-4386-95a6-a34081577822" />

Despres obrim l'arxiu login.defs que modifica es regles generals del sistema per a: contrasenyes creació d’usuaris permisos comportament del login

Introduirem que la contrasenya tingui un maxim de 20 dies i un minim de 15 dies amb avís als 3 dies

<img width="726" height="192" alt="image" src="https://github.com/user-attachments/assets/a8da16c6-c049-4470-b6c6-877bf7bdf3f3" />


Creem un usuari de prova per a comprovar que els canvis s'han realitzat:

<img width="659" height="311" alt="image" src="https://github.com/user-attachments/assets/585002c8-8d54-4a3f-911a-f6b8e74ea864" />


Ara modificarem el useradd i canviarem el shell a bash:

<img width="912" height="329" alt="image" src="https://github.com/user-attachments/assets/7267aff6-4a4e-42d9-8fdc-2e70749720b0" />

Creem un usuari, comprovem el id i que estigui al bash:

<img width="399" height="24" alt="image" src="https://github.com/user-attachments/assets/f80cdb19-267f-4264-84c6-16a591e11471" />

























































