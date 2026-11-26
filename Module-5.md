---
title: "Module 5 - Les conditions en Python"
permalink: /module-5/
---

# Module 5 - Les conditions en Python

## 1. Pourquoi utiliser les conditions ?

Imaginez que vous développez un petit programme pour une école. Vous souhaitez vérifier si un étudiant a obtenu la moyenne à son examen.

- Si sa note est supérieure ou égale à 10, il est admis.
- Si sa note est inférieure à 10, il n'est pas admis.

Comment demander à Python de faire ce choix automatiquement ?

C'est précisément le rôle des **conditions**. Elles permettent à un programme d'exécuter des instructions différentes selon qu'une situation est vraie ou fausse.

En Python, les principaux mots-clés utilisés sont :

- `if` : si une condition est vraie ;
- `elif` : sinon, si une autre condition est vraie ;
- `else` : sinon, dans tous les autres cas.

## 2. La condition `if`

La structure `if` permet d'exécuter une instruction uniquement lorsqu'une condition est vraie.

Prenons un premier exemple :

```python
age = 20

if age >= 18:
    print("Vous êtes majeur.")
```

Dans cet exemple, Python vérifie si `age` est supérieur ou égal à 18.

Comme la condition est vraie, le message s'affiche.

En revanche, si nous remplaçons l'âge par 15, le message ne s'affichera pas.

**À retenir :** après une condition `if`, on utilise deux-points `:`. Les instructions qui dépendent de cette condition doivent être indentées, c'est-à-dire décalées vers la droite.

Exemple :

```python
temperature = 30

if temperature > 25:
    print("Il fait chaud.")
    print("Pensez à vous hydrater.")

print("Fin du programme.")
```

Les deux premières instructions appartiennent au bloc `if`. La dernière instruction s'exécute dans tous les cas.

## 3. Ajouter une alternative avec `else`

Jusqu'ici, notre programme ne faisait quelque chose que lorsque la condition était vraie.

Mais comment lui demander d'effectuer une autre action lorsque la condition est fausse ?

C'est le rôle de `else`.

```python
age = 16

if age >= 18:
    print("Vous êtes majeur.")
else:
    print("Vous êtes mineur.")
```

Cette fois, le programme choisit automatiquement entre deux possibilités.

- Si l'âge est supérieur ou égal à 18, le premier message s'affiche.
- Dans le cas contraire, le deuxième message s'affiche.

La structure générale est la suivante :

```python
if condition:
    # Instructions si la condition est vraie
else:
    # Instructions si la condition est fausse
```

## 4. Multiplier les possibilités avec `elif`

Certaines situations nécessitent plus de deux réponses possibles.

Prenons l'exemple d'un système qui apprécie le niveau d'un étudiant en fonction de sa moyenne.

Nous voulons obtenir les résultats suivants :

- Une moyenne supérieure ou égale à 16 : Très bien.
- Une moyenne supérieure ou égale à 14 : Bien.
- Une moyenne supérieure ou égale à 12 : Assez bien.
- Une moyenne supérieure ou égale à 10 : Passable.
- Une moyenne inférieure à 10 : Ajourné.

Voici comment écrire ce programme :

```python
moyenne = 14

if moyenne >= 16:
    print("Très bien")
elif moyenne >= 14:
    print("Bien")
elif moyenne >= 12:
    print("Assez bien")
elif moyenne >= 10:
    print("Passable")
else:
    print("Ajourné")
```

Python examine les conditions dans l'ordre.

Dès qu'il trouve une condition vraie, il exécute son bloc et ignore les autres possibilités.

**Attention à l'ordre des conditions !**

Dans notre exemple, il faut commencer par la moyenne la plus élevée. Si nous écrivions `moyenne >= 10` en premier, une moyenne de 16 satisferait déjà cette condition et Python afficherait « Passable ».

## 5. Utiliser les conditions avec les opérateurs logiques

Dans le module précédent, vous avez découvert les opérateurs `and`, `or` et `not`.

Nous pouvons maintenant les utiliser pour construire des conditions plus précises.

### Avec `and`

L'opérateur `and` signifie « et ».

Toutes les conditions doivent être vraies pour que le résultat soit vrai.

Exemple : un étudiant doit avoir une moyenne supérieure ou égale à 10 et avoir payé ses frais pour être autorisé à passer ses examens.

```python
moyenne = 12
frais_payes = True

if moyenne >= 10 and frais_payes:
    print("Étudiant autorisé à passer les examens.")
else:
    print("Conditions non remplies.")
```

### Avec `or`

L'opérateur `or` signifie « ou ».

Une seule condition vraie suffit.

```python
jour = "samedi"

if jour == "samedi" or jour == "dimanche":
    print("C'est le week-end.")
else:
    print("C'est un jour de semaine.")
```

### Avec `not`

L'opérateur `not` permet d'inverser une condition.

```python
connecte = False

if not connecte:
    print("Veuillez vous connecter.")
else:
    print("Bienvenue sur votre compte.")
```

## 6. Les conditions imbriquées

Il est également possible de placer une condition à l'intérieur d'une autre condition.

On parle alors de conditions imbriquées.

Prenons un exemple : avant de vérifier si un étudiant est admis, nous voulons d'abord vérifier s'il a payé ses frais.

```python
frais_payes = True
moyenne = 13

if frais_payes:
    if moyenne >= 10:
        print("Étudiant admis.")
    else:
        print("Étudiant non admis.")
else:
    print("Paiement non effectué.")
```

Le programme commence par vérifier le paiement.

- Si le paiement est effectué, il vérifie ensuite la moyenne.
- Si le paiement n'est pas effectué, il affiche directement le message correspondant.

Les conditions imbriquées sont utiles, mais évitez de les multiplier inutilement. Un programme simple est souvent plus facile à comprendre et à maintenir.

## 7. Récupérer une information avec `input()`

Jusqu'à présent, nous avons directement donné des valeurs à nos variables.

Mais dans un vrai programme, l'utilisateur doit pouvoir saisir ses propres informations.

Pour cela, Python propose la fonction `input()`.

Exemple :

```python
nom = input("Quel est votre nom ? ")

print("Bienvenue", nom)
```

La fonction `input()` permet de récupérer une saisie au clavier.

Attention : **la valeur récupérée avec `input()` est toujours de type chaîne de caractères (`str`)**, même si l'utilisateur saisit un nombre.

Si nous voulons effectuer un calcul ou une comparaison numérique, nous devons convertir cette valeur.

Exemple :

```python
age = int(input("Quel âge avez-vous ? "))

if age >= 18:
    print("Vous êtes majeur.")
else:
    print("Vous êtes mineur.")
```

Ici, `int()` transforme la saisie en nombre entier.

Pour récupérer un nombre décimal, vous pouvez utiliser `float()` :

```python
moyenne = float(input("Entrez votre moyenne : "))

if moyenne >= 10:
    print("Vous êtes admis.")
else:
    print("Vous êtes ajourné.")
```

## 8. Exemple pratique : vérifier l'admission d'un étudiant

Mettons en pratique les notions abordées avec un programme qui demande le nom et la moyenne d'un étudiant, puis affiche son résultat.

```python
nom = input("Nom de l'étudiant : ")
moyenne = float(input("Moyenne obtenue : "))

if moyenne >= 16:
    resultat = "Très bien"
elif moyenne >= 14:
    resultat = "Bien"
elif moyenne >= 12:
    resultat = "Assez bien"
elif moyenne >= 10:
    resultat = "Passable"
else:
    resultat = "Ajourné"

print("--------------------------")
print("Étudiant :", nom)
print("Moyenne :", moyenne)
print("Résultat :", resultat)
print("--------------------------")
```

Essayez ce programme avec différentes moyennes : 8, 10, 12, 14 et 17.

Observez comment Python adapte automatiquement le résultat.

## 9. Les erreurs fréquentes à éviter

Lorsque vous commencez à utiliser les conditions, certaines erreurs sont très courantes.

### Oublier les deux-points

Incorrect :

```python
if age >= 18
    print("Majeur")
```

Correct :

```python
if age >= 18:
    print("Majeur")
```

### Oublier l'indentation

Incorrect :

```python
if age >= 18:
print("Majeur")
```

Correct :

```python
if age >= 18:
    print("Majeur")
```

### Confondre `=` et `==`

- `=` sert à affecter une valeur à une variable.
- `==` sert à comparer deux valeurs.

Exemple :

```python
age = 20

if age == 20:
    print("Vous avez 20 ans.")
```

### Oublier de convertir une saisie numérique

Incorrect :

```python
age = input("Votre âge : ")

if age >= 18:
    print("Majeur")
```

Correct :

```python
age = int(input("Votre âge : "))

if age >= 18:
    print("Majeur")
```

## 10. Ce qu'il faut retenir

| Instruction | Rôle |
|---|---|
| `if` | Vérifie une première condition |
| `elif` | Vérifie une autre condition |
| `else` | Exécute une action si aucune condition précédente n'est vraie |
| `and` | Toutes les conditions doivent être vraies |
| `or` | Au moins une condition doit être vraie |
| `not` | Inverse le résultat d'une condition |
| `input()` | Récupère une saisie utilisateur |
| `int()` | Convertit une valeur en entier |
| `float()` | Convertit une valeur en nombre décimal |

Les conditions permettent à vos programmes de prendre des décisions. Vous pouvez désormais créer des programmes capables de réagir différemment selon les informations fournies par l'utilisateur.

Avant de passer au module suivant, prenez le temps de refaire les exemples sans regarder le cours. Essayez également de modifier les valeurs pour comprendre le comportement de chaque condition.

---

**Prochain module :** Les boucles en Python (`for` et `while`), pour apprendre à répéter automatiquement des instructions.
