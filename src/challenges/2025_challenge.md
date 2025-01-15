# Défis 

### 🌐 Défi RSK 1 : "Mission Prêt ! Partez !"  ⭐★★★★ 🌐

Afin d'avoir une vue d'ensemble sur le match et d'être dans une position optimale pour recevoir la balle de n'importe où, vous avez décidé d'accompagner votre robot bleu n°1 jusqu'au centre du terrain.

#### 🎯 Réception à toute épreuve !

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

#### 💡 Astuce 💡 :
 Vous pouvez aussi récupérer votre robot grâce à la commande robots, ce qui permet d'avoir un code plus facilement maintenable :

```python
myRobot = client.robots['<couleur>'][<numeros>]
```

### 🌐 Défi RSK 2 : "Dos à dos" ⭐⭐★★★ 🌐

Afin de couvrir une zone encore plus grande, vous avez décidé d'utiliser vos deux robots comme tours de garde.

#### 🎯 I've got you in my sights
Votre mission sera de faire collaborer vos deux robots afin qu'ils couvrent la zone la plus large possible.

Tandis que l'un couvre la première partie du terrain avec `x>0`, l'autre se charge de la zone avec `x<0`.

Pour cela, vous pouvez réutiliser le programme précédemment écrit afin de positionner le robot bleu 1 en `(1,0)` et le robot bleu 2 en `(−1,0)`.
Veillez également à ce que les deux robots regardent dans des directions opposées.

#### 💡 Indice 💡 :
Vous pouvez donner des instructions à deux robots en même temps dans le même programme !

Si vous n’arrivez pas à faire en sorte que les deux robots regardent dans des directions opposées, pensez que l’orientation des robots est exprimée en radians !

### 🌐 Défi RSK 3 : "Mission Scan" ⭐⭐★★★ 🌐

Maintenant que vos robots sont prêts à s'adapter à toutes les situations, il reste à identifier ces situations ! Pour cela, vous devez connaître votre environnement.

##### 🎯 Surveillance Maximal :

Lors de cette mission, vous devrez récupérer toutes les informations dynamiques sur le terrain, ce qui inclut les coordonnées des 4 robots ainsi que celles de la balle, et les afficher.

##### 🧩 Défi Technique :

Votre code devra récupérer et afficher les positions `X`, `Y` de chaque robot et de la balle. Cela nécessitera une attention méticuleuse aux données et une capacité à interpréter les informations en temps réel. Il est conseillé de consulter la documentation de RSK pour compléter ce défi  ([Cliquez ici)](https://robot-soccer-kit.github.io/programming#localization-informations))

##### 👁‍🗨 Visualisation des Données :

Assurez-vous que les données soient présentées de manière claire et précise. Une bonne visualisation est essentielle pour comprendre le champ de bataille numérique.

Si vous êtes bloqué, voici un petit indice : [indice](https://www.docstring.fr/glossaire/print/)

### 🌐 Défi RSK 4 : Mission "Défense offensive !"⭐⭐★★★  🌐

Vous avez reperer que votre enemie vert s'appretais a tirer dans vos cage ! Votre meilleur façon d'empecher se tire est de foncer le plus vite possible vers la balle !

##### 🔄 Votre Mission :

Réutilisez et adaptez ce que vous avez réalisé lors de vos deux précédentes missions afin de
Récupérer la position de la balle
donner à votre robot Bleu 1 la même position

#### 🎯 Arrete la !

1 - Récupérez la position `(x,y)` de la balle à l’aide des informations disponibles sur le terrain.
2 - Donnez l’ordre à votre robot Bleu 1 d'aller vers cette position

### 🌐 Défi RSK 5 : Mission "Retour à la réalité"⭐⭐⭐★★  🌐

Pour l'instant vous vous etes concentré a réaliser vos testes dans le simulateur, ne serais t-il pas tant de tester en réalité ! 

##### 🔄 Votre Mission :
Votre mission consistera en l'utilisation du game controlleur en l'apprentissage de la connexion avec celui-ci afin de faire bouger les robot en vrai !
Votre seconde mission sera de voir ce qu'il se passe lorsque l'un des robot n'est pas sur le terrain 

💥 😱 COMMENT ÇA, VOTRE PROGRAMME CRASH ?!

cela veux dire que vous n'avez pas gerer les erreurs !
le fait que l'un des robot ou meme la balle sorte du terrain vous enleve une donnée a votre programme ! 
pour le corriger il suffi de faire un test si il manque une valeur votre programme fera quelque chose d'autre en conséquences

```python
try:
    #Votre code

except rsk.client.ClientError as e:
    print(e)
    #autre chose 
```

#### 💡 Astuce 💡 :

Vous pouvez aussi gerer chacune des erreur afin de pouvoir continuer a bouger malgré la perte d'information par exemple vous pouvez definir d'une autre maniere les données perdu !


### 🌐 Défi RSK 6 : Mission "Carton jaune" ⭐⭐⭐⭐★ 🌐

Maintenant que votre robot suit la balle vous vous rendez compte durant votre match qu'il ne peux pas rester a coté d'elle durant trop de temps sous penne de se prendre une pénalité ! mais on peux faire de cette penalité aussi un avantage !

##### 🔄 Votre Mission :

Votre mission sera de detecter lorsque un robot est pénaliser, de cette maniere vous pourrez lorsque les deux robot attaquant sont pénaliser faire monter votre defenseur pour qu'il attaque ! 
Pour cela vous avez acces aux information du `referee` [referee](https://robot-soccer-kit.github.io/referee#access-to-referee-information-) 

#### 🎯 A l'ataque !

1 - Récupérez les information de l'arbitre 
2 - Vérifiez que les deux robot vert 1 et bleu 1 sont penalisés 
3 - Faites monter votre defenseur en attaquant 

Voici un exemple d'utilisation du `referee` :
```python
import rsk

with rsk.Client() as client: 
    while True:
        client.referee["game_is_running"] #Cette ligne renvoie True si la partie est débuté False sinon
```

### 🏆 Défi RSK Final : Mission "Match Ultime" ⭐⭐⭐⭐⭐ 🏆

Combinez tout ce que vous avez appris, et plus encore, pour créer un programme imparable. Que toutes les équipes vertes tremblent rien qu'en entendant votre nom ! 😈

C’est l’occasion de mettre en pratique toutes vos compétences et de créer une stratégie gagnante. Allez, faites briller votre robot et montrez à l’équipe verte qui est le vrai champion ! 💪⚽

##### ⚽ Votre Mission :

Organiser un match impliquant deux équipes de robots. Chaque équipe doit essayer de marquer des buts tout en défendant son propre but.

##### 🤖 Stratégie et Exécution :

- Programmez les robots pour qu'ils puissent se déplacer sur le terrain, contrôler la balle, et tirer au but.
- Implémentez des stratégies défensives pour que les robots puissent bloquer les tentatives de but de l'équipe adverse.
- Assurez une bonne communication et coordination entre les robots de la même équipe.

### 🌐 Les Défi RSK Continuent ⭐⭐⭐⭐⭐⭐⭐⭐⭐⭐ ! 🌐
Maintenant que votre match est passé, corrigez ce qui ne fonctionne pas, améliorez ce qui marche bien et inventez de nouvelles stratégies de jeu pour surprendre vos adversaires !

C’est le moment de peaufiner votre programme et d’explorer de nouvelles idées pour être encore plus performant. Gardez à l'esprit que l'innovation et l'adaptabilité sont les clés du succès ! 🚀

