# citadelinvaders

Auteures : Emma REDOR & Emma DEMURE   -   Groupe de TP n°1 de PO

Brève description du jeu :

« Citadel Invaders » est un jeu de type TowerDefense, le but étant de protéger à tout prix son château des vagues d’ennemis voulant l’envahir en plaçant diverses tours de défense (tour d’archer, tour de neige, tour de feu, tour lanceuse de bombes, tour laser) sur le chemin y menant. Cependant, vous devez simultanément gérer votre bourse d’or sachant que pour chaque ennemi tué, vous gagnerez quelques pièces. 


/// COMMANDES /// :

Appuyez sur S : Commencer une partie/Mettre sur pause.
Appuyez sur A : sélectionner la Tour d’Archer (50 gold).
Appuyez sur B : sélectionner la Tour de Bombe (50 gold).
Appuyez sur F : sélectionner la Tour de Feu (120 gold).
Appuyez sur I : sélectionner la Tour de Neige (120 gold).
Appuyez sur L : sélectionner la Tour de Laser (200 gold).
Appuyez sur E : faire évoluer une tour (40 gold).
Clickez où vous le souhaiter pour construire ou faire évoluer une tour précise !

A chaque fois qu’une commande est choisie par le joueur, elle s’affiche dans la console.


/// TOURS /// :

Il y a 5 types de tours différents. Elles ont toutes la possibilité d’être upgradées (elles gagnent toutes 10 points de vie en plus et leur périmètre d’attaque augmentent de 0.01 x le level actuel de la tour). Aussi, lorsque la tour est complètement  ou partiellement détruite par les ennemis, il y a possibilité de la réparer et de restaurer tous ses PV moyennant ainsi un peu d’agent à savoir si la tour est encore fonctionnelle : ses PV restant en gold sinon ses PV maximum + son level x 10 en gold. 
En survolant un tour avec la souris, il est possible de connaître son niveau actuel (affichage direct sur l’écran de jeu).
Si le joueur n’a pas assez d’argent, la console l’avertit par un message : « Not enough gold ». 
Si la tour possède une jauge de vie déjà remplie, il en est de même : « Tower’s hp are maximum. ». Aussi, si la tour ne peut pas excéder un certain level, le joueur en est aussi informé via la console.

-> Tour d’archer (ArrowTower) :

- coût : 50€
- points de vie : 15 PV
- temps de rechargement : 15
- périmètre d’attaque : 0.3
- id : 1 (sert à identifier le type de la tour dans la classe Projectile)
- particularité : tire de façon fluide sur les ennemis avec des flèches (un projectile de base dont la vitesse est égale à 0.02 + le level de la tour d’archer x 0.001 et dont la capacité d’attaque est de 4 + le level actuel de la tour d’archer)

-> Tour de bombe (BombTower) :

- coût : 60€
- points de vie : 10 PV
- temps de rechargement : 20
- périmètre d’attaque : 0.2
- id : 2 (sert à identifier le type de la tour dans la classe Projectile)
- particularité : tire à intervalle régulier sur les ennemis avec des bombe (un projectile dont la vitesse est égale à 0.04 + le level de la tour d’archer x 0.001 et dont la capacité d’attaque est de 8 + le level actuel de la tour d’archer)

-> Tour de feu (FireTower) :

- coût : 120€
- points de vie : 8 PV
- temps de rechargement : 100
- périmètre d’attaque : 0.2
- id : 4  (sert à identifier le type de la tour dans la classe Projectile)
- particularité : tire à intervalle régulier sur les ennemis avec des boules de feu (un projectile dont la vitesse est égale à 0.01 + le level de la tour d’archer x 0.001 et dont la capacité d’attaque est de … + le level actuel de la tour d’archer)

-> Tour de neige (IceTower) :

- coût : 120€
- points de vie : 2 PV
- temps de rechargement : 100
- périmètre d’attaque : 0.2
- id : 3  (sert à identifier le type de la tour dans la classe Projectile)
- particularité : tire à intervalle régulier sur les ennemis avec des flocons (un projectile dont la vitesse est égale à 0.01 + le level de la tour d’archer x 0.001 et dont la capacité d’attaque est de … + le level actuel de la tour d’archer)

-> Tour de laser (LaserTower) :

- coût : 200€
- points de vie : 5 PV
- temps de rechargement : 0
- périmètre d’attaque : 0.3
- id : 5  (sert à identifier le type de la tour dans la classe Projectile)
- particularité : tire en continu sur les ennemis avec un faisceau laser (un projectile dont la vitesse est égale à 1 et dont la capacité d’attaque est de 1 + le level de la tour d’archer/2)


/// MONSTRES /// :

Il y a 4 types de monstres pour les 2 levels actuels du jeu :

-> Monstre de base (BaseMonster) :

- vitesse : 0.01
- points de vie : 5 PV
- level up :  la vitesse augmente de 0.01 x le numéro de la vague en cours, les points de vie augmentent de 8 x le numéro de la vague en cours
- apparence :
	—> LVL1 : goblin
	—> LVL2 : pirhana

-> Boss (BossMonster) :

- vitesse : 0.06
- points de vie : 150 PV
- pas de level up
- apparence : 
	—> LVL1 : ogre
	—> LVL2 : triton

-> Monstre volant (FlyingMonster) :

- vitesse : 0.02
- points de vie : 8 PV
- level up :  la vitesse augmente de 0.01 x le numéro de la vague en cours, les points de vie augmentent de 8 x le numéro de la vague en cours
- apparence : 
	—> LVL1 : chauve-souris
	—> LVL2 : moustique

-> Monstre armé (ShootingMonster) :

- vitesse : 0.02
- points de vie : 5 PV
- temps de rechargement : 30
- capacité d’attaque = -1 PV
- périmètre d’attaque : 0.02
- level up : la vitesse augmente de 0.01 x le numéro de la vague en cours, les points de vie augmentent de 8 x le numéro de la vague en cours, le périmètre d’attaque augmente de 0.001 x le numéro de la vague en cours, sa capacité d’attaque augmente du numéro de la vague en cours.
- apparence : 
	—> LVL1 : gnome équipé d’un lance pierre
	—> LVL2 : crevette qui crache des bulles



/// GOLD /// :

On commence le jeu avec 100 gold. A chaque fois qu’un ennemi meurt, il rapporte un certain montant de gold :

-> Monstre de base : 5€
-> Boss : 50€
-> Monstre volant : 5€
-> Monstre armé : 8€

Aussi, un bonus d’or est attribué à chaque fin de vague d’ennemis (correspondant au : numéro de la vague x 3)

/// PLATEAU DE JEU /// :

Le plateau de jeu a une largeur et une longueur donné par les créateurs au lancement du jeu (dans la classe Main). Il est divisé en cellules afin d’être plus « malléable » lors de la création d’un chemin jusqu’au château. Ce chemin est comme un « empilement » de cellules adjacentes (stockées dans un ArrayList de Cellules) déterminé par le créateur dans la fonction makeChemin().
Toutes les cellules d’un niveau ont la même texture : le lvl1 possède un sol de forêt et celui du lvl2 est entièrement composé d’eau.

/// ANIMATIONS /// :

Les animations sont faites de dessins réalisés par nos soins et elles sont mises en oeuvres soit à l’aide d’un switch case soit à l’aide de fichiers .gif créés au préalable. Le tout se trouve dans le dossier « image » lui même se trouvant dans le fichier src.

/// MENU D’ACCUEIL /// :

Le menu « Titre » est composé du nom du jeu et d’un bouton « Play » géré par une fonction contains qui détermine si on a bien cliqué ou non dans le périmètre de ce bouton et si oui, la fonction run qui démarre le jeu.

/// MENUS « WIN » et « LOOSE » /// :

Lorsque le joueur perd, une page s’affiche et propose au joueur de réessayer ou de revenir à l’écran d’accueil.
Lorsque le joueur gagne, une page s’affiche et propose au joueur de passer au niveau suivant ou de revenir à l’écran d’accueil.

/// CHEATCODES /// :

Pour faire apparaître la liste des cheats dans la console, il suffit d’appuyer sur la touche « ? ».

Appuyez sur 1 : life + 10
Appuyez sur 2 : gold + 100
Appuyez sur 3 : Terminez immédiatement la vague en cours.
Appuyez sur 4 : Augmentez le level de toutes les tours du plateau au maximum.
Appuyez sur 5 : Augmentez tous les monstres présents sur la map au level 4.


/// BONUS AJOUTÉS /// :

—> Générateur de suggestions en haut à droite du plateau de jeu. Toutes les 60 secondes, il propose une action aléatoire au joueur. Le tout est géré dans la fonction drawInfos() de la classe World.
—> Jauge d’or et de vie avec animation à leur gauche. La jauge de vie se décrémente et la jauge de gold possède un montant inscrit dessus. Le tout est géré dans la fonction drawInfos() de la classe World.
—> Amélioration et réparation des tours (cf. section TOURS)
—> CheatCodes (cf. section CHEATCODES)
—> Ajout d’un boss pour chaque level (cf. section MONSTRES)
—> Ajout de FlyingMonster (monstres volants)
—> Ajout d’un level 2 : Jungle 
—> Ajout de codes de triches (cf. section CHEATCODES)
—> Ajout de types de tours différents de ceux de base (cf. FireTower, LaserTower, IceTower)
—> Ajout d’écran d’affichage « win » et « loose »
—> Ajout d’une fonction pause au jeu permettant au joueur de s’arrêter à n’importe quel moment et de reprendre là où il en était juste quand il le veut (elle garde en mémoire la valeur des différents timers et la position des monstres).

/// RÉPARTITION DU TRAVAIL /// :

Nous avons principalement travaillé via VisualStudioCode et Messenger afin de pouvoir implémenter les fonctions simultanément, pouvoir faciliter la transmission de nos avis sur chaque fonction et ainsi nous permettre à chacune d’apporter ses idées pour chaque partie du code.
Nous avons bien évidemment commencé par implémenter la partie « mécanique » dans la classe World (gestion des vagues dans le waveMaker notamment, updateMonsters(), updateTowers(), drawInfos()…) ainsi que les deux tours de base (BombeTower et ArrowTower) et le monstre de base (BaseMonster).
On a ensuite ajouté des tours de types différents et implémenté des fonctions comme findTarget() (classe World) afin de gérer l’arrivé des projectiles sur leur cible (que ce soit pour la tour d’archer, de bombe, laser ou bien les ennemis tirant sur les tours).
Puis, à la fin, on s’est occupées de la partie « Game design » en ajoutant des bonus (cités ci-dessus).
