# MiniTrice

------------------------------------------------------------------------

# Installation

## 1) Prérequis

Le projet fonctionne avec **Python 3**.

Vérifier que Python est installé :

``` bash
python3 --version
```

Si Python n'est pas installé :

### Linux (Debian / Ubuntu)

``` bash
sudo apt update
sudo apt install python3
```

### Windows

Télécharger Python depuis :\
https://www.python.org/downloads/


------------------------------------------------------------------------

## 2) Bibliothèques

Aucune bibliothèque externe n'est requise.\
Le programme utilise uniquement la bibliothèque standard de Python.

------------------------------------------------------------------------

# Exécution

## Mode interactif

    1. $ python minitrice
    2. > 3+9
    3. 12
    4. >
    5. Fin des calculs :)
    6. $ echo $?
    7. 0
    8. $

------------------------------------------------------------------------

## Utilisation avec echo

    1. $ echo "3+12" | python minitrice
    2. 15
    3. $ echo $?
    4. 0
    5. $

------------------------------------------------------------------------

## Utilisation avec un fichier

    1. $ cat good-expression.txt | python minitrice
    2. 15
    3. 27
    4. 42
    5. $ echo $?
    6. 0
    7. $

------------------------------------------------------------------------

## Erreur de syntaxe

    1. $ echo "3+*12" | python minitrice
    2. SyntaxError
    3. $ echo $?
    4. 1
    5. $

------------------------------------------------------------------------

## Division par zéro

    1. $ echo "3/0" | python minitrice
    2. ZeroDivisionError
    3. $ echo $?
    4. 2
    5. $

------------------------------------------------------------------------

# Generator

Le programme `generator` permet de générer automatiquement des
expressions mathématiques valides.

------------------------------------------------------------------------

## Utilisation normale

    1. $ python generator 3
    2. 12+45
    3. 78-3
    4. 5*9
    5. $

------------------------------------------------------------------------

## Utilisation avec minitrice (pipe)

    1. $ python generator 3 | python minitrice
    2. 57
    3. 75
    4. 45
    5. $

------------------------------------------------------------------------

# Gestion des erreurs du Generator

## Argument manquant

    1. $ python generator
    2. Usage: python generator <nombre_expressions>
    3. $

------------------------------------------------------------------------

## Argument non numérique

    1. $ python generator abc
    2. Error: argument must be an integer
    3. $

------------------------------------------------------------------------

## Argument nul ou négatif

    1. $ python generator 0
    2. Error: argument must be a positive integer
    3. $

ou

    1. $ python generator -5
    2. Error: argument must be a positive integer
    3. $
------------------------------------------------------------------------

# Publication

Lien vidéo YouTube : https://youtu.be/FeEE8FHKFLk