<link rel="stylesheet" href="../style.css"/>

[<span class="icon-big">&#8592;</span>](./../2-3-backlog.md)

# User storie creation instrument 

En tant que proprietaire je veux pouvoir ajouter des instruments sur l'app.<br>
Afin que des musiciens puissent venir en jouer chezmoi<br>

## Condition

je dois avoir un compte **proprietaire** sur l'application et etre loggé avec.<br/>
Sinon une popup s'ouvre demandant de faire le necessaire.

## Parcours utilisateur 

Une fois logge en **proprietaire** je vais dans la rubrique de mon espace personnel "ajout instrument"<br>
Un formulaire s'ouvre avec une serie d'input a remplir:
- le nom de l'instrument (titre de l'annonce)
- sa famille (vent, corde...)
- L'instrument (guitare, piano...)
- sa marque (kawai, fender...)
- Une description de l'instrument
- Un uploader de photos (photo de l'instrument)
- le choix des dispo par jours.

Une fois ces inputs remplis correctement, un message est envoye dans ma boite msg(recap creation)<br>
L'instrument est en attente de validation par l'admin et un message sera envoyer en cas de refus ou acceptation.



## Regles metier

Les familles, marques et types d'instrument sont a choisir dans un menu deroulant,
Issus de la base de donnees.
L'utilisateur ne peut pas les ecrires coontrairement au nom et description.<br>
Le nom de l'instrument ne peut depasser 50 caracteres et la description 1000 caracteres. 
Et de peuvent etre nul<br>
Un maximum de 5 photos par instrument<br>
L'input suivant doit etre 'disable' si celui d'avant n'est pas rempli.<br>
L'amplitude horaires de creneaux est de 9h a 22h tous les jours de la semaine<br>
