# S400 - S300 : profinet :
======================


## Configurer S400 :

- configuration "normal"
- lorsque l'on ajouter le *CP 443-1 Advanced-IT* 
	- il faut cliquer sur **nouveau** 
	- cliquer sur **OK**

- charge !

## Configurer S300 :
- changer le cable gris et le mettre dans le S300 
- configuration normal 
- ![](config300.png)
- lorsque l'on rajouter le *CPU315-2-DP v2*, il ne faut rien configurer. Il faut directement cliquer sur *OK*
- pour le *SM374*, c'est -> *SM 323 DI8/D08xDC24V/0,5V*
- lorsque l'on rajoute le *CP 341-1 Advanced-IT* il faut selectionne le réseau que l'on a crée avant dans le *S400* et changer l'@IP du CP
- ![](ip.png)
- charge 

## Configuration réseau 

- aller dans *MPI* pour configurer le réseau
- connecter les 2 stations (les CP) au cable ethernet
- ![](mpi.png)
- mettre le cable gris sur le S400 charge la config dans S400
- changer le cable gris et cable sur S300
- charge dans S300
- cliquer la *CPU 315-2 DP* et double click sur l'ID 
	- ![](liaison.png)
	- liaison S7
	- mettre l'ID a 1
	- faire la meme manip pour le S400 avec le meme ID

puis recharger dans chaquqe machine

## Put et get 

### PUT S400
Ou ?

- Bibliotheque
- Standard lib
- System fonction bock
- Il faut choisir le *SFB15 PUT*

![](PUT_400.png)

- *REG* : action qui transmet les infos, ici la memento de cadence
- *ID* : l'ID encode dans la laison MPI
- *ADDR_1* : l'adresse ou envoye les informations
- *SD_1* : les données que l'on veut envoyer sur *ADDR_1*




### GET S400
Ou ?

- Bibliotheque
- Standard lib
- System fonction bock
- Il faut choisir le *SFB14 PUT*

![](get_400.png)

- *REG* : action qui receptionne les infos, ici la memento de cadence
- *ID* : l'ID encode dans la laison MPI
- *ADDR_1* : l'adresse ou recupere les informations
- *RD_1* : ou stocké les information recues

### Compteur S300


![](compteur_300.png)

- ZV : pour incrementer
- ZR : pour decremneter
- E 0.7 pour reset





