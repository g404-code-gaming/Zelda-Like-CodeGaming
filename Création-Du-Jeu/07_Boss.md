# Boss

Pour conclure le travail sur ce jeu Zelda et proposer une fin de jeu, nous allons ajouter un Boss à notre Donjon.

Le Boss est un ennemi spécial, très difficile, doté d'attaque spéciales. 

![image combat de fin]() 

## Préparation du boss 

### 1 - Création du boss 

Ajoutez un objet **Boss** à votre niveau de Donjon. 

![image boss]() 

Ne Placez pas le Boss dans la scène pour le moment, nous allons le faire apparaître par le programme. 

### 2 - Apparition du boss et lancement du combat de fin 

Dans notre jeu, Le boss apparait lorsque le personnage déplace une entrée. Il se retrouve enfermé et le boss apparaît. 

![image fin de niveau]() 

Ajoutez une Box de déclenchement **Trigger_Box**. Il s'agit d'une zone invisible qui va détecter le personnage du joueur et déclencher l'apparition du boss et le fermture de la salle.

Vous pouvez créer cet objet à partir de zéro. 

![image trigger_box]() 

Placez cet objet à l'entrée de votre salle de boss : il faut que le joueur soit obligé de la traverser pour entrer.

Ajoutez ensuite le programme pour que, lorsque votre joueur touche la **Trigger_box**, cela ferme une porte derrière lui et fasse apparaître le boss.

> NOTE : les éléments en Vert sur l'image suivante sont des coordonnées. Adaptez-les à votre niveau pour faire apparaître les objets au bon endroit.

![image code trigger box]() 

## programmation du Boss

