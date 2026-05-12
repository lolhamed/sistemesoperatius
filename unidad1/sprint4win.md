
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

