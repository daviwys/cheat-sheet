# CHEAT SHEET SUR GIT

## Configurer Git

Après avoir installer Git, configurer son nom et son e-mail, **dans cette ordre** :
```
$ git config --global user.name "MonPrénom MonNom"
$ git config --global user.email "Mon E-mail"
```

À partir de maintenant mes "commit" indiqueront par qui (et son e-mail) ils ont été fait.

## Initialiser un projet
Commencer par se placer dans le dossier du projet et puis faire ``` $ git init ```  
Ce qui va créer un dossier caché (.git) avec tout ce dont GIT a besoin pour gérer le projet.

## Rejoindre un projet existant
```
$ git clone <URL du dépôt> 		<= Télécharge un projet complet et son historique de versions
$ git remote add <ma branche> git@github.com:<user>/<nom du projet>.git	<= Ici, on ajoute une connexion vers le "remote"
```
## Travailler avec Git
Définition d'un "add" => mise à l'index  
À chaque modification/ajout/suppression de code et/ou fichier/dossier, il faudra faire un "add" et un "commit".
```
$ git add page.html style.css			<= ici 2 fichiers d'un coup ;)
$ git commit -m "Mon commentaire"		<= Enregistre un instantané de fichier(s) de façon permanente dans l'historique des versions
$ git status 					<= Liste tous les nouveaux fichiers ainsi que ceux qui ont étés modifiés à "commiter"
$ git diff					<= Affiche tous les changements depuis le dernier "git add"
$ git diff <fichier>				<= Affiche les changements d'1 fichier en particulier (ici <fichier>) depuis le dernier "git add"
$ git reset <fichier>				<= Enlève le fichier de l'index, mais conserve son contenu !
$ git show					<= Affiche les modifications de métadonnées et de contenu inclues lors du dernier commit
```
* Sur un dépôt distant
```
$ git remote					<= Liste les serveurs distants que vous avez enregistrés
$ git remote -v					<= Affiche l’URL que Git a stockée pour chaque nom court
$ git remote show <nom distant>			<= Affiche les infos sur un dépôt distant
$ git ls-remote					<= Liste les empreintes de toutes les branches
```
* Apporter des changements au projet
```
$ git rm <fichier>				<= Supprime le fichier du répertoire de travail & met à jour l'index
$ git rm --cached <fichier>			<= Supprime le fichier du système de suivi de version mais le préserve localement
$ git mv <fichier> <fichier_nouveau_nom>	<= Renomme le fichier et prépare le changement pour un commit
```
## Annuler un "add"
```
$ git reset <fichier>
```
## Annuler un "commit"
```
$ git reset HEAD 			<= Annule le dernier commit
$ git reset HEAD^			<= Annule l'avant dernier commit
$ git reset d6d98923868578a7f38dea79833b56d0326fcba1		<= Annule un commit dont l'empreinte est "d6..."
$ git reset d6d98923			<= Version courte de la précédente ;)
```
## Basculer/switcher vers un commit ou une branche
```
$ git checkout <nom de la branche>
$ git checkout <empreinte du commit>
```
## Lister les commits
Affche les x derniers commits : ``` $ git log -n x ```

## Refaire des commits
```
$ git reset <commit>			<= Annule tous les commits après <commit> en conservant les modifications
$ git reset --hard <commit>		<= Supprime tout l'historique et les modifications effectuées après le <commit> spécifié
```
## Les branches
### Créer une branche
* Avec 2 lignes : créer et basculer sur la nouvelle branche
```
$ git branch <nom de ma nouvelle branche>
$ git checkout <nom de ma nouvelle branche>
```
* Avec 1 seule ligne : créer et basculer
```
$ git checkout -b <nom de ma nouvelle branche>
```
### Supprimer une branche
* Si la branche est local et n'est pas créée sur le repo distant
```
$ git branch -d <nom de la branche locale>
```
* Si la branche est présente sur le repo distant
```
$ git push origin --delete <nom de la branche distante>
```
### Lister les branches
```
$ git branch		<= local
$ git branch -a		<= local + distant
```
### Vérifier l'historique des versions
```
$ git diff <première_branche> ... <deuxième_branche>	<= Montre les différences de contenu entre 2 branches
$ git diff show <commit>		<= Montre les modifications des métadonnées et de contenu inclues dans le commit spécifié
```
### Fusionner les branches
```
$ git merge <nomde la branche>	<= Combine/fusionne dans la branche courante l'historique de la branche spécifiée
```
**Pour faire  ce qui suit, il faut avoir créé un nouveau repository sur github et avoir configuré son compte avec sa clé SSH !!**

### Synchroniser les changements
```
$ git fetch <nom du dépôt>			<= Récupère tout l'historique du dépôt nommé
$ git merge <nom du dépôt>/<branche>		<= Fusionne la branche du dépôt dans la branche locale courante
$ git push <alias> <branche>			<= Envoie tous les commits de la branche locale vers GitHub
$ git pull					<= Récupère tout l'historique du dépôt nommé et incorpore les modifications

$ git push -u origin <ma branche>		<= Ici, on met à jour le "remote" en poussant la branche <ma branche>
```
### Envoyer un projet vers le gestionnaire de projets (Github)
S'assurer qu'on soit enregistré avant ;)  
Envoyer ses commits vers le dépôt distant : ``` $ git push -u origin <nomde la branche> ```

### Récupérer un projet
Mettre à jour le dépôt local : ``` $ git pull	<= On récupère que les infos des modifications ! ```

## INFOS COMPLÉMENTAIRES
### git pull ou git fetch ?  
Les commandes git pull et git fetch sont toutes les deux utilisées pour mettre à jour un répertoire de travail local avec les données d'un repository distant.  
Elles n'ont cependant pas le même fonctionnement.  

La commande **git fetch** va récupérer toutes les données des commits effectués sur la branche courante qui n'existent pas encore dans votre version en local. Ces données seront stockées dans le répertoire de travail local mais ne seront pas fusionnées avec votre branche locale. Si vous souhaitez fusionner ces données pour que votre branche soit à jour, vous devez utiliser ensuite la commande git merge.

La commande **git pull** est en fait la commande qui regroupe les commandes git fetch suivie de git merge. Cette commande télécharge les données des commits qui n'ont pas encore été récupérées dans votre branche locale puis fusionne ensuite ces données.

Le choix de la commande à utiliser dépend de la façon dont vous souhaitez travailler. La commande git pull automatise la mise à jour des données mais peut entraîner de nombreux conflits si vous avez modifié beaucoup de fichiers. Utiliser la commande git fetch permet de garder son répertoire de travail à jour et de contrôler le moment où l'on souhaite fusionner les données.

### rebase  
La commande rebase remplace la base d'une branche par une nouvelle.  
Lors de la création d'une branche, sa base est celle du master à instant T. Lors d'un rebase, sa base est remplacer par celle du master à un instant T + 1.  
Pourquoi ? Parce que à "l'instant T+1" la base master à changé ! Une branche (ou plus) autre(s) que la mienne a été mergé sur master.  
Ce qui permet d'actualiser ma branche avec les modifications apportées par les autres sur la branche master.
