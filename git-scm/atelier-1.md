## Atelier 1 : Création et gestion d’un dépôt Git local

## 🎯 Objectifs
- Comprendre les concepts de dépôt, staging area, commit, branches.
- Savoir utiliser les commandes de base de Git en local.


### PARTIE 1

### 1 Initialisation d’un dépôt Git

Crées un dossier `projet-demo` et puis se positionner dessus :

```bash
mkdir projet-demo && cd projet-demo
```
Initialises le dépôt git :
```bash
git init
```
Verifies l'etat des fichiers :

```bash
git status
```


---

### 2 Ajout de fichiers et premiers commits

Ajoutes un fichier ` README.md` contenant *` Mon premier dépôt Git `* : 

```bash
echo "# Mon premier dépôt Git" > README.md
```

```bash
git status
```

Ajoutes ` README.md` dans la zone de transit (staging) : 

```bash
git add README.md
```

Enregistres ` README.md` : 

```bash
git commit -m "Ajout du fichier README"
```
Affiches l'historique des commits : 

```bash
git log 
```

💡 **Question :**  
- Que signifie ce message ?

```bash
Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

```

---

### 3 Travail sur les branches

Crées une branche nommée `develop` : 

```bash
git branch develop
```

Bascules sur la branche nommée `develop` : 

```bash
git checkout develop
```

Dans `README.md` ajoutes *`Mon travail`* (sans effacer le contenu du fichier existant) : 

```bash
echo "Mon travail" >> README.md
```

Ajoutes ` README.md` dans la zone de transit (staging) : 

```bash
git add README.md
```

Enregistres ` README.md` : 

```bash
git commit -m "Ajout de mon travail dans README"
```

Visualises le contenu de `README.md` de la branche nommée `develop` : 

```bash
cat README.md
```

Bascules sur la branche nommée `main` : 

```bash
git checkout main
```

Visualises le contenu de ` README.md` de la branche nommée `main` : 

```bash
cat README.md
```

Executes la commande ci-dessous : 

```bash
git merge develop
```

Visualises de nouveau le contenu de ` README.md` de la branche nommée `main` : 

```bash
cat README.md
```

💡 **Question :**  
- Que constates-tu dans le contenu de `README.md` de la branche nommée `main` après l'execution de la commande `git merge` ?

---


### PARTIE 2

### 4 Fusionner les branches

- Crées une nouvelle branche nommée `feature-1` à partir de la branche `develop` en utilisant la commande `git switch -c feature-1`.
- Dans le `README.md` de la branche nommée `feature-1`, ajoutes le contenu *`Ajout d'une nouvelle fonctionnalité dans README`* (sans effacer le contenu du fichier existant).
- Depuis la branche `develop`, executes la commande `git merge feature-1`.
- Et pour finir executes la commande `git branch -d feature-1`

💡 **Questions :**  
- Que constates-tu dans le contenu de `README.md` de la branche nommée `develop` par rapport à `main` ? 
- À quoi sert la commande `git branch -d` ?


---

### PARTIE 3

### 5 Gestion des conflits de fusion

Simules un conflit :  
- Assures toi que le contenu de `README.md` soit identique dans les deux branches `develop` et `main`.
- Modifies le même fichier `README.md` dans `develop` et `main`.  
- Essayez de fusionner et observez le message de conflit.

Résolvez le conflit manuellement et validez avec :

```bash
git add README.md
git commit -m "Résolution du conflit"
```
---

**Atelier terminé ! Félicitations pour ton travail !**


Retour à la page [Débuter avec Git](README.md).