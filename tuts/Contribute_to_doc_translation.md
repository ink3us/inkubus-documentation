# Comment contribuer à la traduction


SRC : https://github.com/wearehive/project-guidelines#some-git-rules

## Cloner le repertoire existant
```
cd /path/to/your/existing/code 
git clone https://github.com/openclassmates/kikikoz
```
## Travailler à partir de la branche dev

Avant de créer ses branches de travail, on part de la branche **dev**:
```
git checkout dev
```
## Ajouter une branche pour votre traduction

Une fois sur la branche dev, vous pouvez créer votre branche spécifique
```
git branch <branch>
```
Où <branch> est le note de votre branche de traduction

## Switcher sur la nouvelle branch

```
git checkout <existing-branch>
```

Où <existing-branch> est la branche que vous venez de créer. Cela permet de définir <existing-branch> comme la branche courante, et mets à jour le répertoire de travail.

Il est également possible de créer et switcher sur une nouvelle branche en une étape avec la commande suivante:

```
git checkout -b <new-branch>
```

### Exemple concret

Par exemple, si votre tâche est de chapitre 1 de la documentation de Grav, créez une nouvelle branche grav-traduction-chapitre-1 comme suite:

```
git branch grav-traduction-chapitre-1
git checkout grav-traduction-chapitre-1
```

## Commencer à travailler sur un fichier

Pour travailler sur un nouveau fichier, vous commencez par le signaler à git avec la commande:

```
# Signaler à git qu'on désire éditer le fichier
git add <file>
```

Vous pouvez ensuite éditeur le fichier à votre guise. Si la tâche en cours demande d'éditer une deuxième fichier, vous répétez une seconde fois le processus et modifiez le deuxième fichier.

## Commit pour valider le travail réalisé

Un fois votre tâche terminée, vous pouvez visualiser les fichiers modifiés avec la commande suivante:

```
git status
```

Vérifiez que tous les fichiers modifiés font partie du prochain commit. Si ce n'est pas le cas, vous pouvez **ajouter de nouveaux fichiers** avec `git add <file>` ou en **enlever** avec `git reset HEAD <file>`.

Une fois que tous les fichiers que vous voulez ajouter au commit sont **on stage**, vous pouvez effectuer le commit avec la commande:

```
git commit -m "mon message descriptif des modifications réalisées" 
```

## Faire un git push pour envoyer sur github puis ouvrir une Pull Request

Une fois votre travail réalisé, vous ne faites pas de merge sur les branches dev ou master. Lorsque votre travail est terminé et que le dernier commit a été effectué, synchronisez votre branche avec github:

```
git push -u origin <ma-branche-specifique>
```

Une fois le code synchro avec github, ouvrir une nouvelle Pull Request.

## Ouvrir une nouvelle Pull Request sur Github

TODO

## En synthèse cela donne

```
# Start a new feature
git checkout -b new-feature dev

# Edit some files
git add <file>

# do some work on those files...

# validate you changes with a commit
git commit -m "Comment your changes on the feature"

# Again, edit some files
git add <file>

# do some work on those files...

git commit -m "Comment your changes on the feature"

# Push your code on Github
git push -u origin new-feature

# Open a Pull Request on Github to discuss the modifications and the merge
```
