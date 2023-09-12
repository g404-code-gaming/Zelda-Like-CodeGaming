# Création d'ennemis 🧟‍♂️

Maintenant que nous avons notre personnage et notre carte, il est temps d'ajouter des ennemis pour rendre notre jeu plus intéressant. Dans ce tutoriel, nous allons créer 4 types d'ennemis : BigDemon, RockHead, AngryPig et Necromancer.

## BigDemon 👹
BigDemon est un ennemi qui change de direction lorsqu'il heurte un mur. Cela signifie que si BigDemon se déplace vers le haut et heurte un mur, il commencera à se déplacer vers le bas. Cela permet à BigDemon de se déplacer de manière imprévisible, ce qui le rend plus difficile à éviter pour le joueur.

## Variable
Direction : La direction dans laquelle BigDemon se déplace actuellement.
Moved : Un booléen qui indique si BigDemon a déjà changé de direction lors de la collision actuelle.

[image]

## Code 
Tout d'abord, nous allons nous occuper de ces déplacements, on aimerait que l'ennemie face seulement des mouvements de gauche à droite ou de haut en bas. Ceci sera notre ennemi le plus faible et basique pour donner une approche croissante dans la difficulté du jeu afin de ne pas décevoir les joueurs de mourir ou de tomber directement sur un ennemi compliqué à tué.

[Image code deplacement]

Ensuite nous allons gérer les événement telle que la collision avec l'épée pour tué l'ennemie et si l'ennemie nous touche.

Tout d'abord, commençons par le plus simple, c'est-à-dire si l'épée est en contact avec notre ennemie, on va tout simplement supprimer notre ennemie. Rien de plus simple !!

Par la suite, on vas gérer la collision de notre ennemis avec notre personnage.
[Image code attaque ennemie et mort]

## RockHead 🪨
RockHead est un ennemi qui change d'animation lorsqu'il est touché. Cela signifie que lorsque le joueur attaque RockHead, l'animation de RockHead change pour montrer qu'il a été touché. De plus, la vie de RockHead est réduite chaque fois qu'il est touché. Si la vie de RockHead atteint 0, il est supposé être détruit.


## AngryPig 🐷
AngryPig est un ennemi qui charge le joueur lorsqu'il est en colère. Cela signifie que lorsque AngryPig est en colère, sa vitesse de déplacement augmente et il se dirige directement vers le joueur. Cela rend AngryPig plus dangereux lorsque le joueur l'attaque, car il peut rapidement se rapprocher du joueur et l'attaquer.

## Necromancer 💀
Necromancer est un ennemi qui tire un laser sur le joueur lorsqu'il est en charge. Cela signifie que lorsque Necromancer est en charge, il se déplace vers une position spécifique et tire un laser en direction du joueur. Cela rend Necromancer dangereux à distance, car il peut attaquer le joueur même s'il est loin de lui.
