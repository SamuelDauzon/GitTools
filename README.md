# GitTools

## Ce dépôt contient des outils propres à une utilisation de Git.

### Les alias

Pour configurer les alias, il faut : 

- Connaitre le fichier de configuration (Voir plus bas)
- Il faut ensuite copier/coller le contenu du fichier alias.txt dans votre fichier de configuration (global pour une configuration au niveau utilisateur). Si une section `[alias]` existe déjà, alors il faut intégrer les nouveaux alias à ceux existants.


## Fichiers de configuration

Pour obtenir la liste des fichiers de configuration de Git selon le niveau (local, global, system), il est possible de définir un alias dans chacun des fichiers. Cet alias, est un alias qui va donner la liste des éléments de configuration avec leur emplacement.

```
git config --local alias.getconfig "config --list --show-origin"
git config --global alias.getconfig "config --list --show-origin"
git config --system alias.getconfig "config --list --show-origin"
```

Une fois ces alias définis, il est possible d'utiliser l'alias avec un `grep` de façon à obtenir les chemins des différents fichiers de configuration.

```
git getconfig | grep getconfig
```
