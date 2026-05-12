
## SPRINT 4: CONFIGURACIÓ DE PROGRAMARI BASE I SISTEMES D'EMMAGATZEMATGE EN WINDOWS ##


Primer, en una màquina virtual de windows servers 2022, afegim 3 discos adicionals, mínim per a fer el RAID 5 i que tinguin la mateixa mida els 3 discs:

<img width="1061" height="610" alt="image" src="https://github.com/user-attachments/assets/da2ffffb-7740-45a8-9222-c0d37b984587" />



Obrim la màquina i anem a disc manager:

<img width="411" height="215" alt="image" src="https://github.com/user-attachments/assets/b929ae3b-dae6-4c7e-9950-297f19ea415b" />




Després, quan ens surti l'assistent iniciem els discos com a MBR:

<img width="415" height="303" alt="image" src="https://github.com/user-attachments/assets/25e64f2f-23b2-41bb-8401-4517ad2a229c" />


Important, no formatar ni crear particions:

<img width="913" height="823" alt="image" src="https://github.com/user-attachments/assets/5e07fe9f-7f9c-40f2-b8aa-028d902d3369" />




Després farem click dret sobre un dels discos i farem click a "nou volum RAID-5":

<img width="914" height="473" alt="image" src="https://github.com/user-attachments/assets/d5fdda16-2f51-4269-989a-19aac534d139" />





Agreguem els discos restants (en el meu cas havia fet click dret al disc 1 per tant afegeixo el disc 2 i el disc 3)

<img width="489" height="403" alt="image" src="https://github.com/user-attachments/assets/851f20ca-8816-4faa-9523-1bc6ebabe34f" />




Assignem una lletra, en el meu cas és la lletra E:

<img width="492" height="399" alt="image" src="https://github.com/user-attachments/assets/57d05cdf-e0a4-4167-85be-a20176192ca5" />




Després, formatem el volum amb el sistema d'arxius NTFS, la mida de unitat d'assignació predeterminada i a la etiqueta de volum jo personalment li he ficat RAID5- Test:

<img width="490" height="404" alt="image" src="https://github.com/user-attachments/assets/a7f43523-b235-4006-9dee-4de158a78ab0" />




Final de la configuració:

<img width="493" height="401" alt="image" src="https://github.com/user-attachments/assets/eb2dd333-32c3-4a48-b82a-ad40160b7b16" />


Ara esperem a que el porcentatge arribi al 100& i una vegada acabada l'espera tindrem aixó:

<img width="914" height="845" alt="image" src="https://github.com/user-attachments/assets/91bc82bf-0ee0-4804-acb6-a79cb4f286e8" />


Aqui ho tenim:

<img width="913" height="589" alt="image" src="https://github.com/user-attachments/assets/a29b3b5d-c9d8-431c-ad65-797b91f418ef" />



Ara farem proves de funcionalitat:


Creem una carpeta de prova:

<img width="472" height="291" alt="image" src="https://github.com/user-attachments/assets/6100123b-aa24-45a2-8cb3-1ca49e02bda1" />


Ara afegim la carpeta a la RAID5:

<img width="693" height="213" alt="image" src="https://github.com/user-attachments/assets/66aab445-1045-41a6-b67a-ac69f49628c2" />


Com podem veure és totalment accesible:

<img width="899" height="244" alt="image" src="https://github.com/user-attachments/assets/7f83ed37-71fd-4f5f-9ed4-d0c3130b061c" />



Ara farem una simul·lació de fallada (treure un disc):

Tornem a l'administrador de discos i fem click dret a un disc, jo he escollit el disc 1:

<img width="299" height="355" alt="image" src="https://github.com/user-attachments/assets/c5c4f681-e1d6-4a7a-ad8b-21d675795c27" />


Disc 1 està desconnectat:

<img width="923" height="382" alt="image" src="https://github.com/user-attachments/assets/aacdaafe-8f12-4151-a71a-d01d567d8b0e" />


Tot i haver desconnectat el disc 1, encara tenim accés a la carpeta:

<img width="916" height="514" alt="image" src="https://github.com/user-attachments/assets/f7003142-c4f9-4c1a-93c3-1a57be9ccc74" />


<img width="894" height="499" alt="image" src="https://github.com/user-attachments/assets/92d1cc61-7c1a-4275-b218-ec1ed32198e4" />



Ara desconnectarem un altre disco, jo desconectaré el disc 2 i com podrem veure ens donarà error i no podrem accedir a la carpeta:

<img width="913" height="525" alt="image" src="https://github.com/user-attachments/assets/0b869c03-5b16-4d3d-9aec-7cb0268bc30e" />


Ara fem click dret als discos que acabem de desconnectar i fem click a "en línia":

<img width="906" height="477" alt="image" src="https://github.com/user-attachments/assets/58706c24-05a2-408a-8921-7a33f825d052" />


Després fem click dret a la linia blava i fem click a "reactivar volum":

<img width="881" height="489" alt="image" src="https://github.com/user-attachments/assets/e317dc98-66c2-440f-8b8d-34c5eb615263" />


Després d'haver-se sincronitzat, els raids estaràn en estat correcte:

<img width="919" height="491" alt="image" src="https://github.com/user-attachments/assets/ef1c34fd-5d65-4f35-bb30-e8d88697977e" />


I també tindrem accés a la carpeta que prèviament hem creat:

<img width="900" height="507" alt="image" src="https://github.com/user-attachments/assets/854b91ba-14fd-416c-acec-a1551895ee79" />

<img width="885" height="284" alt="image" src="https://github.com/user-attachments/assets/78b2ec8d-fa3d-4a35-a5fa-5534b2ecd368" />

<img width="724" height="351" alt="image" src="https://github.com/user-attachments/assets/9aa951c4-c19f-4cfe-8b9e-c5c4b5e289b4" />



Per tant podem concluïr que RAID5 tolera com a molt la fallada d'un disc, NO és una còpia de seguretat i NO funciona si fallen els dos discs com hem vist abans.





