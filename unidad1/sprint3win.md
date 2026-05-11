
## SPRINT 3: ADMINISTRACIÓ DE DOMINIS I SEGURETAT ##


  Configuració bàsica:


  Fem un ipcoonfig per veure la nostra ip


<img width="625" height="248" alt="image" src="https://github.com/user-attachments/assets/2a9dd5da-bf67-482a-9a6a-ddb9eaadd988" />



  
<img width="387" height="449" alt="image" src="https://github.com/user-attachments/assets/4f6af9b5-518b-455b-8d52-eeb229c2e1c0" />



Ping de prova:

<img width="506" height="245" alt="image" src="https://github.com/user-attachments/assets/3b10e91e-ac84-4044-8872-d0cf5eefbe8e" />



Obrim l'administrador del servidor:

<img width="777" height="558" alt="image" src="https://github.com/user-attachments/assets/cbeb00cc-f531-4631-9469-d2905551f012" />


Premem següent 3 vegades i marquem la casella de serveis de domini de active directory:

<img width="781" height="558" alt="image" src="https://github.com/user-attachments/assets/d6d417c2-d8c5-457f-b93e-e091bf2bc27e" />


Tornem a premer següent 2 vegades i a l'apartat de confirmació, marquem la casella de "reiniciar servidor en cas necessari":

<img width="778" height="559" alt="image" src="https://github.com/user-attachments/assets/b8979074-a6e3-4fc2-b373-9c764310c43d" />


Fem click a "promoure servidor a controlador de domini":

<img width="951" height="180" alt="image" src="https://github.com/user-attachments/assets/9d27ecb1-8a87-49e9-ba22-672c5688084d" />


Despreś, ens sortirà una finestra que diu "configuració de implementació", fem click a l'apartat "agregar un nou bosc" i escrivim el nom del domini que volem:

<img width="758" height="554" alt="image" src="https://github.com/user-attachments/assets/b5c878ab-1166-4e83-a126-8875efe151dc" />


Afegim la nostra contrasenya:

<img width="758" height="560" alt="image" src="https://github.com/user-attachments/assets/1b35e716-d8cc-49ef-a782-e0bc70eaf35a" />


Després farà un reinici:

<img width="1014" height="729" alt="image" src="https://github.com/user-attachments/assets/2e1d34ca-062f-4d61-b083-cc7524ea01f2" />


Una vegada s'ha reiniciat, farem click a "usuaris i equips d'active directory":

<img width="1021" height="702" alt="image" src="https://github.com/user-attachments/assets/23c8ab48-1071-41b5-91e6-bac1a8d1b7e3" />

Després fem click dret al nostre domini i a nou, afegim una unitat organitzativa:

<img width="657" height="525" alt="image" src="https://github.com/user-attachments/assets/a68f51c2-542d-46fe-8aab-3a50d0668c8c" />


Li fiquem el nom "classe":

<img width="436" height="373" alt="image" src="https://github.com/user-attachments/assets/04a44af7-e3f4-436f-a67c-f2839f0ff16b" />


Fem click dret a classe i afegim un nou usuari:

<img width="717" height="497" alt="image" src="https://github.com/user-attachments/assets/72a4d229-05d9-407e-a5d6-fc43e09d8930" />


<img width="429" height="374" alt="image" src="https://github.com/user-attachments/assets/668fbc39-b49d-419c-bb3e-553da2dd6ddd" />


Ja ho tenim:

<img width="751" height="521" alt="image" src="https://github.com/user-attachments/assets/011c799e-c8cc-4706-8cb9-ef85c5e50d00" />



Ara al client configurem la ip del server dns i fiquem la ip del server:

<img width="400" height="451" alt="image" src="https://github.com/user-attachments/assets/f9870683-03bd-48b4-a921-3e03b2f66a21" />


Anem a propietats del sistema:

<img width="406" height="471" alt="image" src="https://github.com/user-attachments/assets/c539e655-d101-4a13-9b55-6bb19d666ef1" />


Anem a "nom d'equip" i premem "cambiar el nom d'aquest equip o cambiar el domini o grup de treball":

<img width="409" height="489" alt="image" src="https://github.com/user-attachments/assets/835a04e1-89c7-439c-9d3c-0851b6bb26f8" />


Escrivim el nostre domini:

<img width="322" height="384" alt="image" src="https://github.com/user-attachments/assets/ee0bdfe5-a530-49db-b76b-ea8a02d2e2e2" />


Fiquem les nostres credencials:

<img width="448" height="326" alt="image" src="https://github.com/user-attachments/assets/fe1c6b25-ffe4-43bc-9024-9bdf552c9798" />


I finalment s'ha unit correctament al nostre domini:

<img width="615" height="394" alt="image" src="https://github.com/user-attachments/assets/52927282-48ed-48c6-b497-899985ce6c74" />


S'haur'a de reiniciar per aplicar els canvis:

<img width="350" height="173" alt="image" src="https://github.com/user-attachments/assets/27cd81d1-314c-4127-ac43-709eb83c2147" />

