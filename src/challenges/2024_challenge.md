# Défis

<!-- ## 🟢 Défi facile -->

### 🌐 Défi RSK 1 : Mission "Au centre" 🌐

Lors de votre match face à la redoutable équipe verte, vous avez calculé que la meilleure position pour marquer un but serait au centre du terrain.

Votre mission sera donc d'amener le robot Bleu 1 vers le centre du terrain afin qu'il puisse marquer ⚽⚽ !
#### 🎯 Cours Forest ! Cours !

Une fois connecté, votre objectif est d'amener votre robot 1 vers le centre du terrain aux coordonnées `x = 0` et `y = 0`.

Pour cela, vous utiliserez la redoutable commande Go To, qui ordonne à un robot d'aller à une position `(x, y)` avec une orientation `theta`.

```python
client.<couleur><numeros>.goto((x,y,theta), wait=False)
```

Votre code ressemblera à ceci :
```python
import rsk

with rsk.Client() as client: 
    while True:
        client.blue1.goto((0,0,0), wait=False)
```

💡 Astuce 💡 : Vous pouvez aussi récupérer votre robot grâce à la commande robots, ce qui permet d'avoir un code plus facilement maintenable :

```python
myRobot = client.robots['<couleur>'][<numeros>]
```



##### 🌈 Déchaînez votre Créativité :

N’hésitez pas à expérimenter avec différentes couleurs et intensités pour créer des effets visuels étonnants.

Bonne chance dans ce défi coloré, et que les meilleures couleurs gagnent!

### 🌐 Défi RSK 2 : Mission "Surveillance des Coordonnées" 🌐

Votre mission est de surveiller et d'afficher les coordonnées des agents sur le terrain : nos fidèles robots, codés "Bleu 1", "Bleu 2", "Vert 1" et "Vert 2".
Chaque robot a sa propre trajectoire et position dans l'espace, et il est crucial de les suivre avec précision.

##### 🎯 Surveillance de la Cible - La Balle :

En plus de suivre nos agents robots, une cible mobile - une balle - est en jeu. Votre mission inclut également de traquer et d'afficher en continu les coordonnées de cette balle.

##### 🧩 Défi Technique :

Votre code devra récupérer et afficher les positions X, Y de chaque robot et de la balle. Cela nécessite une attention méticuleuse aux données et une capacité à interpréter les informations en temps réel.

##### 👁‍🗨 Visualisation des Données :

Assurez-vous que les données soient présentées de manière claire et précise. Une bonne visualisation est la clé pour comprendre le champ de bataille numérique.

### 🌐 Défi RSK 3 : Mission "Navigation Stratégique" 🌐

Après avoir maîtrisé l'art de l'illumination et de la surveillance, il est temps de passer à la navigation et à la stratégie.
Dans ce défi, vous allez diriger un robot dans une danse délicate de positionnement et de mouvement.

##### 🌐 Votre Mission :

Au lieu de tourner autour d'une cible, votre tâche est de guider le robot vers des points cardinaux spécifiques autour de la balle. Pensez à cela comme un jeu de positionnement stratégique : Nord, Sud, Est, Ouest.

##### 🤖 Manœuvres du Robot :

Vous contrôlerez le robot "Bleu 1" pour le déplacer vers des points prédéterminés autour de la balle, en utilisant des coordonnées relatives. Votre agilité en programmation et votre sens de la précision seront essentiels ici.

##### 📍 Instructions de Navigation :

1. Déplacez le robot de 0.25 mètres à l'ouest de la balle.
2. Ensuite, dirigez-le 0.25 mètres au nord de la balle.
3. Poursuivez en le déplaçant de 0.25 mètres à l'est.
4. Enfin, amenez-le 0.25 mètres au sud de la position initiale.

### 🌐 Défi RSK 4 : Mission "Rotation Maîtrisée" 🌐

Votre quatrième mission dans l'arène numérique est une danse de précision et d'agilité. Dans ce nouveau défi, vous allez orchestrer une rotation élégante de votre robot, en mettant à l'épreuve votre maîtrise des commandes de mouvement.

##### 🔄 Votre Mission :

Vous devez faire exécuter à votre robot une rotation complète sur lui-même. Cette manœuvre requiert un contrôle minutieux et une compréhension approfondie des commandes de votre robot.

##### 🚨 Attention - Changement de Commande :

Pour ce défi, oubliez la commande goto habituelle. Vous allez plutôt utiliser la commande control pour diriger le robot. Cette approche vous donne un contrôle plus direct et précis sur les mouvements du robot, essentiel pour réussir une rotation parfaite.

### 🌐 Défi RSK 5 : Mission "Coup de Maître" 🌐

Votre cinquième mission dans cette aventure technologique consiste à manœuvrer votre robot de manière à frapper une balle placée au centre.
Ce défi mettra à l'épreuve votre habileté à évaluer les distances et à contrôler le mouvement de votre robot.

##### ⚽ Votre Mission :

Le but est de positionner et de faire avancer le robot pour qu'il frappe la balle située au centre.
Cela nécessitera une compréhension fine de la dynamique et de la force nécessaire pour un impact efficace.

##### 📐 Position de Départ :

Le robot commence sa mission depuis une position sur l'axe des x positifs (à une distance x quelconque du centre).
Votre tâche est de le guider depuis cette position initiale jusqu'à la balle.

### 🌐 Défi RSK 6 : Mission "Passe Parfaite" 🌐

Votre sixième mission consiste à exécuter une passe précise entre deux robots. Ce défi nécessite une compréhension approfondie de la dynamique des mouvements et une synchronisation impeccable entre les deux robots.

##### ⚽ Votre Mission :

Un robot doit envoyer la balle à un autre robot situé à une certaine distance. La clé est d'ajuster la force et l'angle de la passe pour assurer une réception réussie par le robot destinataire.

### 🌐 Défi RSK 7 : Mission "Orbite Circulaire" 🌐

Votre septième défi est de faire naviguer un robot autour d'une balle, en suivant la trajectoire d'un cercle parfait. Ce défi sollicitera vos compétences en géométrie et en programmation pour réaliser une orbite circulaire précise.

##### 🔵 Votre Mission :

Faire tourner le robot autour de la balle en maintenant une distance constante, comme s'il suivait l'orbite d'un satellite.
La trajectoire doit ressembler à un cercle parfait autour de la balle.

### 🏆 Défi RSK Final : Mission "Match Ultime" 🏆

Votre mission finale est de mettre en œuvre tout ce que vous avez appris pour orchestrer un match de robot. Ce défi combine stratégie, précision, coordination d'équipe, et adaptation en temps réel. Vous devrez faire preuve de créativité, de logique de programmation avancée et de compréhension tactique du jeu.

##### ⚽ Votre Mission :

Organiser un match impliquant deux équipes de robots. Chaque équipe doit essayer de marquer des buts tout en défendant son propre but.

##### 🤖 Stratégie et Exécution :

- Programmez les robots pour qu'ils puissent se déplacer sur le terrain, contrôler la balle, passer à leurs coéquipiers, et tirer au but.
- Implémentez des stratégies défensives pour que les robots puissent bloquer les tentatives de but de l'équipe adverse.
- Assurez une bonne communication et coordination entre les robots de la même équipe.

<!-- ## Défi normale -->

<!-- ## Défi difficile -->
