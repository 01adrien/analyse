<link rel="stylesheet" href="../style.css"/>

[<span class="icon-big">&#8592;</span>](./../2-3-users-stories.md)

# User storie reservation instrument

En tant que **musicien** je veux pouvoir reserver un creneaux de l'instrument de mon choix. <br>
Afin d'aller en jouer chez son proprietaire.

## Condition

L'utilisateur doit avoir un compte **musicien** et etre loggé.<br>
Sinon une popup s'ouvre lui demandant de se logger

## Parcours utilisateur

Apres avoir selectionné un instrument l'utilisateur clique sur le bouton reservation de la page detail de l'instrument.<br>
Un composant calendrier s'ouvre et en cliquant sur un jour, il sera redirigé vers formulaire de reservation.<br>
L'utilisateur choisit alors le jour et les horaires du **creneau**<br>

## Regles metier

Le debut de creneau ne peut pas etre aprés la fin<br>
Un **creneau** ne peut etre pris le jour meme.