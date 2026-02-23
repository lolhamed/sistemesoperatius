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



















