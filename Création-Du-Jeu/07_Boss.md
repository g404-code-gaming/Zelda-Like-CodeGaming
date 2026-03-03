# Boss

Pour conclure le travail sur ce jeu Zelda et proposer une fin de jeu, nous allons ajouter un Boss à notre Donjon.

Le Boss est un ennemi spécial, très difficile, doté d'attaques spéciales.

![image combat de fin](/image/7_image_combat_final.JPG) 

## Préparation du boss 

### 1 - Création du boss 

Ajoutez un objet **Boss** à votre niveau de Donjon. 

![image boss]() 

Ne placez pas le Boss dans la scène pour le moment, nous allons le faire apparaître par le programme.

Ajoutez le Boss aux groupes suivants :
  - **Danger** : Pour que le Boss puisse blesser le Joueur en le touchant.
  - **Ennemi** : Pour que le Boss puisse être ciblé et touché par l'épée du joueur.

Enfin, définissez les points de vie du Boss (personnellement, j'en ai mis 25). 

### 2 - Apparition du boss et lancement du combat de fin 

Dans notre jeu, le boss apparaît lorsque le personnage se déplace à travers une entrée. Il se retrouve enfermé et le boss apparaît.

![image fin de niveau]() 

Ajoutez une Box de déclenchement Trigger_Box. Il s'agit d'une zone invisible qui va détecter le personnage du joueur et déclencher l'apparition du boss et la fermeture de la salle.

Vous pouvez créer cet objet à partir de zéro.

![image trigger_box]() 

Placez cet objet à l'entrée de votre salle de boss : il faut que le joueur soit obligé de la traverser pour entrer.

Il s'agit d'une zone "fictive" : elle est concrètement invisible pour le joueur. Modifiez son opacité à 0 pour qu'elle ne soit pas visible du joueur.

Ajoutez ensuite le programme pour que, lorsque votre joueur touche la **Trigger_box**, cela ferme une porte derrière lui et fasse apparaître le boss.

> NOTE : les éléments en vert sur l'image suivante sont des coordonnées. Adaptez-les à votre niveau pour faire apparaître les objets au bon endroit.

![image code trigger box]() 

Testez votre programme pour vérifier que le boss et le mur apparaissent bien lorsque votre joueur entre dans la salle de fin. 

## Programmation du Boss

Tout d'abord, ajoutons un programme pour mettre à jour la barre de PV du boss et éviter qu'il ne puisse traverser les murs.

![boss code]() 

Pour construire un Boss intéressant, plusieurs méthodes sont possibles :

Dans la partie qui suit, plusieurs actions sont possibles pour le boss, elles ne sont pas toutes obligatoires : il est même possible d'en ajouter d'autres autant que nécessaire pour un adversaire intéressant et vivant.

### BONUS - Déplacement du boss 

![image boss_deplacement]() 

Pour éviter que le boss ne reste immobile, il est possible de lui ajouter un déplacement aléatoire dans le niveau.

Lors de l'apparition du Boss, ajoutez un Chronomètre qui servira à déplacer le boss au fil du temps.

![image boss_deplacement_code1]() 

Ensuite, ajoutez le programme qui le fait changer de direction à chaque fois que le chronomètre dépasse une certaine valeur.

> Attention, les paramètres en vert sont à adapter à votre niveau : ce sont des coordonnées.

![image boss_deplacement_code2]() 

Testez votre Boss pour voir s'il se déplace de manière erratique sur votre niveau.

### BONUS - Lancé de projectile 

Pour permettre au boss d'attaquer le joueur à distance, il est possible de lui ajouter un lancer de projectile.

![image boss_attaque]() 

Ajoutez à la scène un **projectile** pour votre boss.

Ajoutez ensuite le programme pour initier le chronomètre permettant de tirer des projectiles.

![image boss_attaque_code1]() 

Ajoutez ensuite le programme pour que le Boss tire des projectiles selon la valeur de son Chronomètre.

![image boss_attaque_code2]() 

> Note : vous pouvez aussi utiliser le comportement pour Tirer des balles.

Testez votre programme pour vérifier qu'il fonctionne correctement : normalement, votre Boss tire des projectiles vers le joueur à intervalle régulier.

### BONUS - Invocation d'explosion 

Une autre attaque possible pour le boss serait d'invoquer une explosion qui force le joueur à être constamment en déplacement pour ne pas mourir. 

![image boss_explosion]() 

Ajoutez à la scène deux objets : 
  - un objet **bombe** qui va être invoqué par le Boss sur la position du joueur.
  - un objet **Explosion** : c'est la bombe qui explose pour blesser le joueur.

Ajoutez ensuite le programme pour initier le chronomètre permettant d'invoquer l'explosion. 

![image boss_explosion_code1]() 

Ajoutez ensuite le programme pour que le Boss invoque des explosions selon la valeur de son Chronomètre. 

![image boss_explosion_code2]() 

Testez votre programme pour vérifier qu'il fonctionne correctement : le Boss invoque sur le joueur une bombe, qui, quelques secondes plus tard, explose.

Avec les éléments suivants, vous avez tout ce qu'il faut pour faire un Boss efficace.
