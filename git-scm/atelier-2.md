## Atelier 2 : Création et gestion d’un dépôt Git distant avec GitLab

## 🎯 Objectifs
- Créer un compte et un dépôt sur GitLab.
- Lier un dépôt local à GitLab.
- Utiliser les commandes Git pour pousser, récupérer et collaborer sur du code.
- Comprendre les notions de clone, push, pull, remote, et merge.



### PARTIE 1

### 1 Créer un compte sur GitLab

- Rendez-vous sur [https://gitlab.com](https://gitlab.com) et inscris-toi.

### 2 Créer un nouveau dépôt (projet)

- Cliques sur **"New Project"**.
- Nommes ton projet `projet-demo-gitlab`.
- Laisses l'option "Initialize repository with a README" décochée (tu le feras en local).
- Valides en créant le projet.

---

### PARTIE 2

### 3 Lier un Dépôt Local à GitLab

- Crées un nouveau dépôt local nommé `projet-demo-gitlab`.
- Ajoutes un fichier `README.md` contenant "# Projet Démo GitLab" et réalises ton premier commit.
- Récupéres l'URL de ton dépôt GitLab (par exemple : `https://gitlab.com/ton-compte/projet-demo-gitlab.git`).
```bash
git remote add origin https://gitlab.com/ton-compte/projet-demo-gitlab.git
```
- Envoyes ton premier commit sur GitLab

```bash
git push -u origin main
```

💡 **Question :**  
- Que fait l'option `-u` dans la commande `git push` ?  

---

### PARTIE 3

### 4 Travailler avec GitLab et Git

- Clones le dépôt sur une autre répertoire
```bash
git clone https://gitlab.com/ton-compte/projet-demo-gitlab.git
```
- Crées une branche de travail `feature-readme`
- Ajoutes du contenu "Ajout d'une section de test" dans `README.md` sans effacer le contenu déjà présent puis commit avec comme description *` Ajout d'une section de test dans README`*.
- Pousses la nouvelle branche `feature-readme` sur GitLab


💡 **Question :**  
- Quelle est la différence entre `git push` et `git pull` ?

---

### PARTIE 4

### 5 Fusionner branche sur GitLab

- Allez sur l’interface GitLab, créez une **Merge Request** depuis `feature-readme` vers `main`.
- Validez la fusion.

---

### PARTIE 5

### 6 Supprimer la branche distante et locale

```bash
git push origin --delete feature-readme
```

```bash
git branch -d feature-readme
```

---

### PARTIE 6

### 7 Ajouter un fichier `.gitignore`

- Crées un fichier `.gitignore` :

```bash
echo "*.log" > .gitignore
echo "__pycache__/" >> .gitignore
git add .gitignore
git commit -m "Ajout du fichier .gitignore"
git push
```

---

**Atelier terminé ! Félicitations pour ton travail !**


Retour à la page [Débuter avec Git](README.md).