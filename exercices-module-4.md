---
title: "Exercices - Module 4 : Les opérateurs en Python"
permalink: /exercices-module-4/
---

# Travaux pratiques — Module 4 : Les opérateurs en Python

Après avoir étudié les opérateurs arithmétiques, les opérateurs de comparaison et les opérateurs logiques, il est temps de vérifier votre compréhension à travers des exercices pratiques.

L'objectif n'est pas simplement d'obtenir le bon résultat, mais aussi de comprendre comment construire un programme capable de réaliser une opération.

**Consignes générales :**

- Réalisez chaque exercice dans un fichier Python.
- Donnez des noms explicites à vos variables.
- Utilisez `print()` pour afficher les résultats.
- Privilégiez les f-strings pour présenter vos résultats.
- Essayez de résoudre chaque exercice avant de consulter une éventuelle correction.
- Lorsque c'est demandé, expliquez votre raisonnement.

---

## Partie 1 — Se familiariser avec les opérateurs

### Exercice 1 : Ma première calculatrice

Créez deux variables :

```python
a = 25
b = 7
```

À partir de ces deux variables, effectuez les opérations suivantes :

1. L'addition de `a` et `b`.
2. La soustraction de `b` à `a`.
3. La multiplication de `a` par `b`.
4. La division de `a` par `b`.
5. La division entière de `a` par `b`.
6. Le reste de la division de `a` par `b`.
7. La puissance de `a` à la puissance `b`.

**Travail supplémentaire :** affichez chaque opération sous la forme suivante :

```text
25 + 7 = 32
25 - 7 = 18
```

### Exercice 2 : Comprendre le reste d'une division

On vous donne les nombres suivants :

```python
a = 18
b = 5
c = 24
```

Sans exécuter le programme, déterminez les résultats des expressions suivantes :

```python
print(a % 2)
print(b % 2)
print(c % 2)
print(a % b)
print(c % b)
```

Répondez ensuite aux questions :

1. Quel est le reste de la division de 18 par 2 ?
2. Quel est le reste de la division de 5 par 2 ?
3. Quels nombres sont pairs ?
4. Quels nombres sont impairs ?
5. Pourquoi l'opérateur `%` est-il utile pour identifier un nombre pair ou impair ?

### Exercice 3 : Modifier une variable

Considérez le programme suivant :

```python
nombre = 10

nombre += 5
nombre *= 2
nombre -= 8
nombre /= 2

print(nombre)
```

**Travail demandé :**

1. Déterminez la valeur de `nombre` après chaque instruction.
2. Trouvez le résultat final sans exécuter le programme.
3. Vérifiez votre réponse avec Python.
4. Expliquez le rôle de chaque opérateur utilisé.

---

## Partie 2 — Comparer et analyser des valeurs

### Exercice 4 : Les opérateurs de comparaison

On vous donne les variables suivantes :

```python
age = 22
note = 14
moyenne = 9.5
```

Écrivez des expressions permettant de vérifier :

1. Si l'âge est égal à 22.
2. Si l'âge est supérieur à 18.
3. Si la note est supérieure ou égale à 10.
4. Si la moyenne est inférieure à 10.
5. Si la note est différente de 12.
6. Si l'âge est inférieur ou égal à 25.

Affichez les résultats de toutes les comparaisons.

### Exercice 5 : Comprendre les résultats booléens

Sans exécuter le code, indiquez si chaque expression renvoie `True` ou `False`.

```python
print(10 > 5)
print(8 == 10)
print(15 != 12)
print(20 <= 20)
print(7 >= 9)
print(12 < 15)
```

Ensuite, exécutez le programme pour vérifier vos réponses.

### Exercice 6 : Combiner plusieurs conditions

Un étudiant peut bénéficier d'une réduction sur ses frais de scolarité s'il est boursier ou s'il bénéficie d'une aide particulière.

On dispose des informations suivantes :

```python
est_boursier = True
beneficie_aide = False
```

**Travail demandé :**

1. Vérifiez si l'étudiant est boursier ET bénéficie d'une aide.
2. Vérifiez s'il est boursier OU bénéficie d'une aide.
3. Vérifiez s'il n'est pas boursier.
4. Affichez les trois résultats.

Modifiez ensuite les valeurs des variables et observez les changements.

---

## Partie 3 — Appliquer les opérateurs à des situations concrètes

### Exercice 7 : Calculer le prix d'un achat

Un étudiant se rend dans une librairie et achète :

| Article | Quantité | Prix unitaire |
|---|---:|---:|
| Cahier | 4 | 1 000 FCFA |
| Stylo | 3 | 500 FCFA |
| Classeur | 2 | 2 500 FCFA |

**Travail demandé :**

1. Créez une variable pour chaque quantité.
2. Créez une variable pour chaque prix unitaire.
3. Calculez le montant de chaque catégorie.
4. Calculez le montant total de l'achat.
5. Affichez une facture récapitulative.

Résultat attendu :

```text
========== FACTURE ==========

Cahiers : 4000 FCFA
Stylos : 1500 FCFA
Classeurs : 5000 FCFA

Total à payer : 10500 FCFA

=============================
```

### Exercice 8 : Calculer une moyenne générale

Un étudiant a obtenu les notes suivantes :

| Matière | Note |
|---|---:|
| Algorithmique | 15 |
| Programmation | 12 |
| Mathématiques | 14 |
| Anglais | 16 |

**Travail demandé :**

1. Enregistrez les quatre notes dans des variables.
2. Calculez la somme des notes.
3. Calculez la moyenne générale.
4. Vérifiez si la moyenne est supérieure ou égale à 10.
5. Vérifiez si la moyenne est supérieure ou égale à 15.
6. Affichez les résultats.

**Attention :** à ce stade, vous devez uniquement afficher les résultats des comparaisons. Nous étudierons prochainement comment utiliser ces résultats pour exécuter différentes instructions.

### Exercice 9 : Gestion d'un compte bancaire

Un client possède un compte avec un solde initial de 150 000 FCFA.

Il effectue les opérations suivantes :

- Dépôt de 50 000 FCFA.
- Retrait de 25 000 FCFA.
- Retrait supplémentaire de 10 000 FCFA.

**Travail demandé :**

1. Créez une variable `solde`.
2. Utilisez les affectations augmentées pour effectuer les dépôts et les retraits.
3. Calculez le solde final.
4. Vérifiez si le solde est supérieur à 100 000 FCFA.
5. Vérifiez si le solde est inférieur à 200 000 FCFA.
6. Affichez le résultat.

### Exercice 10 : Vérifier les conditions d'accès à un examen

Un établissement souhaite vérifier si un étudiant remplit certaines conditions administratives pour accéder à un examen.

Les informations disponibles sont :

```python
inscription_validee = True
frais_payes = True
dossier_complet = False
```

L'étudiant doit avoir une inscription validée, avoir payé ses frais et posséder un dossier complet.

**Travail demandé :**

1. Créez une expression avec `and` pour vérifier les trois conditions.
2. Affichez le résultat.
3. Modifiez les valeurs pour rendre les trois conditions vraies.
4. Testez également les cas où une seule condition est fausse.

### Exercice 11 : Calculer l'âge et vérifier une condition

Une personne est née en 2004.

**Travail demandé :**

1. Créez une variable contenant son année de naissance.
2. Créez une variable contenant l'année actuelle : 2026.
3. Calculez son âge approximatif.
4. Vérifiez si son âge est supérieur ou égal à 18 ans.
5. Vérifiez si son âge est inférieur à 25 ans.
6. Combinez les deux comparaisons avec `and`.

*Remarque : pour cet exercice, on suppose que l'anniversaire de la personne est déjà passé en 2026.*

---

## Partie 4 — Développer sa logique

### Exercice 12 : Trouver le résultat d'une expression

Sans exécuter les programmes, déterminez les résultats.

**Programme A :**

```python
resultat = 10 + 5 * 2
print(resultat)
```

**Programme B :**

```python
resultat = (10 + 5) * 2
print(resultat)
```

**Programme C :**

```python
resultat = 20 / 4 + 3 ** 2
print(resultat)
```

**Questions :**

1. Pourquoi les programmes A et B ne donnent-ils pas le même résultat ?
2. Quelle opération est exécutée en premier dans le programme C ?
3. Quel est le rôle des parenthèses dans une expression mathématique ?

### Exercice 13 : Calculer une réduction

Un magasin propose une réduction de 10 % sur un article dont le prix initial est de 50 000 FCFA.

**Travail demandé :**

1. Créez une variable contenant le prix initial.
2. Créez une variable contenant le taux de réduction.
3. Calculez le montant de la réduction.
4. Calculez le prix après réduction.
5. Affichez le prix initial, la réduction et le prix final.

### Exercice 14 : Répartir des étudiants en groupes

Un établissement souhaite répartir 53 étudiants en groupes de 5 personnes.

**Travail demandé :**

1. Créez une variable `nombre_etudiants`.
2. Créez une variable `taille_groupe`.
3. Calculez le nombre de groupes complets avec `//`.
4. Calculez le nombre d'étudiants restants avec `%`.
5. Affichez les résultats.

Expliquez pourquoi il est intéressant d'utiliser simultanément `//` et `%` dans cet exercice.

---

## Partie 5 — Mini-projet

### Exercice 15 : Gestion des frais de scolarité

Vous travaillez au service de la scolarité d'un établissement supérieur.

Un étudiant doit régler les frais suivants :

| Désignation | Montant |
|---|---:|
| Frais de dossier | 25 000 FCFA |
| Inscription | 200 000 FCFA |
| Première mensualité | 60 000 FCFA |

L'étudiant dispose actuellement de 250 000 FCFA.

Votre mission consiste à développer un programme permettant de calculer le montant total des frais et de vérifier si l'étudiant dispose d'un montant suffisant.

**Travail demandé :**

1. Créez une variable pour chaque frais.
2. Calculez le montant total à payer.
3. Créez une variable contenant le montant disponible.
4. Calculez la différence entre le montant disponible et le montant total.
5. Vérifiez si le montant disponible est supérieur ou égal au montant total.
6. Vérifiez si le montant disponible est inférieur au montant total.
7. Affichez les différentes informations sous forme de récapitulatif.

**Résultat attendu :**

```text
=================================
       FRAIS DE SCOLARITÉ
=================================

Frais de dossier : 25000 FCFA
Inscription : 200000 FCFA
Première mensualité : 60000 FCFA

Total à payer : 285000 FCFA
Montant disponible : 250000 FCFA

Différence : -35000 FCFA
Paiement suffisant : False

Reste à payer : 35000 FCFA

=================================
```

**Pour aller plus loin :**

Modifiez les données afin que l'étudiant dispose de 300 000 FCFA.

Observez les changements dans les résultats et expliquez ce qui se passe.

---

## Quelques défis supplémentaires

Si vous avez terminé les exercices précédents, essayez ces petits défis sans reprendre directement les exemples du cours.

**Défi 1 :** créez un programme qui échange les valeurs de deux variables.

Exemple :

```python
a = 10
b = 20
```

Résultat attendu :

```text
a = 20
b = 10
```

**Défi 2 :** créez un programme qui vérifie si un nombre est divisible à la fois par 3 et par 5.

**Défi 3 :** un étudiant a obtenu trois notes. Créez un programme qui calcule sa moyenne et vérifie si celle-ci est comprise entre 10 et 20 inclus.

---

## Autoévaluation

À la fin de ces travaux pratiques, vous devriez être capables de :

- [ ] Effectuer les opérations arithmétiques en Python.
- [ ] Utiliser les opérateurs de division entière et de modulo.
- [ ] Modifier une variable avec les affectations augmentées.
- [ ] Comparer deux ou plusieurs valeurs.
- [ ] Comprendre les résultats booléens.
- [ ] Combiner plusieurs conditions avec `and`, `or` et `not`.
- [ ] Respecter l'ordre des opérations.
- [ ] Résoudre un problème simple en utilisant plusieurs opérateurs.

**Un dernier conseil :** ne vous découragez pas si certains exercices vous semblent difficiles. Essayez de décomposer chaque problème en petites étapes, identifiez les informations dont vous disposez et déterminez les opérations nécessaires.

En programmation, apprendre à réfléchir et à résoudre un problème est aussi important que connaître les instructions du langage.

**Prochaine séance : les conditions en Python (`if`, `elif` et `else`).**
