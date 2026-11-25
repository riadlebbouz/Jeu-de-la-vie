LE JEU DE LA VIE

<img width="653" height="306" alt="image" src="https://github.com/user-attachments/assets/14047dd8-7048-4f8d-8655-31ba8b404f87" />


- Présentation:

Imaginé en 1970 par le mathématicien John Horton Conway, le jeu de la vie n'a pas de joueur : on choisit un état de départ, puis on observe l'évolution.
L'univers est une grille de cellules, chacune vivante ou morte. À chaque génération, toutes les cellules sont mises à jour en même temps selon deux règles :

1. Une cellule morte qui a exactement 3 voisines vivantes devient vivante.
2. Une cellule vivante qui a 2 ou 3 voisines vivantes le reste, sinon elle meurt.

Le voisinage d'une cellule est formé des 8 cellules qui l'entourent.
Ces règles très simples produisent des comportements variés : structures stables, oscillateurs, vaisseaux qui se déplacent (comme le planeur) et canons qui en fabriquent indéfiniment, comme celui de l'image ci-dessus. Le jeu de la vie est d'ailleurs Turing-complet.

- Objectifs du projet:

Modéliser le jeu avec les concepts de la programmation orientée objet et les principes SOLID.
Séparer la logique métier de l'interface graphique.
Proposer un mode console et un mode graphique.
Valider le comportement par des tests unitaires.
Documenter la conception en UML (classes, séquence, activité).

- Fonctionnalités:

Chargement de l'état initial depuis un fichier texte.
Mode console : export de chaque itération dans un dossier <nom_du_fichier>_out.
Mode graphique (SFML) : simulation en temps réel, durée entre deux itérations réglable.
Arrêt quand la grille n'évolue plus ou après un nombre maximal d'itérations.
Test unitaire vérifiant la grille obtenue après un nombre donné d'itérations.

Auteurs:

Prénom NOM

Prénom NOM
