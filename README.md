---
title: "Intro à la programmation en Python"
author: "Miguel PALENCIA-OLIVAR"
date: '2022-02-14'
output: 
  html_document:
    keep_md: true
    df_print: paged
---

# Préambule

Ce document a pour but de donner les bases, les essentiels à tout non-spécialiste intéressé par l'informatique. Si maîtrisés, ces fondamentaux devraient permettre. Vous ne sortirez pas informaticiens de cette cure; en revanche, vous saurez vous débrouiller et aller chercher ce qu'il manque par vous-même. Soyez fair-play : ne trichez que si vous n'y arrivez vraiment pas. Le secret de la réussite en programmation réside dans la réflexion, la compréhension/décomposition en opérations de base de ce que l'on veut faire, et bien sûr dans la pratique; en d'autres termes, il faudra coder jusqu'à ce que "ça rentre". Je recommande d'ailleurs de coder en même temps que vous consultez les documents-supports. Les exercices proposés sont tous corrigés et commentés, ils se veulent un peu complets pour que toutes les notions soient vues. [Un petit projet sympathique](https://github.com/mpalenciaolivar/Simple-Game-Of-Life) en rapport avec des automates cellulaires et AVEC corrigé clôt ce petit programme de mise à niveau. Ce projet est vraiment simple, ne requiert que peu de temps pour être pris en main, et est essentiel pour "voir comment on fait en vrai" et pour voir comment on modularise son code correctement. Il fait appel à toutes les notions qui auront été vues ici. En bref, de quoi convaincre les plus réfractaires d'entre vous que, loin des poncifs de l'Informatique froide et sans saveur, on est ici aux portes d'un monde haut en couleurs et dont les possibilités sont quasi-infinies, en particulier pour les bidouilleurs.

J'ai fait le choix de Python pour plusieurs raisons :

\- parce que c'est simple à aborder;

\- parce qu'il existe plein de ressources à explorer, pour tous les goûts, dans toutes les langues;

\- parce que c'est multiplateforme et que l'on peut l'interfacer avec un certain nombre de logiciels.

# Ce qu'il faut installer

**Lisez tout avant d'installer**

Un IDE ou un éditeur de texte au choix. Je recommande [Visual Studio Code (VSCode)](https://www.rstudio.com/) pour les débutants. Mais avant, il faudra Python 3. Pour cela, on va installer la distribution [Anaconda](https://www.anaconda.com/products/individual), qui permet également d'installer un IDE ou un éditeur de texte via son interface graphique.

# Le cours

À consulter - éventuellement à visionner, *cf* liens Youtube - et à mettre en pratique dans cet ordre-ci :

+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| Lien vers le cours                                                                                                                                                                                                                                                                      | Vidéo                                         |
+=========================================================================================================================================================================================================================================================================================+===============================================+
| [Introduction à la programmation Python. Les bases du langage Python. Types de données, affectation, calculs, structures algorithmiques (branchements conditionnels, boucles)](https://eric.univ-lyon2.fr/~ricco/cours/slides/PA%20-%20intro%20python%20-%20bases%20algorithmiques.pdf) | <https://www.youtube.com/watch?v=EffofzHutZA> |
+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| [Programmation modulaire sous Python. Procédures et fonctions, découpage des projets en modules.](https://eric.univ-lyon2.fr/~ricco/cours/slides/PB%20-%20programmation%20modulaire%20avec%20python.pdf)                                                                                | <https://www.youtube.com/watch?v=r3wxi4cYVn4> |
+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+
| [Collection d'objets sous Python. Création des tuples, listes et dictionnaires. Indices et plages d'indices. Digressions sur les chaînes de caractères.](https://eric.univ-lyon2.fr/~ricco/cours/slides/PC%20-%20collections%20sous%20python.pdf)                                       | <https://www.youtube.com/watch?v=10Y2kJ-O9p8> |
+-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------+-----------------------------------------------+

# Les exercices maison

Attention aux terminologies : une fonction et une procédure se ressemblent beaucoup, mais divergent sur un point ;-)

## Exercice 0

Écrire une fonction dans un module Python qui, à tout chiffre/nombre compris entre 1 et 10, lui appliquera un exposant que l'on spécifiera. Par exemple, si l'on souhaite 10 exposant 3, nous obtenons 1000.

## Exercice 1

Écrire une procédure dont l'exécution ne cessera que lorsque l'utilisateur entrera la chaîne de caractères (string) suivante : `"stop"` .

Astuce : la fonction à utiliser pour saisir une donnée est `input()` .

## Exercice 2

Écrire une fonction qui, à chaque chaîne de caractères, retirera les lettres dans une liste fournie en entrée (les voyelles, par ex.).

Indice : il nous faudra stocker toutes les lettres d'une part, et toutes lettres que l'on souhaitera retenir d'autre part, puis retourner la liste des lettres que l'on retiendra.

Exemple : "voyelles" doit devenir "vlls" si l'on décide d'en retirer les voyelles, avec y inclus.

## Exercice 3

Écrire une fonction qui retourne tous les multiples d'un nombre compris entre dans un intervalle fourni en entrée.

Indices : il faudra spécifier un intervalle, recueillir les multiples dans une structure, et tester si un nombre est un multiple d'un autre. Pour cette dernière opération, on utilisera le modulo, qui est le reste d'une division euclidienne. Ainsi, `5 % 2` vaut `1`, tandis que `4 % 2` vaut `0`. Vous l'aurez compris : le modulo d'un nombre par un autre facteur dont il est le multiple vaut 0.

## Exercice 4

Jouons à un jeu de plus ou moins. Écrire une procédure dans laquelle un chiffre est sélectionné au hasard entre 0 et 9. L'utilisateur doit deviner lequel c'est. S'il saisit un chiffre supérieur à celui sélectionné, alors la fonction doit afficher que c'est moins, et vice versa. Le jeu s'arrête lorsque l'utilisateur aura deviné le bon chiffre.

Astuce : pour sélectionner un chiffre entre 0 et 9, on devra importer un package et utiliser une fonction de ce dernier, tel que ci-dessous :


```python
import random


random.randint(0, 9) # Ceci doit faire partie du corps de la procédure à développer.
```

```
## 6
```

## Exercice 5

Créer une fonction qui remplace tous les termes dans la diagonale d'un tableau carré par la chaîne `"diag"`. Voici un exemple de tableau et la sortie attendue pour celui-ci :

*Entrée :*

|     |     |     |
|-----|-----|-----|
| 1   | 2   | 3   |
| 4   | 5   | 6   |
| 7   | 8   | 9   |

*Sortie :*

|      |      |      |
|------|------|------|
| diag | 2    | 3    |
| 4    | diag | 6    |
| 7    | 8    | diag |

Sortie version Python :

``` python
[["diag", 2, 3], [4, "diag", 6], [7, 8, "diag"]]
```

Astuces :

-   en Python, un tableau est une liste qui contient des listes, ou une liste de listes. On peut y mettre tous les éléments que l'on souhaite, et même les panacher, et on peut avoir des lignes avec un nombre d'éléments variable . Nous nous en tiendrons à un tableau carré de 9 éléments que l'on remplira d'éléments quelconques.

-   soit L une liste, la longueur d'une liste s'obtient ainsi : `len(L)`

## Exercice 6

La fonction factorielle est certainement la [fonction récursive](https://www.jesuisundev.com/comprendre-la-recursivite-en-7-min/) la plus simple à comprendre. Une fonction récursive signifie que l'on peut appeler la fonction que l'on définit dans le corps de son expression, en décomposant la donnée à traiter en blocs plus petits. Concrètement, si l'on devait définir la factorielle récursivement, on ferait ainsi :

``` python
factorielle(n) = n * factorielle(n-1)
```

On demande ici de coder la fonction factorielle.

Indice : il faudra forcément une condition d'arrêt.

## Exercice 7

Voici un problème populaire : le fizzbuzz. Je vous propose d'en faire une version basique (il y a des concours d'implémentations sur internet !). Les données du problème sont les suivantes :

Pour les nombres compris dans un intervalle :

-   si le nombre est divisible par 3 : on affiche `Fizz` ;

-   si le nombre est divisible par 5 : on affiche `Buzz` ;

-   si le nombre est divisible par 3 et par 5 : on affiche `Fizzbuzz` ;

-   sinon on affiche le nombre.

Codez une procédure qui prend un intervalle en entrée (mettons de 1 à 20, intervalle fermé) et qui résout ce problème.

# Les solutions

Sous chaque portion de code se trouve le résultat de l'exécution.

## Exercice 0


```python
# On définit notre fonction
def puissance(nombre, exposant):
  return nombre ** exposant


# Spécifions, par exemple, un exposant 2
exposant = 2

# l'argument `end` permet d'éviter le retour à la ligne
for i in range(1, 11):
  print(puissance(i, exposant), end=" ")
```

```
## 1 4 9 16 25 36 49 64 81 100
```

## Exercice 1


```python
def saisie_infinie():
  # La fonction while est toujours vraie, donc s'exécute perpétuellement
  while True:
    saisie = input("Saisir quelque chose. Saisir \"stop\" pour sortir de la fonction.")
    if saisie != "stop":
      print("Saisie vaut: " + str(saisie))
    else:
      # Si la saisie est stop, on "casse" la boucle
      break


# Décommenter les 2 lignes ci-dessous pour exécuter le code. Il a été commenté pour pouvoir générer le document.
# saisie_infinie()
# print("Fin de la boucle.")
```

## Exercice 2


```python
def mot_filtre(mot, liste_de_lettres):
  filtrage = ""
  for lettre in mot:
    if lettre not in liste_de_lettres:
      filtrage += lettre
  return filtrage


mot = "voyelles"
liste_de_lettres = ["a", "e", "i", "o", "u", "y"]
print(mot_filtre(mot, liste_de_lettres))
```

```
## vlls
```

## Exercice 3


```python
def multiple(intervalle, facteur):
  multiples = []
  for i in intervalle:
    if i % facteur == 0:
      multiples.append(i)
  return multiples


# Mettons que nous voulions les multiples de 2 compris entre 3 et 20 inclus:
# (attention: range s'arrête à 19 si on met 20 comme borne supérieure, d'où le 21)
print(multiple(range(3, 21), 2))
```

```
## [4, 6, 8, 10, 12, 14, 16, 18, 20]
```

## Exercice 4


```python
import random


def plus_ou_moins():
  pari = -1
  a_deviner = random.randint(0, 9)
  # On pourrait aussi faire un while True et faire un break plus loin, comme ci-dessus.
  while pari != a_deviner:
    pari = int(input("Saisir un entier entre 0 et 9."))
    if pari > a_deviner:
      print("C'est moins.")
    if pari < a_deviner:
      print("C'est plus.")
  print("Bravo !")

# Décommenter la ligne ci-dessous pour l'exécution
# Pour une obscure raison, les "C'est plus" et "C'est moins" apparaissent en fin d'exécution dans RStudio, càd, lorsque le jeu se termine. Pour autant, le code est bien correct.
# plus_ou_moins()
```

## Exercice 5


```python
def remplace_diagonale(tableau):
  for i in range(len(tableau)):
    for j in range(len(tableau[i])):
      if i == j: # Si l'on est sur la diagonale, on remplace
        tableau[i][j] = "diag"
  return tableau

      
T = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(remplace_diagonale(T))
```

```
## [['diag', 2, 3], [4, 'diag', 6], [7, 8, 'diag']]
```

## Exercice 6

Les factorielles de 0 ou de 1 valent 1, c'est notre condition d'arrêt. On calcule à chaque fois pour des valeurs plus petites jusqu'à atteindre 1 ou 0, en fonction de la valeur saisie en entrée. Notez que la récursivité intervient en dernière ligne ; on parle de *tail-recursion* (par opposition à la *head-recursion*).


```python
def factorielle(n):
  # Condition d'arrêt
  if n == 0 or n == 1:
    return 1
  else:
    return n * factorielle(n-1)
  
  
for n in range(0, 11):
  print(factorielle(n), end=" ")
```

```
## 1 1 2 6 24 120 720 5040 40320 362880 3628800
```

## Exercice 7

Notez l'ordre des conditions, et le mot-clé `continue`, qui fait passer le `for` à l'itération suivante.


```python
def fizzbuzz(intervalle):
  for i in intervalle:
      if i % 3 == 0 and i % 5 == 0:
          print("Fizzbuzz", end=" ")
          continue
      elif i % 3 == 0:
          print("Fizz", end=" ")
          continue
      elif i % 5 == 0:
          print("Buzz", end=" ")
          continue
      print(i, end=" ")
      
      
intervalle = range(1, 21)
fizzbuzz(intervalle)
```

```
## 1 2 Fizz 4 Buzz Fizz 7 8 Fizz Buzz 11 Fizz 13 14 Fizzbuzz 16 17 Fizz 19 Buzz
```

# Davantage d'exercices corrigés

[En voilà d'autres](https://python.developpez.com/cours/apprendre-python-3/?page=exercices-corriges#L14-1). Je dirais qu'ils sont un peu plus complexes que les miens, mais non moins utiles. On a dit qu'il fallait pratiquer, vous voilà servis.
