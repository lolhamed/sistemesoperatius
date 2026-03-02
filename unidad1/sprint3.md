<h1>Sprint 3: Administració de Dominis i Seguretat</h1>






1. Usuaris, Grups i Recursos
Són els objectes bàsics que conté el directori:
Usuaris: Comptes individuals per a persones (com el meu usuari ferranbernis).
Grups: Conjunts d'usuaris (ex: grup "professors", grup "alumnes") per gestionar permisos de cop.
Recursos: Impressores, carpetes compartides o servidors que estan registrats a la xarxa.</p>

<p>2. Unitats Organitzatives (OU)
Pensa en les OU com a carpetes o contenidors dins del servidor. Serveixen per organitzar els objectes segons la lògica de l'empresa o centre:
Exemple: Una OU anomenada Sistemes i una altra Administració.
Permeten aplicar polítiques (GPOs) diferents a cada grup.</p>

<p>3. L'Arbre (Tree)
Un Arbre és un conjunt d'un o més dominis que comparteixen un espai de noms continu (un nom arrel).
Si el teu domini principal és fje.edu, un subdomini anomenat clot.fje.edu formaria part del mateix arbre. Tots comparteixen una relació de confiança i una base de dades comuna.</p>

<p>4. El Bosc (Forest)
El Bosc és el nivell més alt del disseny. És un conjunt d'un o més arbres que no necessàriament comparteixen el mateix nom, però sí que comparteixen el mateix esquema (les regles de què pot contenir el directori) i configuració.
Exemple: Si l'escola fje.edu compra una empresa anomenada empresa.com, podrien unir els dos arbres en un mateix bosc per poder compartir recursos entre ells.</p>



<h2>Servidor LDAP</h2>

<p>Primer de tot canviarem de DHCP a IP manual</p>

<img width="579" height="469" alt="image" src="https://github.com/user-attachments/assets/1a7f7af2-ca37-44f2-be45-bbeab51f526b" />


Instal·lem slapd ldap-utils

<img width="718" height="294" alt="image" src="https://github.com/user-attachments/assets/10f91117-3b08-41bf-b1d6-2d8696ae4a93" />


Descomprimim un paquet que estaba al moodle:

<img width="307" height="81" alt="image" src="https://github.com/user-attachments/assets/25ba4747-a761-4cba-a1a9-8d28cdfdc5e3" />

I després fem dpkg-reconfigure slapd:

<img width="637" height="198" alt="image" src="https://github.com/user-attachments/assets/8355e242-9a1c-4bcf-977e-311baf0f28ce" />


Introduïm nom del domini (gina.cat):

<img width="642" height="135" alt="image" src="https://github.com/user-attachments/assets/798b3c40-a49d-452e-a68b-c068bdb532d9" />

Nom de l'organització:

<img width="504" height="114" alt="image" src="https://github.com/user-attachments/assets/f9e27661-5161-403a-a4d4-4d4421c8a52b" />


NO volem que s'hi purgui la base de dades:


<img width="487" height="122" alt="image" src="https://github.com/user-attachments/assets/8e7ee4d3-4fd9-4779-82a2-b83b79a9e34a" />


SI volem moure la base de dades antiga per sustituïrla per una de nova:


<img width="710" height="130" alt="image" src="https://github.com/user-attachments/assets/e69fef32-009e-4194-9f63-19b015b4e7ba" />


Una vegada acabat, fem la comanda slapcat i podem veure els canvis realitzats:


<img width="554" height="242" alt="image" src="https://github.com/user-attachments/assets/58909704-6883-4e60-925d-8961c37f6135" />

Entrarem a uo.ldif que estava al archiu comprimit i veurem que es un arxiu que crea una unitat organizativa anomenada users:

<img width="718" height="115" alt="image" src="https://github.com/user-attachments/assets/8c16299a-36f2-4128-989d-f3fcbdf20548" />


Entrarem a group.ldif que estava al archiu comprimit i veurem que es un arxiu que crea un grup anomenat alumnes i afegeix al usuari alu1 al grup:


<img width="716" height="122" alt="image" src="https://github.com/user-attachments/assets/294dc803-c81c-436a-9774-b69a24bb667d" />


Entrem a usu.ldif i veurem que el arxiu crea un usuari anomenat alu1 amb la contrasenya alu1 tambe especifcat la seva shell (bin/bsh) i la home (home/alu1) i el uid (1001):


<img width="705" height="335" alt="image" src="https://github.com/user-attachments/assets/ff5d2c39-07a4-4344-aba2-f5bcbce20e37" />


Després executem els 2 arxius i fem una altra comprovació amb slapcat:


<img width="504" height="673" alt="image" src="https://github.com/user-attachments/assets/ee2338f0-0dff-43bd-b77b-2841f258ca6b" />


<img width="525" height="560" alt="image" src="https://github.com/user-attachments/assets/cdc72e6e-a0c8-4cca-9673-697b76ed6241" />



Ara anirem al client,i instalarem els paquets neccesaris. libnss-ldap, d'aquesta manera el sistema pugui consultar noms d'usuari i grups al servidor i libpam-ldap per a que el sistema pugui gestionar l'autenticació (contrasenyes) contra el servidor, una vegada instal·lats ens sortirà la configuració:



<img width="666" height="151" alt="image" src="https://github.com/user-attachments/assets/2a574a5f-6791-4b9e-9bd4-88f8f0ab57d0" />


Introduïm el domini:


<img width="675" height="137" alt="image" src="https://github.com/user-attachments/assets/04d01282-9215-4b2a-a509-e05f0d33584a" />


La versió (3):


<img width="688" height="145" alt="image" src="https://github.com/user-attachments/assets/e45a43e5-56be-4641-932b-c1f208b80d44" />


En cas que vulguessim que l'usuari local sigui adminsitrador de la base de dades i que el arxiu de les contrasenyes sol serà accesible per root:


<img width="637" height="155" alt="image" src="https://github.com/user-attachments/assets/df644da1-f6ed-4c48-b32f-367d000c5b1b" />


I en cas que volguessim login a la base de dades:


<img width="498" height="131" alt="image" src="https://github.com/user-attachments/assets/09953bcf-4aa3-4ad6-8730-5ceca3317cf1" />
































