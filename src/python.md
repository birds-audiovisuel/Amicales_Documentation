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

## Exemples de Code

### Variables

Python possède plusieurs types de données courants :

## Nombres entiers (`int`)

```python
a = 5
print(type(a))
# >> int
```

## Nombres décimaux (`float`)

En informatique, les nombres décimaux sont souvent représentés en nombre à virgule flottante, encore appelés nombres flottants.

```python
b = 3.14
print(type(b))
# >> float
```

Compte tenu de la manière dont les nombres à virgule flottante sont stockés en mémoire, ils sont souvent approximés, ce qui peut entraîner des erreurs de calcul. Il faut donc éviter de tester l'égalité de deux nombres flottants.

## Chaînes de caractères (`str`)

```python
c = "Salut"
print(type(c))
# >> str
```

## Booléens (`bool`)

```python
d = True
print(type(d))
# >> bool
```

En Python, il n'est pas nécessaire de déclarer le type d'une variable, le langage se charge de le déterminer automatiquement.


### Boucle `for`

```python
for i in range(5):
    print(i)
```

### Fonctions

```python
def saluer(nom):
    return f"Bonjour, {nom}!"

print(saluer("Alice"))
```

## Ressources supplémentaires

- [Documentation Officielle](https://docs.python.org/3/)
- [Tutoriels Python pour Débutants](https://www.learnpython.org/)
