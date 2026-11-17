---
title: "Module 3 - Les opérateurs en Python"
permalink: /module-3/
---

# Module 3 — Les opérateurs en Python

*Cours de programmation Python — Niveau débutant*

Lors des séances précédentes, nous avons appris à afficher des informations avec `print()` et à les enregistrer dans des variables.

Mais un programme informatique ne sert pas uniquement à stocker des données. Il doit également pouvoir effectuer des calculs, comparer des valeurs et manipuler des informations.

Prenons un exemple simple : vous travaillez au service de la scolarité d'un établissement. Vous souhaitez calculer la moyenne d'un étudiant, vérifier s'il a payé ses frais d'inscription ou déterminer le montant restant à régler.

Pour réaliser ces opérations, nous avons besoin des **opérateurs**.

## 1. Effectuer des calculs avec Python

Python peut être utilisé comme une véritable calculatrice. Il dispose de plusieurs opérateurs arithmétiques permettant d'effectuer les opérations mathématiques courantes.

Commençons par les quatre opérations que vous connaissez déjà.

### L'addition, la soustraction, la multiplication et la division

| Opérateur | Opération | Exemple | Résultat |
|---|---|---|---:|
| `+` | Addition | `10 + 5` | 15 |
| `-` | Soustraction | `10 - 5` | 5 |
| `*` | Multiplication | `10 * 5` | 50 |
| `/` | Division | `10 / 5` | 2.0 |

Essayons directement dans Python :

```python
a = 10
b = 5

print(a + b)
print(a - b)
print(a * b)
print(a / b)
```

Résultat :

```text
15
5
50
2.0
```

Vous remarquez que la division avec `/` donne ici `2.0` et non `2`. En Python, l'opérateur `/` produit un résultat de type `float`, même lorsque la division tombe juste.

### Les autres opérateurs arithmétiques

Python propose également trois autres opérateurs particulièrement utiles.

**La division entière `//`**

Elle permet d'obtenir uniquement la partie entière du résultat d'une division.

```python
print(17 // 5)
```

Résultat :

```text
3
```

En effet, 17 divisé par 5 donne 3,4. La division entière conserve ici uniquement 3.

**Le modulo `%`**

Il permet de récupérer le reste d'une division.

```python
print(17 % 5)
```

Résultat :

```text
2
```

Car 17 divisé par 5 donne 3, avec un reste de 2.

Cet opérateur est notamment utilisé pour vérifier si un nombre est pair ou impair.

```python
nombre = 8

print(nombre % 2)
```

Résultat :

```text
0
```

Si le reste d'une division par 2 est égal à zéro, le nombre est pair.

**La puissance `**`**

Elle permet d'élever un nombre à une puissance.

```python
print(2 ** 3)
```

Résultat :

```text
8
```

Cela correspond à 2 × 2 × 2.

### Récapitulons

| Opérateur | Signification | Exemple | Résultat |
|---|---|---|---:|
| `+` | Addition | `8 + 2` | 10 |
| `-` | Soustraction | `8 - 2` | 6 |
| `*` | Multiplication | `8 * 2` | 16 |
| `/` | Division | `8 / 2` | 4.0 |
| `//` | Division entière | `17 // 5` | 3 |
| `%` | Reste de division | `17 % 5` | 2 |
| `**` | Puissance | `2 ** 3` | 8 |

## 2. Utiliser les opérateurs avec des variables

Jusqu'ici, nous avons réalisé des calculs directement avec des nombres. En pratique, nous utiliserons très souvent des variables.

Imaginons qu'un étudiant dispose de 20 000 FCFA et qu'il décide de payer 5 000 FCFA de frais.

```python
solde = 20000
paiement = 5000

reste = solde - paiement

print(f"Solde initial : {solde} FCFA")
print(f"Paiement effectué : {paiement} FCFA")
print(f"Montant restant : {reste} FCFA")
```

Résultat :

```text
Solde initial : 20000 FCFA
Paiement effectué : 5000 FCFA
Montant restant : 15000 FCFA
```

L'intérêt est simple : nous pouvons modifier les valeurs des variables sans avoir à réécrire tout le programme.

Essayez maintenant de remplacer le paiement de 5 000 par 8 000. Le résultat changera automatiquement.

## 3. Simplifier les affectations

Vous avez déjà rencontré une instruction comme celle-ci dans le module précédent :

```python
solde = solde + 5000
```

Python propose une écriture plus courte pour réaliser la même opération :

```python
solde += 5000
```

On appelle cela une **affectation augmentée**.

Elle permet de modifier directement la valeur d'une variable en utilisant un opérateur.

| Écriture simplifiée | Écriture équivalente |
|---|---|
| `x += 5` | `x = x + 5` |
| `x -= 5` | `x = x - 5` |
| `x *= 2` | `x = x * 2` |
| `x /= 2` | `x = x / 2` |
| `x //= 2` | `x = x // 2` |
| `x %= 2` | `x = x % 2` |
| `x **= 2` | `x = x ** 2` |

Prenons un exemple :

```python
points = 10

points += 5
points -= 2
points *= 2

print(points)
```

Résultat :

```text
26
```

Le calcul se déroule progressivement :

- Au départ, `points` vaut 10.
- Après `points += 5`, il vaut 15.
- Après `points -= 2`, il vaut 13.
- Après `points *= 2`, il vaut 26.

Prenez l'habitude de reconnaître ces écritures. Vous les rencontrerez régulièrement dans vos programmes.

## 4. Comparer des valeurs

Un programme doit parfois vérifier si une information respecte une condition.

Par exemple :

- Un étudiant a-t-il obtenu une moyenne supérieure ou égale à 10 ?
- Un paiement est-il suffisant ?
- Deux mots sont-ils identiques ?
- Un étudiant a-t-il exactement 18 ans ?

Pour répondre à ces questions, nous utilisons les **opérateurs de comparaison**.

Voici les principaux :

| Opérateur | Signification | Exemple | Résultat |
|---|---|---|---|
| `==` | Égal à | `10 == 10` | `True` |
| `!=` | Différent de | `10 != 5` | `True` |
| `>` | Supérieur à | `10 > 5` | `True` |
| `<` | Inférieur à | `5 < 10` | `True` |
| `>=` | Supérieur ou égal à | `10 >= 10` | `True` |
| `<=` | Inférieur ou égal à | `5 <= 10` | `True` |

Attention à ne pas confondre `=` et `==` :

- `=` permet d'affecter une valeur à une variable.
- `==` permet de vérifier si deux valeurs sont égales.

Exemple :

```python
age = 20

print(age == 20)
print(age > 18)
print(age < 18)
```

Résultat :

```text
True
True
False
```

Pourquoi ?

- `age == 20` est vrai, car l'âge est exactement 20.
- `age > 18` est vrai, car 20 est supérieur à 18.
- `age < 18` est faux, car 20 n'est pas inférieur à 18.

Vous remarquerez que les comparaisons produisent toujours un résultat booléen : `True` ou `False`.

C'est justement ce résultat qui permettra à un programme de prendre des décisions.

## 5. Combiner plusieurs conditions

Il arrive que nous ayons besoin de vérifier plusieurs conditions en même temps.

Imaginons qu'un étudiant puisse accéder à un examen uniquement si son inscription est validée et s'il a réglé ses frais.

Python propose trois opérateurs logiques pour gérer ces situations : `and`, `or` et `not`.

### L'opérateur `and`

L'opérateur `and` signifie « ET ».

Il renvoie `True` uniquement lorsque toutes les conditions sont vraies.

```python
inscription_validee = True
frais_payes = True

autorisation = inscription_validee and frais_payes

print(autorisation)
```

Résultat :

```text
True
```

Si l'une des deux conditions devient fausse, le résultat sera `False`.

### L'opérateur `or`

L'opérateur `or` signifie « OU ».

Il renvoie `True` lorsqu'au moins une des conditions est vraie.

```python
est_boursier = False
a_paye = True

acces_autorise = est_boursier or a_paye

print(acces_autorise)
```

Résultat :

```text
True
```

Ici, l'étudiant n'est pas boursier, mais il a payé. L'une des conditions étant vraie, le résultat est `True`.

### L'opérateur `not`

L'opérateur `not` permet d'inverser une valeur logique.

```python
est_absent = False

print(not est_absent)
```

Résultat :

```text
True
```

Puisque `est_absent` vaut `False`, l'expression `not est_absent` renvoie `True`.

### Tableau récapitulatif

| Expression | Résultat |
|---|---|
| `True and True` | `True` |
| `True and False` | `False` |
| `False and False` | `False` |
| `True or False` | `True` |
| `False or False` | `False` |
| `not True` | `False` |
| `not False` | `True` |

Retenez bien ces trois opérateurs. Ils seront indispensables lorsque nous aborderons les conditions avec `if`, `elif` et `else`.

## 6. Comprendre l'ordre des opérations

Comme en mathématiques, Python respecte un ordre de priorité lorsqu'il effectue plusieurs opérations dans une même expression.

Par exemple :

```python
resultat = 10 + 5 * 2

print(resultat)
```

Résultat :

```text
20
```

Pourquoi n'obtient-on pas 30 ?

Parce que la multiplication est effectuée avant l'addition.

Pour modifier cet ordre, vous pouvez utiliser des parenthèses :

```python
resultat = (10 + 5) * 2

print(resultat)
```

Résultat :

```text
30
```

Les parenthèses permettent donc de préciser l'ordre dans lequel les opérations doivent être effectuées.

**Conseil :** lorsque vos calculs deviennent complexes, utilisez des parenthèses pour rendre vos expressions plus lisibles et éviter les erreurs.

## 7. Mettre les opérateurs en pratique

Nous allons maintenant utiliser les notions étudiées dans des situations concrètes.

### Exercice 1 — Les opérations de base

Créez deux variables :

```python
a = 20
b = 6
```

Effectuez les opérations suivantes et affichez chaque résultat :

1. L'addition.
2. La soustraction.
3. La multiplication.
4. La division.
5. La division entière.
6. Le reste de la division.
7. La puissance de `a` à la puissance `b`.

### Exercice 2 — Gestion d'un solde

Un étudiant dispose de 50 000 FCFA.

Il effectue les opérations suivantes :

- Il paie 15 000 FCFA.
- Il reçoit ensuite 10 000 FCFA.
- Il dépense encore 5 000 FCFA.

Travail demandé :

1. Créez une variable `solde` contenant 50 000.
2. Utilisez les affectations augmentées pour mettre à jour le solde.
3. Affichez le montant restant.

### Exercice 3 — Comparer des notes

Un étudiant obtient les notes suivantes :

```python
note = 14
```

Écrivez des expressions permettant de vérifier :

1. Si la note est égale à 14.
2. Si la note est supérieure à 10.
3. Si la note est inférieure à 10.
4. Si la note est supérieure ou égale à 10.
5. Si la note est différente de 12.

Affichez les résultats de chaque comparaison.

### Exercice 4 — Vérifier une inscription

Un étudiant possède les informations suivantes :

```python
inscription_validee = True
frais_payes = False
```

À l'aide des opérateurs logiques, vérifiez :

1. Si l'inscription est validée ET si les frais sont payés.
2. Si l'inscription est validée OU si les frais sont payés.
3. Si les frais ne sont pas payés.

Affichez les trois résultats.

### Exercice 5 — Calculer le prix total

Un étudiant achète :

- 3 cahiers à 1 000 FCFA l'unité.
- 2 stylos à 500 FCFA l'unité.
- 1 sac à 8 000 FCFA.

Écrivez un programme qui :

1. Stocke les quantités et les prix unitaires dans des variables.
2. Calcule le montant de chaque catégorie.
3. Calcule le montant total.
4. Affiche une petite facture.

Exemple de présentation :

```text
========== FACTURE ==========

Cahiers : 3000 FCFA
Stylos : 1000 FCFA
Sac : 8000 FCFA

Total à payer : 12000 FCFA
=============================
```

### Exercice 6 — Vérifier si un nombre est pair

Créez une variable `nombre` contenant un entier.

Utilisez l'opérateur modulo `%` pour déterminer si le nombre est divisible par 2.

Affichez le résultat de votre vérification.

**Indice :** si le reste de la division par 2 est égal à zéro, le nombre est pair.

### Exercice 7 — Calculer une moyenne

Un étudiant a obtenu les notes suivantes :

| Matière | Note |
|---|---:|
| Algorithmique | 15 |
| Programmation | 12 |
| Mathématiques | 14 |

Écrivez un programme qui :

1. Enregistre les trois notes dans des variables.
2. Calcule la somme des notes.
3. Calcule la moyenne.
4. Vérifie si la moyenne est supérieure ou égale à 10.
5. Affiche la moyenne et le résultat de la comparaison.

---

## 8. Mini-projet : calculateur de frais d'inscription

Pour terminer ce module, nous allons réaliser un programme inspiré d'une situation réelle de gestion de la scolarité.

Un étudiant doit régler les frais suivants :

| Désignation | Montant |
|---|---:|
| Frais de dossier | 25 000 FCFA |
| Inscription | 200 000 FCFA |
| Première mensualité | 60 000 FCFA |

Il dispose actuellement de 250 000 FCFA.

Votre objectif est de créer un programme qui calcule le montant total à payer et vérifie si l'étudiant dispose d'un montant suffisant.

**Travail demandé :**

1. Créez une variable pour chaque frais.
2. Calculez le montant total.
3. Créez une variable contenant le montant disponible.
4. Comparez le montant disponible au montant total.
5. Calculez le reste à payer si le montant disponible est insuffisant.
6. Affichez les différents résultats.

Votre programme doit utiliser :

- Les variables.
- Les opérateurs arithmétiques.
- Les opérateurs de comparaison.
- Les opérateurs logiques si nécessaire.
- Les f-strings pour présenter les résultats.

Exemple de présentation :

```text
=================================
       CALCUL DES FRAIS
=================================

Frais de dossier : 25 000 FCFA
Inscription : 200 000 FCFA
Première mensualité : 60 000 FCFA

Total à payer : 285 000 FCFA
Montant disponible : 250 000 FCFA

Montant restant à payer : 35 000 FCFA

Paiement suffisant : False

=================================
```

Essayez de réaliser ce programme sans reprendre directement les lignes de code des exemples précédents.

---

## 9. Vérifier ce que vous avez appris

Avant de passer à la prochaine séance, assurez-vous de pouvoir réaliser les opérations suivantes :

- [ ] Utiliser les opérateurs arithmétiques.
- [ ] Faire la différence entre `/`, `//` et `%`.
- [ ] Utiliser l'opérateur de puissance `**`.
- [ ] Modifier une variable avec `+=`, `-=`, `*=` et `/=`.
- [ ] Comparer deux valeurs.
- [ ] Comprendre les résultats `True` et `False`.
- [ ] Combiner plusieurs conditions avec `and`, `or` et `not`.
- [ ] Respecter l'ordre des opérations.
- [ ] Réaliser le mini-projet de calcul des frais.

---

Les opérateurs permettent à un programme de réaliser des calculs et d'analyser des informations. Vous disposez maintenant des outils nécessaires pour manipuler les données que vous avez apprises à stocker dans les variables.

La prochaine étape sera particulièrement intéressante : nous apprendrons à faire prendre des décisions à nos programmes grâce aux **conditions `if`, `elif` et `else`**.

C'est à partir de là que vos programmes commenceront véritablement à réagir en fonction des informations qu'ils reçoivent.
