# Création du comportement du personnage 🏃‍♂️

Maintenant que nous avons notre monde de jeu, il est temps de donner vie à notre personnage. La création du comportement du personnage se fera en deux grandes parties : la définition des comportements et des variables, et l'écriture du code avec son animation.

# Comportements et variables 📝

 ## Comportement
Les comportements sont les actions que notre personnage peut effectuer, comme marcher, courir, sauter, attaquer, etc. Pour chaque comportement, nous devrons définir des variables qui contrôlent comment ce comportement fonctionne. Par exemple, pour le comportement de marche, nous pourrions avoir des variables pour la vitesse de marche, la direction de marche, etc.

Voici une liste des comportements et des variables que nous allons définir pour notre personnage :

Marcher : vitesse de marche, direction de marche
Attaquer : puissance de l'attaque, portée de l'attaque
Interagir : distance d'interaction, objet d'interaction

Notre personnage vas devoir hériter d'un comportement "TopDownMouvement" Mais tout d'abord ques qu'un top Down Mouvement?

un top-down movement est un type de mouvement dans les jeux vidéo qui se caractérise par une vue aérienne inclinée vers le bas, des contrôles permettant de déplacer le personnage ou l'objet dans toutes les directions, et une utilisation courante dans une variété de genres de jeux pour offrir une perspective stratégique et une meilleure visibilité.

On aimerait que le personnage n'ait pas d'inertie. Pour cela, on va effectuer une forte accélération vers une vitesse maximum lorsque l'on déplace notre personnage et une forte décélération lorsqu'on relâchera une touche de déplacement.

![TopDown](Images/TopDownPlayer.png)

## Variables

Pour l'instant, nous créerons seulement une variable qu'on appellera "PV" qui représentera notre nombre de vie de notre personnage. On reviendra plus tard dans les variables du personnage n'allons pas trop vite.

# Animation du personnage 🏃‍♂️

Maintenant, que notre personnage se déplace occupons-nous des animations. (Pour ma part, le personnage avait déjà les animations pré fait)

![CodeDeplacementPersonnage](Images/CodePersonageDeplacement.png)

# Création du comportement d'attaque du personnage ⚔️

Maintenant que notre personnage peut se déplacer dans le monde, il est temps de lui donner la possibilité de se défendre contre les monstres. Pour cela, nous allons créer un comportement d'attaque pour notre personnage.

## Comportement et variables 📝

Le comportement d'attaque de notre personnage sera déclenché lorsque le bouton d'attaque est pressé. Lorsque cela se produit, notre personnage va créer une épée et l'agiter dans la direction dans laquelle il fait face. Pour contrôler ce comportement, nous allons définir la variable suivante sur notre  :

Cooldown : Cette variable contrôle le temps entre chaque attaque. Après chaque attaque, notre personnage doit attendre un certain temps avant de pouvoir attaquer à nouveau.

## Code



