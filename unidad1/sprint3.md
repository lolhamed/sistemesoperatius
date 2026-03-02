<h1>Sprint 3: Administració de Dominis i Seguretat</h1>


















<img width="1200" height="748" alt="image" src="https://github.com/user-attachments/assets/a6a780ae-bfef-4293-95b4-f82adc0e9387" />














<p>1. Usuaris, Grups i Recursos
Són els objectes bàsics que conté el directori:
Usuaris: comptes individuals per a persones (com el meu usuari ferranbernis).
Grups: conjunts d'usuaris (ex: grup "professors", grup "alumnes") per gestionar permisos de cop.
Recursos: impressores, carpetes compartides o servidors que estan registrats a la xarxa.</p>

<p>2. Unitats Organitzatives (OU)
Carpetes o contenidors dins del servidor. Serveixen per organitzar els objectes segons la lògica de l'empresa o centre:
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




Posteriorment, ens demanarà un user admin de LDAP:


<img width="476" height="184" alt="image" src="https://github.com/user-attachments/assets/b365d8d0-ca79-48c0-aeec-aff59e7565ab" />


I contrasenya:


<img width="970" height="243" alt="image" src="https://github.com/user-attachments/assets/76235a9f-c59e-423a-8c32-51face82bbbe" />


Ara l'usuari que usarem per iniciar sessió a la base de dades LDAP:


<img width="865" height="196" alt="image" src="https://github.com/user-attachments/assets/5b6e1206-4e29-4da9-af3e-92e9f4abc207" />


Permetre futures actualitzacions:


<img width="774" height="156" alt="image" src="https://github.com/user-attachments/assets/62e9a901-14f2-4226-a7d3-a7890ac5020d" />


També altres avisos com el métode de xifratge per a la contrasenya (escollirem md5):


<img width="984" height="319" alt="image" src="https://github.com/user-attachments/assets/ef646f57-a60b-4ac1-8917-83551456143e" />



<img width="383" height="226" alt="image" src="https://github.com/user-attachments/assets/7457aa06-27ff-4ab4-98a7-defb9f7d5a1e" />



Modificarem l'arxiu nsswitch i a passwd i group introduirem ldap compact files systemd això vol dir que quan el sistema busqui un usuari per fer login, primer preguntarà a la base de dades LDAP.


<img width="789" height="383" alt="image" src="https://github.com/user-attachments/assets/96695d6b-ba57-4cdd-b793-1a20578ac483" />


També modificarem el arxiu common-session que es molt important perque crea la carpeta home de els usuaris LDAP:


<img width="786" height="435" alt="image" src="https://github.com/user-attachments/assets/5ca0ad76-2a76-4f20-8897-2d59d7589017" />



Tambe modificarem el arxiu common password afegint la 4 linea blanca de password que fa:

pam_pwquality.so: Primer es comprova que la contrasenya nova sigui prou segura (complexitat).

pam_unix.so: S'encarrega dels usuaris locals.

pam_ldap.so: És la línia clau que s'ha afegit. El paràmetre try_first_pass fa que el sistema intenti fer servir la contrasenya que ja has escrit abans de tornar-te-la a demanar.

[success=1 user_unknown=ignore default=die]: Aquest és un codi de control. Diu que si el mòdul de LDAP té èxit, se saltarà el següent pas (que sol ser un missatge d'error)



<img width="953" height="341" alt="image" src="https://github.com/user-attachments/assets/e0e3eaef-1654-4f9b-965f-0fa7d80e37e3" />



Per finalizar els arxiu modificarem es e 50-ubuntu.conf afegint la ultima linea que mostra una llista amb els usuaris locals que ja existeixen a la màquina:


<img width="770" height="113" alt="image" src="https://github.com/user-attachments/assets/a7d4149b-9867-4bf2-a007-ae6a3440ed91" />



<h2>Interfice Grafica LDAP</h2>


Primer que res, instal·lar jpxplorer:


<img width="723" height="390" alt="image" src="https://github.com/user-attachments/assets/48c92e8d-13f4-4949-8f66-ff85d4509ddb" />


L'executem:

<img width="438" height="262" alt="image" src="https://github.com/user-attachments/assets/cc12528a-3e3e-43c7-999c-7ed67584bcff" />


Introduïm la IP i el domini:


<img width="662" height="499" alt="image" src="https://github.com/user-attachments/assets/82842602-4581-4dea-bfe2-1105ba48cefc" />


Vista gràfica per gestionar el servidor LDAP:


<img width="784" height="427" alt="image" src="https://github.com/user-attachments/assets/f2033b7c-33ee-4b11-a486-0e0c35ccdbc1" />


<h2>Servidor Samba</h2>

<p>Samba serveix per compartir fitxers, impressores i carpetes en una xarxa local. La seva gran característica, és que permet gestionar l'accés mitjançant una autenticació a nivell d'usuari. Això significa que el servidor no només comparteix el recurs, sinó que verifica qui ets abans de deixar-te entrar, permetent que cada usuari tingui els seus propis permisos i carpetes privades.</p>



<img width="715" height="398" alt="image" src="https://github.com/user-attachments/assets/138f2b12-e66e-4eba-b4b4-ebf593ad8380" />


Ara crearem una carpeta anomenada proves donarem tots els permisos a tothom amb chmod 777 i canviarem el propietari amb chown indicant que no volem propietari a la carpeta i tampoc volem grup i comprovarem que s'hagui creat correctament, crearem 3 usuaris (roig, blau i groc) amb uns paràmetres específics:


<img width="308" height="53" alt="image" src="https://github.com/user-attachments/assets/6d9d3a30-5193-444e-9088-7f209f961753" />


Entreem al arxiu etc/samba/smb.conf que es el arxiu de configuració de samba i afegirem al final de tot proves que serà la carpeta que compartirem amb samba a path introduirem la ruta de la carpeta a guest ok direm si volem usuaris anonims o no a directory mask i a create mask introduirem la màscara que són els permisos que asseguren que els fitxers nous siguin llegibles per tothom però només modificables pel propietari:


<img width="720" height="616" alt="image" src="https://github.com/user-attachments/assets/3535d951-5808-4316-8a79-f6386b842c92" />


Posteriorment, reiniciem el servei i a l'apartat de fitxers, provarem de connectar-nos amb un usuari aleatori (roig) peró no ens deixarà:


<img width="578" height="427" alt="image" src="https://github.com/user-attachments/assets/14635389-a000-4a49-b398-4d58143e7a2e" />


Pero en guest si que funciona (configurat prèviament):


<img width="573" height="183" alt="image" src="https://github.com/user-attachments/assets/f31df2bb-b3c2-4c2e-a2d8-c15adb17bf2d" />


<h2>Servidor NFS</h2>

<p>NFS es un protocol que permet compartir fitxers directoris (no impresores) amb linux a traves de una xarxa local la autentificació es fa a nivell de host no de usuari, a diferencia de samba i poden accedir tant clients windows com linux</p> 









<h3>NFS SENSE LDAP</h3>

<p>Primer de tot instalarem el paquet nfs-kernel server (Servidor NFS)</p> 


<img width="563" height="185" alt="image" src="https://github.com/user-attachments/assets/e3e0e76e-6ac2-4b8b-8e2a-b06da6de33a4" />




Ara crearem la carpeta 1exercici donarem privilegis totals a tohom amb chmod 777 i canviarem el propietari a ningú i el grup també amb chown nobody:nogroup i comprovarem els permisos i el propietari amb ls -l i filtrarem per el 1 i veurem que tindrà tots els permisos correctes:



<img width="741" height="549" alt="image" src="https://github.com/user-attachments/assets/8ccecc5f-4c77-41a1-8dea-55daa76ea920" />



Després, entrem a l'arxiu export i el modificarem:


<img width="809" height="235" alt="image" src="https://github.com/user-attachments/assets/5252b04a-b6d9-4aa7-892f-fb28a93e0d0f" />


Reiniciem el server i veurem que està actiu:


<img width="814" height="132" alt="image" src="https://github.com/user-attachments/assets/9bc4be87-3ea7-4aaa-b51e-4922a8d0b4ce" />


<h3>NFS AMB LDAP</h3>


<p>Al servidor crearem la carpeta homes i donerem privlegis totals a tohom amb chmod 777 i canviarem el propietari a ningu i el grup tambe amb chown nobody:nogroup i crearem la carpeta marcel tambe donarem privlegis totals a tohom i després Copiarem i pegarem la linea de la carpeta 1exercici baix i canviarem el nom a homes</p>


<img width="804" height="241" alt="image" src="https://github.com/user-attachments/assets/b367f479-1082-4d45-9324-d396921ec33c" />



Entrarem a el arxiu /etc/fstab i copiarem la linea de la carpeta 1exercici i la pegarem canviarem el nom de les carpetes a les corresponents al servidor i al client que es /homes al servidor i /homes al client:


<img width="787" height="279" alt="image" src="https://github.com/user-attachments/assets/39eaf0cc-20f9-4f2b-9509-29f2dd3168de" />


Anirem a el Servidor i crearem el usuari marcel a el LDAP introduint que la carpeta home seria /homes/marcel que son les carpetes compartides:



<img width="780" height="379" alt="image" src="https://github.com/user-attachments/assets/42a4d858-4d3f-45eb-8394-da3fab6ddb6d" />


<h3>NFS AMB WINDOWS</h3>

<p>Primer anirem a programes i caracteristiques i instalarem el paquet client per a NFS</p> 


Anem a programes i característiques i instal·lem el paquet:


<img width="621" height="428" alt="image" src="https://github.com/user-attachments/assets/c0cf7526-ec36-43db-9ab2-6f36b9e7a4c2" />


Després obrirem una terminal de powershell i intoduirem mount.exe per a montar la ip de el servidor la ruta de la carpeta al servidor i per últim el punt de muntatge:


<img width="421" height="87" alt="image" src="https://github.com/user-attachments/assets/38845d18-5e01-45d3-8eb2-e6cbf53d20e2" />


I ja ho tindriem:


<img width="435" height="176" alt="image" src="https://github.com/user-attachments/assets/4245a3f3-a34b-4f36-8f5c-c43b00b43700" />
















































































