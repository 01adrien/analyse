<link rel="stylesheet" href="../style.css"/>

[<span class="icon-big">&#8592;</span>](./../2-3-backlog.md)

# User storie reservation instrument

En tant que **musicien** je veux pouvoir réserver un créneaux de l'instrument de mon choix. <br>
Afin d'aller en jouer chez son propriétaire.

## Condition

L'utilisateur doit avoir un compte **musicien** et etre loggé.<br>
Sinon une popup s'ouvre lui demandant de se logger

## Parcours utilisateur

Apres avoir selectionné un instrument l'utilisateur clique sur le bouton réservation de la page détail de l'instrument.<br>
Un composant calendrier s'ouvre et en cliquant sur un jour, il sera redirigé vers formulaire de réservation.<br>
L'utilisateur choisit alors un créneau pour sa **réservation**<br>
Une fois l'étape resérvation terminée un message recapitulatif sera envoyé dans la rubrique message de son espace personnel.

## Regles metier

La réservation n'a pas beoin de validation cotè proprietaire<br>
Le début de creneau ne peut pas être aprés la fin<br>
Une reservation ne peut être pris le jour meme.<br>
Tant qu'il y a des créneaux de libre l'instrument est disponible
