Le jeu de la vie

Implémentation orientée objet en C++ de l'automate cellulaire de John Conway.

Afficher l'image

Le canon à planeurs de Gosper. Animation de Kieff, CC BY-SA 3.0, via Wikimedia Commons.

Présentation

Imaginé en 1970 par le mathématicien John Horton Conway, le jeu de la vie n'a pas de joueur : on choisit un état de départ, puis on observe l'évolution.

L'univers est une grille de cellules, chacune vivante ou morte. À chaque génération, toutes les cellules sont mises à jour en même temps selon deux règles :

Une cellule morte qui a exactement 3 voisines vivantes devient vivante.
Une cellule vivante qui a 2 ou 3 voisines vivantes le reste, sinon elle meurt.

Le voisinage d'une cellule est formé des 8 cellules qui l'entourent.

Ces règles très simples produisent des comportements variés : structures stables, oscillateurs, vaisseaux qui se déplacent (comme le planeur) et canons qui en fabriquent indéfiniment, comme celui de l'image ci-dessus. Le jeu de la vie est d'ailleurs Turing-complet.

Objectifs du projet
Modéliser le jeu avec les concepts de la programmation orientée objet et les principes SOLID.
Séparer la logique métier de l'interface graphique.
Proposer un mode console et un mode graphique.
Valider le comportement par des tests unitaires.
Documenter la conception en UML (classes, séquence, activité).
Fonctionnalités
Chargement de l'état initial depuis un fichier texte.
Mode console : export de chaque itération dans un dossier <nom_du_fichier>_out.
Mode graphique (SFML) : simulation en temps réel, durée entre deux itérations réglable.
Arrêt quand la grille n'évolue plus ou après un nombre maximal d'itérations.
Test unitaire vérifiant la grille obtenue après un nombre donné d'itérations.
Format du fichier d'entrée

La première ligne donne la taille de la grille (lignes puis colonnes). Elle est suivie de la matrice des états : 1 pour une cellule vivante, 0 pour une cellule morte.

text
5 10
0 0 1 0 0 0 0 0 0 0
0 0 0 1 0 0 0 0 0 0
0 1 1 1 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0
0 0 0 0 0 0 0 0 0 0

Cet exemple contient un planeur.

Installation

La bibliothèque SFML est nécessaire pour le mode graphique :

bash
sudo apt-get install libsfml-dev
git clone <URL_DU_DEPOT>
cd <NOM_DU_DEPOT>
Compilation et utilisation

À adapter selon votre système de build et vos options.

bash
# Compilation
make

# Mode console
./life chemin/vers/fichier.txt --console

# Mode graphique
./life chemin/vers/fichier.txt --gui
Architecture

Le diagramme de classes est disponible dans le dossier docs/.

Diagramme de classes

Le projet est organisé en couches indépendantes : logique du jeu (jeu, grille, cellules et états), règles d'évolution, lecture et écriture des fichiers, et affichage (console et SFML).

Tests
bash
make test
Références
Le jeu de la vie sur Wikipédia
LifeWiki
Documentation SFML
Auteurs
Prénom NOM
Prénom NOM
