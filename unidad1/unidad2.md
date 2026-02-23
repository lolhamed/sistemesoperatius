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



