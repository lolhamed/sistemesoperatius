<h1>Sprint 3: Administració de Dominis i Seguretat</h1>






p>1. Usuaris, Grups i Recursos
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


