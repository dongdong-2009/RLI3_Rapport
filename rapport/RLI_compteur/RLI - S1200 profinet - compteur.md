# RLI : S1200 profinet : compteur
===================================

## Ajouter la station avec l'affichage et bouton: (ST1)

!attention! : encoder les bonnes IP

![image](Station1.png)
### Ajouter IHM (IHM1)
!attention! : encoder les bonnes IP
IHM : Ecran 6' : KTP600 Basic PN

![image](hm1.png)

## Ajouter la station avec le compteur(ST2)
!attention! : encoder les bonnes IP
station : SIMATIC S7-1200 CPU 1214 AC/DC/RLY

![image](Station2.png)
### Ajouter IHM (IHM2)
!attention! : encoder les bonnes IP
IHM : Ecran 6' : KTP600 Basic PN
![image](hm2.png)

## Vue sur IHM1

![image](vueHm1.png)

## Réseau :
![image](réseau.png)

## Connecter les machines :

Il faut lié les prise ethernet au réseau et ce pour chaque machine

## Liaison des boutons avec variables
1. cliquer droit sur le bouton 
2. propriete 
3. evenement
4. appuyer
5. action : inverser bit
6. lié la variable a celle correspondante dans le ST2

![image](configBoutton.png)

##Connecter le label a la valeur de compteur
1. cliquer droit sur le bouton 
2. propriete 
2. dans générale 
3. section process
4. associe la bouton à la variable du compteur dans ST2

![image](affichageValeur.png)
## Code OB1 de la ST2


![image](codeOB1station2.png)

## Put et Get
Les instructions put et get se trouver dans la section communication a gauche puis dans le dossier *communication S7*

image

- REQ : ```true``` pour activer l'échange
- ID : valeur que l'on veut
- ADDR_1 : ```P#DB1.DBX0.0 BYTE 2 ``` on veut envoyer ```SD_1``` dans la DB1 à l'adresse 0.0 d'une taille de 2 bytes
- SD_1 : la valeur que l'on veut envoyer

### Configurer la liaison 

1. cliquer sur le block put
2. aller propriete
3. configuration
4. et encoder le nom du partenaire

image

##Problème rencontrer :

- Si les IHM ne sont pas reconnu et que l'Ip est correcte :
	+ quitter la vue la racine de IHM pour revenir sur la vue *loader*