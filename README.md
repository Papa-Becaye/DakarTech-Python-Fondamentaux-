# Cours de Python — Les fondamentaux

> **Objectif général :** apprendre progressivement les fondamentaux de Python, de la première instruction à la réalisation d'un petit projet.
>
> **Méthode :** une séance couvre un ou deux modules selon la difficulté. Chaque séance comprend des objectifs, des explications, des exemples, des exercices et un bilan.
>
> **Date de démarrage :** 27 octobre 2026  
> **Séance 1 :** Module 1 uniquement — Introduction à Python

---

## Plan général du cours

| Séance | Module(s) | Thèmes principaux | Statut |
|---|---|---|---|
| 1 | Module 1 | Introduction à Python, installation, premier programme | En cours |
| 2 | Module 2 | Variables et types de données | À faire |
| 3 | Module 3 | Entrées et sorties : `input()` et `print()` | À faire |
| 4 | Module 4 | Opérateurs et conditions | À faire |
| 5 | Module 5 | Boucles `for`, `while`, `range()`, `break`, `continue` | À faire |
| 6 | Module 6 | Listes, tuples, dictionnaires et ensembles | À faire |
| 7 | Module 7 | Fonctions, paramètres et `return` | À faire |
| 8 | Module 8 | Chaînes de caractères, fichiers et exceptions | À faire |
| 9 | Module 9 | Modules, bibliothèques, `pip` et environnements virtuels | À faire |
| 10 | Module 10 | Bonnes pratiques, débogage et organisation du code | À faire |
| 11 | Module 11 | Initiation à la programmation orientée objet | À faire |
| 12 | Module 12 | Projet final : application de gestion simple | À faire |

> Ce planning est indicatif. On peut consacrer une séance supplémentaire à un module si les exercices montrent que certaines notions doivent être retravaillées.

---

# Séance 1 — Introduction à Python

- **Date :** 27 octobre 2026
- **Durée indicative :** 45 à 90 minutes
- **Module étudié :** Module 1 — Introduction à Python
- **Niveau :** débutant

## 1. Objectifs pédagogiques

À la fin de cette séance, je dois pouvoir :

- expliquer ce qu'est Python et citer quelques utilisations ;
- distinguer un langage de programmation d'un éditeur de code ;
- vérifier si Python est installé sur mon ordinateur ;
- créer et exécuter un fichier Python ;
- utiliser `print()` pour afficher du texte et des résultats simples ;
- comprendre l'ordre d'exécution des instructions.

## 2. Qu'est-ce que Python ?

Python est un langage de programmation qui permet de donner des instructions à un ordinateur. Sa syntaxe est relativement lisible, ce qui en fait un bon choix pour débuter.

### Quelques domaines d'utilisation

- **Développement web :** création de sites, de services et d'API avec des outils comme Django ou FastAPI.
- **Automatisation :** exécution de tâches répétitives.
- **Analyse de données :** traitement et analyse de tableaux de données.
- **Intelligence artificielle :** utilisation et développement de modèles d'IA.
- **Scripts système :** traitement de fichiers et automatisation de certaines opérations.

### À retenir

Python est le langage. Un éditeur comme Visual Studio Code permet d'écrire le code. L'interpréteur Python permet d'exécuter ce code.

## 3. Préparer l'environnement de travail

Sur Windows, deux options simples sont possibles :

- **Visual Studio Code**, recommandé pour apprendre à organiser des projets.
- **Python IDLE**, fourni avec de nombreuses installations de Python et pratique pour tester de petits exemples.

Liens utiles :

- Télécharger Python : <https://www.python.org/downloads/>
- Télécharger Visual Studio Code : <https://code.visualstudio.com/>

### Vérifier l'installation

Ouvrir le terminal Windows et exécuter :

```bash
python --version
```

Si cette commande ne fonctionne pas, essayer :

```bash
py --version
```

Une version installée peut afficher un résultat de ce type :

```text
Python 3.x.x
```

Le `x` représente le numéro de version installé.

**Si aucune commande ne fonctionne :** vérifier l'installation de Python et l'option permettant de l'ajouter au `PATH`, puis fermer et rouvrir le terminal.

## 4. Créer et exécuter son premier programme

Créer un dossier de travail, par exemple `apprentissage-python`, puis créer un fichier nommé `main.py`.

Écrire le code suivant :

```python
print("Bonjour et bienvenue dans Python !")
print("Je commence mon apprentissage.")
```

Dans le terminal, se placer dans le dossier du fichier, puis exécuter :

```bash
python main.py
```

Si nécessaire, utiliser `py main.py` sous Windows.

### Résultat attendu

```text
Bonjour et bienvenue dans Python !
Je commence mon apprentissage.
```

### Explication

- `print()` est une fonction qui affiche une information.
- Les guillemets indiquent ici que leur contenu est du texte.
- Chaque appel à `print()` affiche une ligne.
- Les instructions sont exécutées dans l'ordre, de haut en bas.

## 5. Afficher du texte et effectuer un calcul

Tester ce programme :

```python
print(10)
print(5 + 3)
print("Le résultat est :", 5 + 3)
```

Résultat :

```text
10
8
Le résultat est : 8
```

Il faut distinguer ces deux instructions :

```python
print(5 + 3)
print("5 + 3")
```

La première calcule la somme et affiche `8`. La seconde affiche le texte `5 + 3`, car l'expression est entre guillemets.

## 6. Les premières erreurs à connaître

### Oublier les guillemets autour du texte

Exemple incorrect :

```python
print(Bonjour)
```

Python interprète `Bonjour` comme un nom de variable. Si cette variable n'existe pas, une erreur survient.

Exemple correct :

```python
print("Bonjour")
```

### Mal écrire le nom de la fonction

Exemple incorrect :

```python
Print("Bonjour")
```

Python distingue les majuscules et les minuscules. Il faut écrire `print`, tout en minuscules.

### Ne pas enregistrer le fichier

Après une modification, enregistrer `main.py` avant de relancer le programme pour être sûr d'exécuter la dernière version.

---

## 7. Exercices pratiques

**Consigne :** essayer de résoudre chaque exercice sans consulter les corrections.

### Exercice 1 — Comprendre `print()`

À quoi sert `print()` ?

- A. À récupérer une saisie utilisateur.
- B. À afficher une information.
- C. À créer automatiquement une variable.

**Ma réponse :** `...`

### Exercice 2 — Prévoir le résultat

Sans exécuter le code, écrire ce qui sera affiché :

```python
print(4 + 6)
print("4 + 6")
```

**Mon résultat :**

```text
...
...
```

### Exercice 3 — Personnaliser un programme

Écrire un programme qui affiche :

1. son prénom ;
2. son objectif d'apprentissage ;
3. le résultat de `12 + 8`.

**Mon code :**

```python
# Écrire ma réponse ici
```

### Exercice 4 — Corriger le code

Le programme suivant contient une erreur :

```python
Print("Je découvre Python")
```

Réécrire la ligne correctement.

**Ma correction :**

```python
# Écrire ma réponse ici
```

### Exercice 5 — Petit défi

Créer un fichier `presentation.py` qui affiche au moins quatre lignes :

- une présentation ;
- une phrase expliquant pourquoi apprendre Python ;
- un calcul simple ;
- une phrase de conclusion.

**Mon code :**

```python
# Écrire ma réponse ici
```

---

## 8. Corrections des exercices

<details>
<summary>Correction 1</summary>

**Réponse B :** `print()` permet d'afficher une information.
</details>

<details>
<summary>Correction 2</summary>

```text
10
4 + 6
```

Le premier appel calcule une addition. Le second affiche du texte.
</details>

<details>
<summary>Correction 3</summary>

Exemple :

```python
print("Je m'appelle Bécaye.")
print("Je veux apprendre les fondamentaux de Python.")
print(12 + 8)
```

Résultat :

```text
Je m'appelle Bécaye.
Je veux apprendre les fondamentaux de Python.
20
```
</details>

<details>
<summary>Correction 4</summary>

```python
print("Je découvre Python")
```

Le nom correct de la fonction est `print`, avec un `p` minuscule.
</details>

<details>
<summary>Correction 5</summary>

Exemple de solution :

```python
print("Bonjour, je découvre Python.")
print("Je veux apprendre à programmer.")
print("Le résultat de 15 + 5 est :", 15 + 5)
print("Fin de ma présentation.")
```

Plusieurs réponses sont possibles si le programme respecte les consignes.
</details>

---

## 9. Bilan de la séance

Cocher les éléments que je maîtrise :

- [ ] Je peux expliquer ce qu'est Python.
- [ ] Je peux vérifier la version de Python.
- [ ] Je sais créer un fichier `.py`.
- [ ] Je sais exécuter un programme.
- [ ] Je comprends le fonctionnement de `print()`.
- [ ] Je sais distinguer du texte d'un calcul simple.
- [ ] J'ai réalisé les exercices sans recopier directement les corrections.

### Notes personnelles

- **Ce que j'ai compris :** ...
- **Ce qui reste difficile :** ...
- **Questions à revoir :** ...
- **Temps consacré à la séance :** ...

### Critère de passage à la séance suivante

Je peux passer au module 2 lorsque je sais créer et exécuter un petit programme utilisant plusieurs instructions `print()`, et expliquer pourquoi `print(4 + 6)` et `print("4 + 6")` ne produisent pas le même résultat.

---

# Aperçu de la séance 2

## Module 2 — Variables et types de données

Les notions abordées seront :

- le rôle d'une variable ;
- les règles de nommage ;
- les types `int`, `float`, `str` et `bool` ;
- la fonction `type()` ;
- les conversions avec `int()`, `float()` et `str()` ;
- les erreurs fréquentes liées aux types.

**La séance 2 commencera par une courte révision du module 1 avant d'aborder les nouvelles notions.**

---

## Historique de progression

| Date | Séance | Modules terminés | Observations |
|---|---|---|---|
| 27/10/2026 | 1 | À valider | Introduction à Python |
| À compléter | 2 | À compléter | Variables et types de données |
