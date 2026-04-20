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










