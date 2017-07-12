# Comment contribuer à la traduction


SRC : https://github.com/wearehive/project-guidelines#some-git-rules

## Cloner le repertoire existant

```
cd /path/to/your/existing/code 
git clone https://github.com/openclassmates/kikikoz
```

## Ajouter une branche

```
git branch <branch>
```

Où <branch> est le note de votre branche de traduction

## Switcher sur la nouvelle branch
```
git branch <existing-branch>
```

Où <existing-branch> est la branche que vous venez de créer. Cela permet de définir <existing-branch> comme la branche courante, et mets à jour le répertoire de travail

## Commencer à travailler sur un fichier
```
# Editer des fichier
git add <file>
git commit -m "Commencé à travailler sur une nouvelle fonctionnalité"
# Répeter
```
## Intégrer mes changement à la version Master

```
git checkout master
```

Vous renvoie à l'état du dépot avant que vous ayez commencé à déployer vos fonctionnalités. De là vous avez la possibilité d'intégrer la fonctionnalité complétée, définir une toute nouvelle branche, ou effectuer un travail sur une version stable de votre projet.

```
git merge <branch>
```

Ajoute à la branche courante, les élements de la branche <branch>

## Faire une demande de Pull

## Détruire la branche de fonctionnalité locale et distante après l'avoir integré



## En synthèse cela donne

```
# Start a new feature
git checkout -b new-feature master

# Edit some files
git add <file>
git commit -m "Start a feature"

# Edit some files
git add <file>
git commit -m "Finish a feature"

# Merge in the new-feature branch
git checkout master
git merge new-feature
git branch -d new-feature

```
