---
layout: default
title: Module 2 - Variables et types de données
permalink: /module-2/
---


# Module 2 — Les variables et les types de données en Python

*Cours de programmation Python — Niveau débutant*

Lors de la séance précédente, nous avons appris à utiliser `print()` pour afficher des informations à l'écran. Mais imaginez maintenant que nous souhaitions créer un programme capable de mémoriser le nom d'un étudiant, son âge, ses notes ou encore sa filière.

Comment le programme peut-il conserver ces informations et les réutiliser ?

C'est précisément le rôle des **variables**. Elles permettent à un programme de stocker des informations afin de les utiliser, de les modifier et de réaliser différentes opérations.

## 1. Comprendre le fonctionnement d'une variable

En programmation, une variable est un nom associé à une valeur stockée en mémoire.

Pour mieux comprendre, imaginez plusieurs boîtes. Chaque boîte possède une étiquette indiquant ce qu'elle contient.

En Python, nous pouvons créer ces boîtes de la manière suivante :

```python
nom = "Mamadou"
age = 22
ville = "Dakar"
```

Nous avons créé trois variables :

- `nom` contient le texte `"Mamadou"`.
- `age` contient le nombre `22`.
- `ville` contient le texte `"Dakar"`.

Le symbole `=` permet d'affecter une valeur à une variable. Il indique à Python que nous voulons enregistrer une information sous un nom précis.

Essayons maintenant d'afficher ces informations :

```python
nom = "Mamadou"
age = 22
ville = "Dakar"

print(nom)
print(age)
print(ville)
```

Résultat :

```text
Mamadou
22
Dakar
```

Vous remarquez que nous n'avons pas besoin de réécrire les informations à chaque affichage. Il suffit d'utiliser le nom de la variable.

C'est l'un des principaux avantages des variables : elles permettent de réutiliser facilement les données dans un programme.

## 2. Donner un nom à ses variables

Lorsque vous écrivez un programme, il est important de choisir des noms compréhensibles. Un autre développeur doit pouvoir lire votre code et comprendre rapidement le rôle de chaque variable.

Par exemple :

```python
n = "Aminata"
a = 21
```

Ce programme fonctionne, mais les noms `n` et `a` ne donnent aucune indication sur les informations stockées.

Il est préférable d'écrire :

```python
nom = "Aminata"
age = 21
```

Python impose quelques règles pour nommer les variables :

- Le nom peut contenir des lettres, des chiffres et le caractère `_`.
- Il ne doit pas commencer par un chiffre.
- Il ne doit pas contenir d'espace.
- Il ne doit pas être un mot réservé du langage.
- Les majuscules et les minuscules sont différentes.

Voici quelques exemples :

```python
nom_etudiant = "Mamadou"  # Correct
age2 = 22                 # Correct
note_finale = 16          # Correct

2age = 22                 # Incorrect
nom etudiant = "Mamadou"  # Incorrect
```

**Conseil :** prenez l'habitude d'utiliser des noms explicites, comme `nom_etudiant`, `moyenne_generale` ou `nombre_inscrits`. Cette bonne pratique vous aidera à écrire des programmes plus faciles à maintenir.

## 3. Les différents types de données

Toutes les informations ne sont pas de même nature. Un nom est un texte, un âge est généralement un nombre entier et une moyenne peut être un nombre décimal.

Python distingue les données à l'aide de plusieurs types.

### Les chaînes de caractères : `str`

Le type `str` permet de stocker du texte.

```python
nom = "Mamadou"
filiere = "Informatique"
etablissement = "DakarTech"
```

Pour indiquer à Python qu'il s'agit d'un texte, il faut utiliser des guillemets simples ou doubles.

```python
ville = "Dakar"
pays = 'Sénégal'
```

Les deux écritures sont correctes.

### Les nombres entiers : `int`

Le type `int` représente les nombres entiers, c'est-à-dire les nombres sans partie décimale.

```python
age = 22
nombre_etudiants = 35
annee = 2026
```

Vous pouvez utiliser ces variables dans des calculs :

```python
age = 22
age_suivant = age + 1

print(age_suivant)
```

Résultat :

```text
23
```

### Les nombres décimaux : `float`

Le type `float` permet de représenter les nombres comportant une partie décimale.

```python
moyenne = 14.5
prix = 2500.75
taille = 1.75
```

Attention : en Python, le séparateur décimal est le point et non la virgule.

Écrivez `14.5` et non `14,5`.

### Les valeurs booléennes : `bool`

Certaines informations ne peuvent prendre que deux valeurs : vrai ou faux.

Python utilise le type `bool` pour représenter ces situations :

```python
est_inscrit = True
a_paye = False
```

- `True` signifie vrai.
- `False` signifie faux.

Ces valeurs seront particulièrement importantes lorsque nous étudierons les conditions.

Retenons les quatre types principaux :

| Type | Utilisation | Exemple |
|---|---|---|
| `str` | Stocker du texte | `"Dakar"` |
| `int` | Stocker un entier | `25` |
| `float` | Stocker un nombre décimal | `15.5` |
| `bool` | Stocker une valeur logique | `True` |

## 4. Afficher les variables dans une phrase

Jusqu'à présent, nous avons utilisé `print()` pour afficher séparément le contenu de nos variables.

Mais dans un véritable programme, nous avons souvent besoin de présenter plusieurs informations dans une phrase.

Prenons l'exemple d'un étudiant :

```python
nom = "Aminata"
age = 21

print("Je m'appelle", nom)
print("J'ai", age, "ans")
```

Résultat :

```text
Je m'appelle Aminata
J'ai 21 ans
```

Python permet également de construire une phrase complète grâce aux **f-strings**.

```python
nom = "Aminata"
age = 21

print(f"Je m'appelle {nom} et j'ai {age} ans.")
```

Résultat :

```text
Je m'appelle Aminata et j'ai 21 ans.
```

Observez la syntaxe :

- La lettre `f` est placée avant les guillemets.
- Les variables sont insérées entre accolades `{}`.
- Python remplace automatiquement les accolades par les valeurs correspondantes.

Les f-strings sont très pratiques pour présenter des résultats, générer des messages ou afficher des informations dans une application.

## 5. Modifier une variable

Une variable n'est pas obligée de conserver la même valeur pendant toute l'exécution du programme.

Prenons l'exemple d'un étudiant dont l'âge est initialement de 20 ans.

```python
age = 20

print(age)

age = 21

print(age)
```

Résultat :

```text
20
21
```

La deuxième affectation remplace la première valeur.

Nous pouvons également modifier une variable en utilisant sa valeur précédente.

Considérons le solde d'un étudiant qui effectue un dépôt de 5 000 FCFA.

```python
solde = 10000

solde = solde + 5000

print(solde)
```

Résultat :

```text
15000
```

Que s'est-il passé ?

1. Le solde initial est de 10 000 FCFA.
2. Nous ajoutons 5 000 FCFA à cette valeur.
3. Le nouveau résultat est enregistré dans la variable `solde`.
4. Python affiche le nouveau solde.

Vous pouvez également écrire cette opération de manière plus courte :

```python
solde += 5000
```

Cette écriture signifie exactement la même chose que :

```python
solde = solde + 5000
```

Nous reviendrons sur ces raccourcis lorsque nous étudierons les opérateurs.

## 6. Vérifier le type d'une donnée

Il arrive que vous ne sachiez pas exactement quel type de donnée contient une variable. Python propose une fonction très utile pour répondre à cette question : `type()`.

Exemple :

```python
nom = "Mamadou"
age = 22
moyenne = 14.5
est_inscrit = True

print(type(nom))
print(type(age))
print(type(moyenne))
print(type(est_inscrit))
```

Résultat :

```text
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
```

Cette fonction permet de vérifier la nature des données utilisées dans un programme.

Il est important de comprendre qu'une donnée écrite entre guillemets est considérée comme du texte, même lorsqu'elle contient uniquement des chiffres.

Comparez :

```python
age = 22
numero = "221"

print(type(age))
print(type(numero))
```

Résultat :

```text
<class 'int'>
<class 'str'>
```

Dans le premier cas, `22` est un entier. Dans le second, `"221"` est une chaîne de caractères.

Cette différence est importante : Python ne traite pas un texte et un nombre de la même manière.

## 7. Quelques erreurs à éviter

Lorsque vous débutez, certaines erreurs reviennent fréquemment. Apprenez à les identifier.

**Oublier les guillemets autour d'un texte :**

```python
nom = Mamadou
```

Python cherchera une variable appelée `Mamadou` et pourra afficher une erreur si elle n'existe pas.

La bonne écriture est :

```python
nom = "Mamadou"
```

**Utiliser une virgule pour un nombre décimal :**

```python
moyenne = 15,5
```

Cette écriture ne crée pas un nombre décimal. Utilisez plutôt :

```python
moyenne = 15.5
```

**Confondre les majuscules et les minuscules :**

```python
nom = "Mamadou"

print(Nom)
```

Ici, `nom` et `Nom` sont deux noms différents. Python fait la distinction entre les majuscules et les minuscules.

La correction est :

```python
nom = "Mamadou"

print(nom)
```

---

## 8. Exercices d'application

Vous connaissez maintenant les variables et les principaux types de données. Il est temps de passer à la pratique.

Je vous conseille de créer un fichier Python pour chaque exercice et de tester votre programme après chaque modification.

### Exercice 1 — Créer ses premières variables

Créez cinq variables contenant les informations suivantes :

- Votre nom.
- Votre prénom.
- Votre âge.
- Votre ville.
- Votre filière.

Affichez ensuite toutes les informations à l'écran.

**Objectif :** apprendre à créer et à afficher des variables.

### Exercice 2 — Reconnaître les types de données

Considérez le programme suivant :

```python
nom = "Fatou"
age = 23
moyenne = 13.75
admis = True
```

Travail demandé :

1. Indiquez le type de chaque variable sans exécuter le programme.
2. Utilisez `type()` pour vérifier vos réponses.
3. Affichez les quatre variables.

### Exercice 3 — Faire évoluer une valeur

Observez le programme suivant :

```python
solde = 15000

solde = solde + 5000
solde = solde - 3000

print(solde)
```

Répondez aux questions suivantes :

1. Quelle est la valeur initiale du solde ?
2. Quelle est sa valeur après l'ajout de 5 000 ?
3. Quelle est sa valeur après le retrait de 3 000 ?
4. Quel résultat sera affiché ?

Essayez de trouver les réponses avant d'exécuter le programme.

### Exercice 4 — Présenter un étudiant

Écrivez un programme qui stocke les informations d'un étudiant :

- Nom et prénom.
- Âge.
- Filière.
- Niveau d'études.

Utilisez une f-string pour afficher une présentation complète.

Exemple de résultat attendu :

```text
Je m'appelle Mamadou FALL.
J'ai 22 ans.
Je suis étudiant en Informatique, niveau Licence 1.
```

### Exercice 5 — Calculer une moyenne

Un étudiant a obtenu les notes suivantes :

| Matière | Note |
|---|---:|
| Algorithmique | 14 |
| Mathématiques | 12 |
| Programmation | 16 |

Écrivez un programme qui :

1. Stocke chaque note dans une variable.
2. Calcule la somme des trois notes.
3. Calcule la moyenne.
4. Affiche le résultat avec un message explicatif.

### Exercice 6 — Corriger un programme

Le programme suivant contient plusieurs erreurs.

```python
nom = Mamadou
age = "22"
moyenne = 15,5

print("Nom :", Nom)
print("Age :", age)
print("Moyenne :", moyenne)
```

Votre travail consiste à identifier les erreurs et à proposer une version corrigée du programme.

Expliquez également pourquoi chaque correction est nécessaire.

---

## 9. Mise en situation : créer une fiche d'inscription

Nous allons terminer cette séance par un petit projet inspiré d'une situation que vous connaissez : l'inscription d'un étudiant dans un établissement d'enseignement supérieur.

Imaginez que vous travaillez au service de la scolarité de DakarTech. Vous devez créer un programme qui affiche les informations d'un nouvel étudiant.

Votre programme doit enregistrer les éléments suivants :

- Le nom et le prénom.
- L'âge.
- La filière.
- Le niveau d'études.
- L'année académique.
- Le statut de validation de l'inscription.

Vous devez choisir le type de données adapté à chaque information.

Voici un exemple de résultat attendu :

```text
================================
       FICHE D'INSCRIPTION
================================

Nom et prénom : Mamadou FALL
Âge : 22 ans
Filière : Informatique
Niveau : Licence 1
Année académique : 2026-2027
Inscription validée : True

================================
```

**Consigne :** réalisez ce programme en utilisant les variables, les types de données et les f-strings étudiés dans cette séance.

Essayez d'abord de le faire sans reprendre exactement les exemples du cours.

---

## 10. Vérification des acquis

Avant de poursuivre votre apprentissage, vérifiez que vous êtes capable de réaliser les opérations suivantes :

- [ ] Expliquer avec vos propres mots ce qu'est une variable.
- [ ] Créer une variable et lui attribuer une valeur.
- [ ] Respecter les règles de nommage.
- [ ] Faire la différence entre `str`, `int`, `float` et `bool`.
- [ ] Afficher plusieurs variables dans une phrase.
- [ ] Utiliser les f-strings.
- [ ] Modifier la valeur d'une variable.
- [ ] Vérifier le type d'une donnée avec `type()`.
- [ ] Réaliser la fiche d'inscription sans recopier le cours.

---

**Pour terminer :**

Les variables sont présentes dans presque tous les programmes informatiques. Elles permettent de stocker des informations, de les modifier et de les utiliser dans des calculs ou des traitements.

Ne vous contentez pas de lire les exemples. Ouvrez votre éditeur Python, recopiez les programmes, modifiez les valeurs et observez les résultats.

C'est en pratiquant que vous développerez progressivement votre logique de programmation.

**Prochaine étape : les opérateurs en Python.** Nous apprendrons à effectuer des calculs, à comparer des valeurs et à manipuler les données dans nos programmes.
