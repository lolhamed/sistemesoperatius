## SPRINT 2 WINDOWS ##




## FASE 1: PREPARACIÓ DEL SISTEMA ##


Afegim un nou disc a la nostra màquina virtual:

<img width="696" height="451" alt="image" src="https://github.com/user-attachments/assets/a560d70c-4bb3-44b1-a96e-c4f156db51e2" />

Per donar mida:

<img width="690" height="445" alt="image" src="https://github.com/user-attachments/assets/9e38062f-4fc9-4a58-bd30-0c89a627ec8d" />


Fem click dret a la icona de windows i després fem click a administració de discs i després fem click a nou volum simple:

<img width="961" height="633" alt="image" src="https://github.com/user-attachments/assets/09c5a78c-fb57-4314-8e60-b8323228c8a0" />


Assignem la meitat per exemple:

<img width="497" height="390" alt="image" src="https://github.com/user-attachments/assets/0090f59f-a08e-4419-969d-2b2f09fb7faf" />


Configurem la partició anomenada "Dades":

<img width="497" height="395" alt="image" src="https://github.com/user-attachments/assets/2b2013f6-05ca-4185-a915-5322c0f5414b" />


El mateix amb la partició anomenada "Portable":

<img width="496" height="391" alt="image" src="https://github.com/user-attachments/assets/d70927e2-3d66-4598-9d9f-4a2d2e619837" />


Aqui tenim les particions que hem creat/configurat:

<img width="754" height="600" alt="image" src="https://github.com/user-attachments/assets/b9fcac2d-a42b-4345-9e6a-3cce82108d8b" />


Després anem a diskpart i dins de diskpart, fem la comanda "list volume", ens sortirà les particions que hem fet fins al moment:


<img width="746" height="309" alt="image" src="https://github.com/user-attachments/assets/5c35ad8d-6a62-4ad8-bada-c2b11a7cec1f" />



## FASE 2: QUOTES I USUARIS ##


Anem a l'explorador de fitxers i anem a l'apartat "Aquest equip", per veure les nostres particions que hem creat a la fase 1:

<img width="781" height="569" alt="image" src="https://github.com/user-attachments/assets/8025e556-65c9-4129-b10a-2c754e4bdfcc" />


Si anem a les propietats de la partició "dades" i després anem a l'apartat de quotes podrem establir un límit:

<img width="358" height="447" alt="image" src="https://github.com/user-attachments/assets/7e2aee50-ab2d-4e37-ae24-641f2d10d37d" />


El que hem fet és denegar espai de desic a usuaris que superen el límit de cuota, limitar espai de disc a 300MB i establir el nivell d'advertencia a 250mb:

<img width="362" height="447" alt="image" src="https://github.com/user-attachments/assets/5cf826c9-65fe-4203-874c-ab62c9e2ebcf" />


Acceptem el misstage que s'hi mostra:

<img width="406" height="205" alt="image" src="https://github.com/user-attachments/assets/ee049947-ec4f-446e-b39d-2acc5eaa3cdb" />


Ara crearen els comptes per als alumnes pero no em surt ja que estic utilitzant Windows 10 HOME  per tant ho faré amb el cmd :

<img width="991" height="531" alt="image" src="https://github.com/user-attachments/assets/6c499d4c-c26e-43c0-8705-f2ab89e16adf" />


Creem el usuari alumne1

<img width="501" height="61" alt="image" src="https://github.com/user-attachments/assets/436752ea-ae38-4264-9e9c-4b6beb0e9caf" />


Creem el usuari alumne2

<img width="528" height="128" alt="image" src="https://github.com/user-attachments/assets/e9314887-86d7-4d49-bb66-0ca1d048bc68" />


Ara creem el grup:

<img width="460" height="142" alt="image" src="https://github.com/user-attachments/assets/b682e6b0-8229-4096-9f94-41a8bb5206fd" />



I posteriorment afegim els usuaris al grup:

<img width="511" height="198" alt="image" src="https://github.com/user-attachments/assets/1d85de74-4894-4c78-b00f-3c0bff8710c2" />


Ara provarem les cuotes de disc que acabem de configurar i per aixó iniciarem sessió com a alumne1:


Estem a l'usuari alumne1:

<img width="299" height="379" alt="image" src="https://github.com/user-attachments/assets/329e6bba-41f8-4f71-8703-28faa0512ec3" />


Per fer la prova a l'usuari alumne1 creem un fitxer de 350mb:

<img width="802" height="160" alt="image" src="https://github.com/user-attachments/assets/b7959907-e649-4215-8564-4023ba4279f6" />


<img width="599" height="425" alt="image" src="https://github.com/user-attachments/assets/a2a55d55-a3ac-4ff7-a16e-05488fae7460" />

I ens surt un error de cuota al intentar afegir el fitxer al disc:

<img width="437" height="264" alt="image" src="https://github.com/user-attachments/assets/8729db0b-cdc3-4e37-8cb9-92f1d14cf433" />



## FASE 3: SCRIPT DE CÒPIA I AUTOMATITZACIÓ ##


Creem la partició "backups":

<img width="499" height="389" alt="image" src="https://github.com/user-attachments/assets/36f49764-c2b5-42b9-8403-3b0f19049379" />







