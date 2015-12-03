# Rapport RLI : connection avec données globales

## Etape de mise en communication des automates:

1. Charge le matériel avec la **bonne** adresse *MPI* pour l'automate *maitre*.
2. Faire la même chose avec l'autre automate *l'esclave*.
3. Aller dans MPI, connecter les 2 machines au cable *rouge*.
4. Charge les deux machines en même temps.

## Echange par données globales :

1. Aller dans MPI, faire un clique droit sur le câble *rouge* et cliquer sur *définir donnée globale*.
2. Ajouter nos 2 CPU.
3. Definir les données émétrices et réceptrices

> Exemple table des données globales:

|MAITRE(CPU 412-1)|ESCLAVE(CPU 412-1)|
|:------:|:-------:|
|>E0.0|A0.0|

## Echange de données globales avec DB :

1. Définir la DB chez le *maitre* avec les données voulues.
2. Définir la DB chez *l'escalve* avec *aucune* données mais le meme nombre que pour le maitre.
3. Accèder au menu donnée globale via le menu MPI et la cable *rouge* comme précédemment.

> Exemple table des données globales:

|MAITRE(CPU 412-1)|ESCLAVE(CPU 412-1)|Commentaire|
|:------:|:-------:|:------|
|>DB10.DBW0:3|DB15.DBW0:3| pour copier le contenu de la DB10 du maitre du *word0* au *word3* dans le DB15 de l'esclave.

##Auteur :
- Antar Saliba
- De Buyst Nicolas
- Gramaglia Alexis
