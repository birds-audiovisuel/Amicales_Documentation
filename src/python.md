# Python

## Introduction

Python est un langage de programmation de haut niveau créé par Guido van Rossum en 1991.
Son nom s'inspire de la série télévisée "Monty Python's Flying Circus".
Il est géré par la Python Software Foundation, une organisation qui soutient son développement et sa communauté.

## Installation

Pour installer Python, visitez [le site officiel de Python](https://www.python.org/downloads/) et téléchargez la dernière version, Python 3.12.

## Premiers Pas

### Hello World

```python
print("Hello, World!")
```

## Caractéristiques Principales

- Langage de haut niveau : Python est conçu pour être facile à lire et à écrire.
- Gratuit : Python est open source et gratuit.
- Orienté objet : Python supporte la programmation orientée objet.
- Polyvalent : Utilisé dans de nombreux domaines comme l'analyse de données, la bioinformatique, et la robotique

# Exemples de Code
<!-- Cette partie du cour vient du site de Clement Gaspard : https://cgaspard3333.github.io/intro-python/index.html Clément GASPARD - clement.gaspard@u-bordeaux.fr -->

## Variables

Python possède plusieurs types de données courants :

### Nombres entiers (`int`)

```python
a = 5
print(type(a))
# >> int
```

### Nombres décimaux (`float`)

En informatique, les nombres décimaux sont souvent représentés en nombre à virgule flottante, encore appelés nombres flottants.

```python
b = 3.14
print(type(b))
# >> float
```

Compte tenu de la manière dont les nombres à virgule flottante sont stockés en mémoire, ils sont souvent approximés, ce qui peut entraîner des erreurs de calcul. Il faut donc éviter de tester l'égalité de deux nombres flottants.

### Chaînes de caractères (`str`)

```python
c = "Salut"
print(type(c))
# >> str
```

### Booléens (`bool`)

```python
d = True
print(type(d))
# >> bool
```

En Python, il n'est pas nécessaire de déclarer le type d'une variable, le langage se charge de le déterminer automatiquement.

## Conditions et boucles

### Les conditions (Structures de décision)

Les structures conditionnelles permettent de prendre des décisions dans un programme. En fonction de certaines conditions, différentes parties du code peuvent être exécutées.

- **`if`** : vérifie une condition et exécute le bloc de code associé si elle est vraie.
- **`elif`** : vérifie une autre condition lorsque la première est fausse et exécute le bloc de code associé si cette nouvelle condition est vraie.
- **`else`** : exécute un bloc de code si toutes les conditions précédentes sont fausses.

### Exemple :

```python
if condition:
    # Bloc de code exécuté si la condition est vraie
elif autre_condition:
    # Bloc exécuté si la première condition est fausse et l’autre condition est vraie
else:
    # Bloc exécuté si toutes les conditions précédentes sont fausses
```


### Les boucles (Structures itératives)

#### 1. La boucle `for`

La boucle `for` permet de répéter un bloc de code un nombre déterminé de fois. Elle est souvent utilisée pour parcourir des séquences (listes, chaînes de caractères, etc.).

#### Exemple :

```python
for variable in séquence:
    # Bloc de code exécuté pour chaque élément de la séquence

for i in range(3):
    print(i)
```

```plaintext
>> 0
>> 1
>> 2
```

#### 2. La boucle `while`

La boucle `while` exécute un bloc de code tant qu’une condition est vraie.

#### Exemple :

```python
while condition:
    # Bloc de code exécuté tant que la condition est vraie

compteur = 0
while compteur < 4:
    print(compteur)
    compteur += 1
```

```plaintext
>> 0
>> 1
>> 2
>> 3
```

#### 3. Boucle infinie et sortie de boucle

Une boucle infinie se produit quand la condition de sortie n’est jamais atteinte. Cela peut bloquer l’exécution du programme. On peut interrompre une boucle avec l’instruction `break`.

#### Exemple :

```python
compteur = 0
while True:
    print(compteur)
    compteur += 1
    if compteur == 4:
        break
```

```plaintext
>> 0
>> 1
>> 2
>> 3
```

## Fonctions

```python
def saluer(nom):
    return f"Bonjour, {nom}!"

print(saluer("Alice"))
```

## Ressources supplémentaires

- [Documentation Officielle](https://docs.python.org/3/)
- [Tutoriels Python pour Débutants](https://www.learnpython.org/)
- [Introduction au Python + Exercices ](https://cgaspard3333.github.io/intro-python/index.html)
