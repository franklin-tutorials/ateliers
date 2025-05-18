
# Aide-mémoire Git

##  Configuration Initiale
```bash
git config --global user.name "Votre Nom"
git config --global user.email "votre.email@example.com"
git config --list  # Vérifier la configuration
```

---

##  Créer et Initialiser un Dépôt
```bash
git init              # Initialiser un dépôt Git local
git clone <url>       # Cloner un dépôt existant
```

---

##  Gérer les Fichiers
```bash
git status            # Vérifier l'état des fichiers
git add <fichier>     # Ajouter un fichier au staging
git add .             # Ajouter tous les fichiers
git commit -m "Message du commit"  # Enregistrer les changements
```

---

##  Gérer les Branches
```bash
git branch                      # Voir les branches locales
git branch <nom-branche>        # Créer une nouvelle branche
git checkout <nom-branche>      # Changer de branche
git switch <nom-branche>        # (Commande moderne) Changer de branche
git checkout -b <nom-branche>   # Créer et basculer sur une nouvelle branche
git switch -c <nom-branche>     # (Commande moderne) Créer et basculer
git branch -d <nom-branche>     # Supprimer une branche locale
```

---

##  Travailler avec un Dépôt Distant
```bash
git remote -v                   # Voir les dépôts distants
git push origin <branche>       # Envoyer les commits vers le dépôt distant
git pull origin <branche>       # Récupérer et fusionner les modifications
git fetch origin                # Récupérer sans fusionner
```

---

##  Voir l'Historique
```bash
git log                         # Voir l'historique des commits
git log --oneline               # Affichage simplifié
git show <commit_id>            # Voir les détails d’un commit
```

---

##  Annuler des Changements
```bash
git restore <fichier>           # Annuler les modifications d’un fichier (non commit)
git reset --hard <commit_id>    # Revenir à un état précédent (Attention : destructif)
git revert <commit_id>          # Créer un nouveau commit qui annule un précédent
```

---

## Exclure des fichiers de Git
Ignorer des fichiers : créer un fichier `.gitignore`


---

Retour à la page [Débuter avec Git](README.md).
