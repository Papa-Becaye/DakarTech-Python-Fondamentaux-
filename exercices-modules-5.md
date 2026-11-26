---
title: "Exercices pratiques - Module 4 : Les conditions en Python"
permalink: /exercices-module-5/
---

# Travaux pratiques – Module 4 : Les conditions en Python

## Objectif

Dans cette série d'exercices, vous allez apprendre à utiliser les conditions pour permettre à vos programmes de prendre des décisions.

Pour chaque exercice :
- Lisez attentivement l'énoncé.
- Identifiez les variables nécessaires.
- Réfléchissez aux conditions à utiliser.
- Écrivez votre programme en Python.
- Testez votre programme avec plusieurs valeurs.

**Consigne :** utilisez les instructions `if`, `elif` et `else` lorsque cela est nécessaire. N'oubliez pas de récupérer les informations avec `input()` dans les exercices qui le demandent.

---

## Exercice 1 – Vérifier la majorité

Écrivez un programme qui demande à l'utilisateur de saisir son âge.

Le programme doit afficher :
- « Vous êtes majeur » si l'âge est supérieur ou égal à 18.
- « Vous êtes mineur » dans le cas contraire.

**Exemple :**

```text
Quel âge avez-vous ? 20
Vous êtes majeur.
```

## Exercice 2 – Nombre positif, négatif ou nul

Écrivez un programme qui demande un nombre à l'utilisateur.

Le programme doit déterminer si ce nombre est :
- Positif.
- Négatif.
- Nul.

**Exemple :**

```text
Entrez un nombre : -5
Le nombre est négatif.
```

## Exercice 3 – Nombre pair ou impair

Écrivez un programme qui demande un nombre entier.

Le programme doit vérifier si ce nombre est pair ou impair.

**Indice :** utilisez l'opérateur modulo `%`.

Rappel : un nombre est pair lorsque le reste de sa division par 2 est égal à 0.

## Exercice 4 – Vérifier la réussite d'un étudiant

Un étudiant est déclaré admis lorsque sa moyenne est supérieure ou égale à 10.

Écrivez un programme qui :
1. Demande le nom de l'étudiant.
2. Demande sa moyenne.
3. Vérifie son résultat.
4. Affiche son nom et son statut.

**Exemple :**

```text
Nom de l'étudiant : Amadou
Moyenne : 12.5

Étudiant : Amadou
Résultat : Admis
```

## Exercice 5 – Appréciation d'une moyenne

Dans un établissement, les appréciations sont définies ainsi :

| Moyenne | Appréciation |
|---|---|
| 16 à 20 | Très bien |
| 14 à moins de 16 | Bien |
| 12 à moins de 14 | Assez bien |
| 10 à moins de 12 | Passable |
| Moins de 10 | Ajourné |

Écrivez un programme qui demande la moyenne d'un étudiant et affiche son appréciation.

**Attention :** si la moyenne est inférieure à 0 ou supérieure à 20, affichez « Moyenne invalide ».

## Exercice 6 – Vérifier l'accès à un examen

Un étudiant peut participer à un examen s'il remplit les deux conditions suivantes :
- Sa moyenne est supérieure ou égale à 10.
- Ses frais de scolarité sont entièrement payés.

Écrivez un programme qui demande :
- La moyenne de l'étudiant.
- Si ses frais sont payés (`oui` ou `non`).

Le programme doit afficher :
- « Accès autorisé à l'examen » si les deux conditions sont remplies.
- « Accès refusé » dans le cas contraire.

**Indice :** utilisez l'opérateur `and`.

## Exercice 7 – Calculer une réduction

Un magasin propose les réductions suivantes selon le montant des achats :

| Montant des achats | Réduction |
|---|---|
| Moins de 25 000 FCFA | 0 % |
| De 25 000 à moins de 50 000 FCFA | 5 % |
| De 50 000 à moins de 100 000 FCFA | 10 % |
| 100 000 FCFA et plus | 15 % |

Écrivez un programme qui :
1. Demande le montant des achats.
2. Détermine le taux de réduction.
3. Calcule le montant de la réduction.
4. Affiche le montant final à payer.

**Exemple :**

```text
Montant des achats : 60000

Réduction : 10 %
Montant de la réduction : 6000 FCFA
Total à payer : 54000 FCFA
```

## Exercice 8 – Calculateur de frais d'inscription

Vous devez développer un programme permettant de calculer les frais d'inscription d'un nouvel étudiant.

Les frais sont répartis comme suit :

| Désignation | Montant |
|---|---:|
| Frais de dossier | 25 000 FCFA |
| Frais d'inscription | 200 000 FCFA |
| Première mensualité | 60 000 FCFA |

Le programme doit :
1. Demander le nom de l'étudiant.
2. Demander le montant dont il dispose.
3. Calculer le montant total à payer.
4. Vérifier si l'étudiant dispose de suffisamment d'argent.
5. Afficher le montant manquant ou la monnaie restante.

**Exemple :**

```text
Nom de l'étudiant : Fatou
Montant disponible : 250000

Total à payer : 285000 FCFA
Montant manquant : 35000 FCFA
Inscription non finalisée.
```

## Exercice 9 – Identifier le plus grand nombre

Écrivez un programme qui demande trois nombres à l'utilisateur.

Le programme doit déterminer et afficher le plus grand des trois nombres.

**Exemple :**

```text
Premier nombre : 15
Deuxième nombre : 8
Troisième nombre : 22

Le plus grand nombre est : 22
```

Pensez également au cas où les trois nombres seraient égaux ou deux nombres seraient égaux.

## Exercice 10 – Vérification d'identifiants

Vous devez développer un petit système de connexion.

Le programme contient les informations suivantes :

```python
identifiant_correct = "admin"
mot_de_passe_correct = "python123"
```

Demandez à l'utilisateur de saisir son identifiant et son mot de passe.

Le programme doit afficher :
- « Connexion réussie » si les deux informations sont correctes.
- « Identifiant ou mot de passe incorrect » dans le cas contraire.

**Indice :** utilisez `and`.

---

## Exercices de mise en situation

Ces exercices demandent un peu plus de réflexion. Prenez le temps de décomposer chaque problème avant de commencer à coder.

## Exercice 11 – Calcul de facture d'électricité

Une compagnie d'électricité souhaite automatiser le calcul des factures de ses clients.

Le tarif dépend de la consommation mensuelle :

| Consommation | Tarif par kWh |
|---|---:|
| De 0 à 100 kWh | 90 FCFA |
| De 101 à 200 kWh | 110 FCFA |
| Plus de 200 kWh | 125 FCFA |

Pour cet exercice, appliquez le tarif correspondant à la tranche atteinte à l'ensemble de la consommation.

Votre programme doit :
1. Demander la consommation en kWh.
2. Vérifier que la valeur est positive.
3. Déterminer le tarif applicable.
4. Calculer le montant de la facture.
5. Afficher le résultat.

**Exemple :**

```text
Consommation mensuelle : 150 kWh
Tarif appliqué : 110 FCFA/kWh
Montant à payer : 16500 FCFA
```

## Exercice 12 – Vérifier une année bissextile

Une année est bissextile :
- Si elle est divisible par 400.
- Ou si elle est divisible par 4 mais pas par 100.

Écrivez un programme qui demande une année et indique si elle est bissextile ou non.

**Exemples de tests :**
- 2024 : bissextile.
- 1900 : non bissextile.
- 2000 : bissextile.
- 2025 : non bissextile.

**Indice :** utilisez les opérateurs `%`, `and` et `or`.

## Exercice 13 – Vérification d'accès à une formation

Une école souhaite vérifier si un candidat peut accéder à une formation.

Les conditions sont les suivantes :
- Le candidat doit avoir au moins 18 ans.
- Il doit être titulaire du baccalauréat.
- Il doit avoir fourni son dossier complet.

Écrivez un programme qui demande ces trois informations et affiche :
- « Candidat accepté » si toutes les conditions sont remplies.
- « Candidat non accepté » dans le cas contraire.

## Exercice 14 – Petit distributeur de billets

Vous devez développer un programme qui simule un distributeur automatique de billets.

Le programme doit :
1. Demander le solde disponible sur le compte.
2. Demander le montant à retirer.
3. Vérifier que le montant demandé est positif.
4. Vérifier que le montant ne dépasse pas le solde disponible.
5. Vérifier que le montant est un multiple de 5 000 FCFA.
6. Afficher le nouveau solde si le retrait est accepté.

**Exemple :**

```text
Solde disponible : 100000
Montant à retirer : 25000

Retrait accepté.
Nouveau solde : 75000 FCFA
```

## Exercice 15 – Mini-projet : Gestion des résultats d'une classe

Vous êtes chargé de développer un programme permettant de gérer le résultat d'un étudiant.

Le programme doit demander :
- Le nom de l'étudiant.
- Sa note en algorithmique.
- Sa note en programmation Python.
- Sa note en bases de données.

Le programme doit ensuite :

1. Vérifier que chaque note est comprise entre 0 et 20.
2. Calculer la moyenne des trois matières.
3. Afficher la moyenne.
4. Déterminer l'appréciation selon le barème de l'exercice 5.
5. Afficher « Admis » si la moyenne est supérieure ou égale à 10, sinon « Ajourné ».

**Exemple :**

```text
Nom de l'étudiant : Mamadou
Note en algorithmique : 14
Note en Python : 16
Note en bases de données : 12

--------------------------------
Étudiant : Mamadou
Moyenne : 14.0/20
Appréciation : Bien
Résultat : Admis
--------------------------------
```

Si une note est invalide, le programme doit afficher un message d'erreur et ne pas effectuer le calcul.

---

## Défis supplémentaires

Pour ceux qui souhaitent aller plus loin :

### Défi 1 – Calculatrice simple

Créez un programme qui demande deux nombres et une opération parmi les suivantes :
- Addition (`+`)
- Soustraction (`-`)
- Multiplication (`*`)
- Division (`/`)

Le programme doit effectuer le calcul demandé.

Attention : empêchez la division par zéro et affichez un message si l'opération saisie n'est pas reconnue.

### Défi 2 – Déterminer la catégorie d'un enfant

Demandez l'âge d'un enfant et affichez sa catégorie :

- De 0 à 2 ans : Bébé.
- De 3 à 5 ans : Petite enfance.
- De 6 à 11 ans : Enfant.
- De 12 à 17 ans : Adolescent.
- 18 ans et plus : Adulte.

Prévoyez également le cas d'un âge négatif.

### Défi 3 – Simulation d'un code PIN

Développez un programme qui demande un code PIN à quatre chiffres.

Le programme doit comparer le code saisi avec le code enregistré.

- Si le code est correct, afficher « Accès autorisé ».
- Sinon, afficher « Code incorrect ».

**Pour aller plus loin :** donnez à l'utilisateur trois tentatives maximum avant de bloquer l'accès. Ce dernier défi peut être repris lorsque vous étudierez les boucles.

---

## Bilan du module

À la fin de ces travaux pratiques, vous devez être capable de :

- [ ] Utiliser `if`, `elif` et `else`.
- [ ] Construire des conditions avec les opérateurs de comparaison.
- [ ] Combiner plusieurs conditions avec `and`, `or` et `not`.
- [ ] Utiliser `input()` pour récupérer des informations.
- [ ] Convertir les saisies avec `int()` et `float()`.
- [ ] Traiter plusieurs situations dans un même programme.
- [ ] Identifier et corriger les erreurs liées aux conditions.

**Conseil :** ne cherchez pas immédiatement la solution sur Internet. Essayez d'abord de comprendre le problème, de réfléchir aux différentes situations possibles, puis de traduire votre raisonnement en Python.
