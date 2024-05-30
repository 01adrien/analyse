<link rel="stylesheet" href="../style.css"/>

[<span class="icon-big">&#8592;</span>](./../2-3-backlog.md)

# User storie creation instrument 

En tant que propriétaire je veux pouvoir ajouter des instruments sur l'app.<br>
Afin que des musiciens puissent venir en jouer chez moi<br>

## Condition

je dois avoir un compte **proprietaire** sur l'application et etre loggé avec.<br/>
Sinon une popup s'ouvre demandant de faire le necessaire.

## Parcours utilisateur 

Une fois loggé en **proprietaire** je vais dans la rubrique de mon espace personnel "ajout instrument"<br>
Un formulaire s'ouvre avec une série d'input á remplir:
- le nom de l'instrument (titre de l'annonce)
- sa famille (vent, corde...)
- L'instrument (guitare, piano...)
- sa marque (kawai, fender...)
- Une description de l'instrument
- Un uploader de photos (photos de l'instrument)
- le choix des dispo par jours.

Une fois ces inputs remplis correctement, un message est envoyé dans ma boite msg (recap création)<br>
L'instrument est en attente de validation par l'admin et un message sera envoyé en cas de refus ou acceptation.<br>
En attendant l'instrument á le statut 'en attente'.


## Regles metier

Les familles, marques et types d'instrument sont á choisir dans un menu déroulant.
L'utilisateur ne peut pas les ecrire coontrairement au nom et description.<br>
Le nom de l'instrument ne peut depasser 50 caractéres et la description 1000 caractéres.<br>
Et ne pas peuvent être nul<br>
Un maximum de 5 photos par instrument<br>
L'input suivant doit être 'disable' si celui d'avant n'est pas rempli.<br>
L'amplitude horaire des creneaux est de 9h a 22h tous les jours de la semaine<br>
