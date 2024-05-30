
<link rel="stylesheet" href="style.css"/>

[<span class="icon-big">&#8592;</span>](./2-analyse.md)


# Modelisation de base de données

Dans cette partie je vais modeliser la base de données en fonction des entités metiers de l'app<br>
Les 4 grandes entités de cette application sont :
- les utilisateurs
- les réservations 
- les instruments
- la messagerie interne

Les autres entités sont surtout utilisees pour completer les 3 principales (photo, role, creneau...).<br>
Egalement afin d'organiser les données et d'eviter les doublons.<br>

La modelisation sera realisée sur visual paradigm<br>


<br>

<img src="./database/play-my-house.jpg" class="img-center">
<br>

## Description du schema

tous les champs qui ne sont pas indiqués 'nullable' sont requis.

### <u>reservation</u>

cette table représente les informations d'une réservation d'instrument pris par un musicien.
On y retrouve la date de la réservation, l'id du musicien et celui de l'instrument désire. <br>

### <u>instrument</u>

cette table représente les informations d'un instrument au préalable ajouté par un proprietaire.
On y retrouve divers champs concernant ses caractéristiques (marque, famille)
Il est également lié á une liste de photos et á sa 'timeline'. (liste de creneaux)
Pour être 'réservable' son status doit être 'accepté' ( par l'admin ).
 
### <u>utilisateur</u>

cette table represente un utilisateur quelque soit son type. ( proprietaire, musicien, admin )
le champ 'role_id' sert justement a les distinguer.
Pour un musicien les champs télephone et adresse ne sont pas obligatoire.
Un proprietaire devra les remplir á son inscription sur l'app.


### <u>message</u>

cette table représente les messages que les utilisateurs peuvent s'envoyer entre eux.<br>
Pour par exemple avoir des informations sur un instrument ou simplement dire bonjour..
On y retrouve évidement le contenu du message, sa date et l'id de l'expediteur et celui du destinataire, pour pouvoir les afficher dans L'UI.

### <u/>instrument status</u>

cette table représente le status de l'instrument.<br>
au moment ou son proprietaire le crée il est 'en attente', si l'admin l'accepte le status sera 'validé' sinon 'refusé'.<br>
Ce status n'est pas utilisé dans la gestion des reservations d'un instrument mais valide seulement sa conformité sur l'app<br>

### <u>creneau</u>

Cette table représente un creneau de disponibilitè d'instrument.<br>
Ces creneaux composent la 'timeline' de l'instrument et sont renseignès par le proprietaire au moment de l'ajout de l'instrument.<br>
Ex:<br>
le proprietaire veut que pour le jeudi son instrument soit dispo de 10h á 12h et de 14h á 16h.<br>
Il créera renseignera donc 2 creneaux pour ce jour.
