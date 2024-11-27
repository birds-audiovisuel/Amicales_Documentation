# Défis

### 🌐 Défi RSK 1 : Mission "Au centre" ⭐★★★★ 🌐

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

#### 💡 Astuce 💡 :
 Vous pouvez aussi récupérer votre robot grâce à la commande robots, ce qui permet d'avoir un code plus facilement maintenable :

```python
myRobot = client.robots['<couleur>'][<numeros>]
```


### 🌐 Défi RSK 2 : Mission "À l'œil" ⭐⭐★★★ 🌐

Votre match contre l'équipe verte est difficile, et il est nécessaire de vérifier les positions de vos ennemis pour adapter votre stratégie ! Votre mission : capturer un maximum d'informations afin de vaincre la redoutable équipe verte.

##### 🎯 Surveillance Maximal :

Lors de cette mission, vous devrez récupérer toutes les informations dynamiques sur le terrain, ce qui inclut les coordonnées des 4 robots ainsi que celles de la balle, et les afficher.

##### 🧩 Défi Technique :

Votre code devra récupérer et afficher les positions `X`, `Y` de chaque robot et de la balle. Cela nécessitera une attention méticuleuse aux données et une capacité à interpréter les informations en temps réel. Il est conseillé de consulter la documentation de RSK pour compléter ce défi  ([Cliquez ici)](https://robot-soccer-kit.github.io/programming#localization-informations))

##### 👁‍🗨 Visualisation des Données :

Assurez-vous que les données soient présentées de manière claire et précise. Une bonne visualisation est essentielle pour comprendre le champ de bataille numérique.

Si vous êtes bloqué, voici un petit indice : [indice](https://www.docstring.fr/glossaire/print/)

### 🌐 Défi RSK 3 : Mission "Mimétisme"⭐⭐★★★  🌐

Lors de votre affrontement avec l'équipe verte, celle-ci utilise une technique mystérieuse qui désoriente vos robots ! Mais vous avez la solution : toujours regarder dans la même direction que votre ennemi !

##### 🌐 Votre Mission :

Réutilisez et adaptez ce que vous avez réalisé lors de vos deux précédentes missions afin de
Récupérer l'orientation du robot Vert 1 puis
donner à votre robot Bleu 1 la même orientation.

#### 🎯 Mime Mime Mime !

1 - Récupérez l'orientation `theta` du robot Vert 1 à l’aide des informations disponibles sur le terrain.
2 - Donnez l’ordre à votre robot Bleu 1 d’adopter la même orientation.

### 🌐 Défi RSK 4 : Mission "Adaptation Défensive !" ⭐⭐⭐★★ 🌐

L'attaquant de l'équipe verte ne cesse de marquer des buts. Pour l'arrêter, vous avez imaginé une méthode simple : placer votre deuxième robot en gardien de but.

##### 🔄 Votre Mission :

Vous devrez utiliser la position en `y` de la balle pour contrer les tirs de l'équipe verte.
Utilisez également les constantes fournies par la bibliothèque RSK afin de positionner votre gardien avec une précision optimale.

Voici un exemple pour récupérer les constantes :
```python
import rsk
from rsk import constants

position_but = constants.defense_area_width # Correspond à la position en x des cages du côté positif du terrain
```

##### 🧠 Curiosité 500% :

N'hésitez pas à explorer la bibliothèque RSK pour découvrir tout ce qu'elle contient !
Pourquoi ne pas commencer par examiner les différentes constantes disponibles ?
- Astuce 1 : Tapez `constants.` et observez les propositions qui vous sont faites.
- Astuce 2 : Pour une exploration plus poussée, appuyez sur `CTRL + clic` sur le mot `constants`. Vous accéderez directement aux fichiers de la bibliothèque 🤯.

Attention : Ne modifiez rien dans ces fichiers 🤭.

#### 👀 TOUJOURS PLUS ! (Sous-défi facultatif - ⭐⭐⭐⭐⭐)  :

Pour un défi supplémentaire, essayez de programmer votre défenseur pour qu'il se base sur l'orientation du robot Vert 1 plutôt que sur la position de la balle.
Ce défi est optionnel, mais il nécessitera des notions avancées en trigonométrie.

### 🌐 Défi RSK 5 : Mission "Side Swap" ⭐⭐⭐★★ 🌐

La mi-temps du match contre l'équipe verte approche. Comme vous le savez, les côtés du terrain sont échangés entre les mi-temps, mais vous n’avez pas encore pris cela en compte dans votre code.

Vous devez rapidement mettre en place une solution permettant de modifier facilement ce paramètre pour adapter votre stratégie !

##### ⚽ Votre Mission :

Votre mission sera de distinguer le côté **positif** et **négatif** du terrain afin de pouvoir vous adapter à toutes les circonstances et éviter d'attaquer dans votre propre camp !

Pour cela, vous pouvez utiliser la fonction `input` de Python, qui permet de saisir des valeurs à la main pendant l’exécution de votre programme.


Voici comment utiliser `input` :
```python
réponse = input('Que voulez vous faire ?')
```

Voici le résultat dans votre terminal
```bash
Que voulez vous faire ?
>| 
```
Ici, le programme attend une réponse de l’utilisateur, qui sera ensuite stockée dans la variable `réponse`.

#### ⚠️ ATTENTION ⚠️ :
La réponse fournie par l’utilisateur est sous forme de chaîne de caractères. Ainsi, si vous entrez un nombre, le programme le considérera comme une chaîne :
``` python
réponse = '1'
```
Pour résoudre ce problème, vous pouvez convertir la chaîne en nombre à l’aide des fonctions `int` ou `float` :

``` python
réponseEntiere = int('1')
réponseFlottante = float('3.14') 
```

#### 💡 Indice

Si vous ne savez pas par où commencer, essayez de voir comment positionner votre robot défensif du défi précédent dans les buts opposés.

Il se pourrait que vous ayez besoin de multiplier certaines valeurs par **-1** 😉.


### 🌐 Défi RSK 6 : Mission " Des placements " ⭐⭐⭐⭐★ 🌐

Maintenant qu'une muraille protège votre camp, il est temps de passer à l’attaque contre l’équipe verte !

Votre robot 1 est prêt à en découdre et à marquer des BUTS ⚽⚽⚽ !


##### ⚽ Votre Mission :

Votre objectif sera de positionner votre robot derrière la balle, à une distance optimale pour tirer sans la pousser immédiatement puis de tirer. Pour cela, vous devrez prendre en compte trois paramètres :

- Le rayon du robot.
- Le rayon de la balle.
- Une marge d’imprécision arbitraire sur la distance entre le robot et la balle. Vous devrez effectuer plusieurs essais jusqu’à ce que le robot reste bien positionné derrière la balle sans bouger inutilement.

⚠️ Points importants :

- Si vous vous placez trop loin, vous risquez de perdre en puissance de frappe.
- Effectuez un maximum de tests pour trouver la distance optimale !

Pour simplifier cet objectif, placez la balle au centre du terrain et positionnez votre robot à mi-distance entre vos cages et la balle. Cela vous permettra de travailler dans des conditions simples et prévisibles.

Maintenant que vous etes bien positionné, 💥💥 TRIEZ 💥💥 !

### 🌐 Défi RSK 7 : Mission " Panne d'énergie ! " ⭐⭐⭐⭐⭐ 🌐

Suite à votre précédente mission, vous avez sûrement remarqué que la balle ne va pas très loin lorsque vous utilisez la commande `kick` du robot.


##### ⚽ Votre Mission :

Utilisez un timer pour éviter le déchargement trop régulier du condensateur. En effet, le kickeur met un certain temps à se charger à 100 %, et il est important de s’assurer qu’il soit complètement chargé avant de tirer. Sinon, vous risquez de simplement donner la balle à vos ennemis !

Utilisez donc un timer pour vous assurer que le kickeur soit prêt avant chaque tir, afin d’optimiser la puissance et la précision de vos frappes.

#### 💡 Indice 
Allez consulter la documentation de [time](https://www.programiz.com/python-programming/time) !


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

