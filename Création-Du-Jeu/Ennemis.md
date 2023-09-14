# Création d'ennemis 🧟‍♂️

Maintenant que nous avons notre personnage et notre carte, il est temps d'ajouter des ennemis pour rendre notre jeu plus intéressant. Dans ce tutoriel, nous allons créer 4 types d'ennemis : BigDemon, RockHead, Necromancer et AngryPig.

## BigDemon 👹
![BigDemon](Images/BigDemon.png)
BigDemon est un ennemi qui change de direction lorsqu'il heurte un mur. Cela signifie que si BigDemon se déplace vers le haut et heurte un mur, il commencera à se déplacer vers le bas. Cela permet à BigDemon de se déplacer de manière imprévisible, ce qui le rend plus difficile à éviter pour le joueur.

## Variable
Direction : La direction dans laquelle BigDemon se déplace actuellement.
Moved : Un booléen qui indique si BigDemon a déjà changé de direction lors de la collision actuelle.

![VariableBigDemon](Images/VariableBigDemon.png)

## Code 
Tout d'abord, nous allons nous occuper de ces déplacements, on aimerait que l'ennemie face seulement des mouvements de gauche à droite ou de haut en bas. Ceci sera notre ennemi le plus faible et basique pour donner une approche croissante dans la difficulté du jeu afin de ne pas décevoir les joueurs de mourir ou de tomber directement sur un ennemi compliqué à tué.

![DeplacementBigDemon](Images/DeplacementBigDemon.png)

Ensuite nous allons gérer les événement telle que la collision avec l'épée pour tué l'ennemie et si l'ennemie nous touche.

Tout d'abord, commençons par le plus simple, c'est-à-dire si l'épée est en contact avec notre ennemie, on va tout simplement supprimer notre ennemie. Rien de plus simple !!

![BigDemonDie](Images/DieBigDemon.png)

Par la suite, on va gérer la collision de notre ennemi avec notre personnage. Avant tout de chose pour éviter de perdre tous ces PV d'un seul coup, on va rajouter sur notre personnage une variable booléenne qui définira si on est en état d'invincibilité ou non.

![VariableDInvincibilité](Images/InvincibilitéCharacter.png)

Puis maintenant retournons sur notre ennemie qui attend de pouvoir nous tuer. Lors d'une collision de notre personnage contre l'ennemie, on fera perdre 1 PV à notre personnage et nous fera passer en état d'invincibilité pendant un certain temps.

![BigDemonAttaque](Images/BigDemonAttaque.png)

## RockHead 🪨

![RockHead](Images/RockHead.png)

RockHead est un ennemi qui change d'animation lorsqu'il est touché. Cela signifie que lorsque le joueur attaque RockHead, l'animation de RockHead change pour montrer qu'il a été touché. De plus, la vie de RockHead est réduite chaque fois qu'il est touché. Si la vie de RockHead atteint 0, il est supposé être détruit.

## Variable

Hit : Un booléen qui indique si RockHead a été touché par une attaque.
Life : Le nombre de points de vie restants de RockHead.

![RockHeadVariables](Images/VariableRockHead.png)

## Code

Ce code commence par changer l'animation de RockHead à 1. Cela pourrait être l'animation que RockHead utilise lorsqu'il n'est pas en train d'être attaqué.

Ensuite, le code vérifie si l'épée du joueur (SteelRapier24) est en collision avec RockHead, si RockHead n'a pas déjà été touché (la variable Hit est False) et si RockHead a encore de la vie (la variable Life est supérieure à 0).

Si toutes ces conditions sont remplies, cela signifie que le joueur a réussi à attaquer RockHead. Le code réduit alors la vie de RockHead de 1 (ce qui représente les dégâts de l'attaque du joueur) et marque RockHead comme ayant été touché (la variable Hit devient True).

Et enfin lorsque RockHead n'a plus de Life on supprime l'objet.

Voici le résultat que vous devriez obtenir.

![RockHeadCode](Images/CodeRockHead.png)

## Necromancien 💀
Necromancien est un ennemi qui tire un laser sur le joueur lorsqu'il est en charge. Cela signifie que lorsque Necromancer est en charge, il se déplace vers une position spécifique et tire un laser en direction du joueur. Cela rend Necromancer dangereux à distance, car il peut attaquer le joueur même s'il est loin de lui.

## Variables

Charge : Un booléen qui indique si Necromancer est en train de charger son attaque.
Cooldown

## AngryPig 🐷
AngryPig est un ennemi qui charge le joueur lorsqu'il est en colère. Cela signifie que lorsque AngryPig est en colère, sa vitesse de déplacement augmente et il se dirige directement vers le joueur. Cela rend AngryPig plus dangereux lorsque le joueur l'attaque, car il peut rapidement se rapprocher du joueur et l'attaquer.

