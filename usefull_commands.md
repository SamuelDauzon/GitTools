# Commandes prêtes à l'emploi

## Explications des commandes

Les explications, les exemples et les précautions d'emploi de ces commandes se trouvent dans le livre Git : maitrisez la gestion de vos versions (2ème éditions).

Ce fichier contient un nombre restreint de commandes. Le livre présente d'autres commandes et leurs explications.

**Attention : certaines de ces commandes peuvent être dangeureuses. N'hésitez pas à vous référer à la documentation officielle ou les explications du livre avant de les utiliser.**

## Les commandes

### Fichier de configuration actif pour une option

```
git config --show-origin <titre_option>.<option>
```

### Editer facilement un niveau de configuration

```
git config --edit [--global|--system|--local]
```

### Afficher les informations techniques d'un commit

```
git cat-file -p <commit>
```

### Afficher les parents des commits

```
git log --pretty=raw
```

### Afficher les fichiers en conflit

```
git diff --check
```

### Afficher la liste des fichiers modifiés

```
git diff --name-only <commit1>..<commit2>
```

### Afficher l'ancêtre commun

```
git merge-base <branch1> <branch2>
```

### Vérifier une branche sur un dépôt distant

```
git ls-remote <origin> <branch>
```

### Fusionner des branches sans ancêtre commun

```
git merge --allow-unrelated-histories <branch>
```

### Afficher les fichiers modifiés par un commit

```
git show --pretty="format:" --name-only <commit>
```

### Afficher la dernière date de modification des branches

```
git for-each-ref --sort=-committerdate --format='%(refname:short) %(committerdate:short)'
```

### Lister les branches contenant un commit précis

```
git branch --contains <commit>
```

### Chercher un texte/regex dans les commits

```
git log -S "texte/regex à chercher"
```

### Lister les commits des branches

```
git show-branch
```

### Afficher les branches déjà fusionnées dans master

```
git branch --merged master
```

### Lister les branches non mergées dans master

```
git branch --no-merged master
```

### Lister les commits d'une branche non mergée à master

```
git cherry -v master <branch>
```

### Supprimer une branche distante

```
git push origin --delete branch_name
```
