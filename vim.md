# VIM : QUELQUES RACCOURCIS CLAVIERS

## Commandes de base
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|i 			|Passe en mode INSERTION, là où le curseur se trouve|
|a			|Passe en mode INSERTION, à droite du curseur|
|A 			|Ajouter en fin de ligne|
|:q 			|Quitter|
|:q! 			|Quitter sans enregistrer|
|:w 			|Enregistrer le fichier|
|:w <fichier>		|Enregistre le fichier courant sous le nom <fichier>|
|:wq 			|Enregistrer et quitter|
|:x 			|Enregistrer (seulement en cas de modification) et quitter|
|:set paste 		|Passer en mode "collage"|
|CTRL+g			|Affiche une barre d'état en bas à gauche, avec le chemin du fichier et le n° de la ligne où se trouve le curseur (entre-autre)|
|:!<commande>		|Exécute une <commande> shell|
|:r !<commande>		|Récupère le résultat de la <commande> et l'insère sous la position du curseur|
|:r <fichier>		|Récupère le contenu de <fichier> et l'insère sous la position du curseur|

## Les modes
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|v			|visual, selectionne le texte caractère par caractère|
|CTRL + v 		|v-block, sélectionne du texte sur la largeur d'une colonne|
|SHIFT + v 		|v-lines, sélectionne le texte ligne par ligne|

## Se déplacer
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|h			|Déplace le curseur d'un caractère à gauche|
|j			|Déplace le curseur à la ligne du dessous|
|k			|Déplace le curseur à la ligne du dessus|
|l			|Déplace le curseur d'un caractère à droite|
|gg			|Déplace le curseur au début de la 1ère ligne du document|
|G			|Déplace le curseur au début de la dernière ligne du document|
|G<n° de ligne>		|Déplace le curseur à <n° de ligne>|
|0			|Déplace le curseur au début de la ligne|
|$			|Déplace le curseur à la fin de la ligne|
|e			|Déplace le curseur à la fin du prochain mot|
|nw			|Déplace le curseur de n mot(s) vers l'avant|
|ne			|Déplace le curseur à la fin du nième mot vers l'avant|

## Commandes d'édition
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|u 			|Annuler la dernière opération (comme le Ctrl+Z traditionnel)|
|Ctrl + r		|Rétablir la dernière opération annulée (comme le Ctrl+Y traditionnel)|
|.			|Répéter la dernière opération d'édition|
|U			|Annule tous les changements sur une ligne|
|yy			|Copier la ligne (4yy = 4 lignes)|
|dd			|Couper la ligne (4dd = 4 lignes)|
|p			|Coller après (P = insérer avant) le curseur, à la ligne suivante|
|R			|Passe en mode REMPLACEMENT. C'est comme le mode INSERTION, mais tous les caractères tapés effacent un caractère existant.|
|x			|Efface le caractère où se trouve le curseur|
|ce			|Efface à partir du cuseur et jusque la fin du mot, et passe en mode INSERTION|
|dd			|Efface la ligne complète|
|de			|Efface jusqu'à la fin du mot courant, en EXCLUANT son dernier caractère|
|dw			|Efface jusqu'au début du prochain mot, en EXCLUANT son premier caractère|
|d$			|Efface jusqu'à la fin de la ligne, en INCLUANT son dernier caractère|
|diw			|Efface le mot sous le curseur|
|exemples :||
|d6w				|Efface les 6 prochains mots|
|2dd				|Efface les 2 lignes, à compter du curseur|
|r<caractère de remplacement>	|Remplace le caractère par le <caractère de remplacement>|
|c$				|Efface jusqu'à la fin de la ligne, et passe en mode INSERTION|
|cw				|Efface jusqu'à la fin du mot, et passe en mode INSERTION|
|o				|Insère une ligne en-dessous du curseur, et passe en mode INSERTION|
|O				|Insère une ligne au-dessus du curseur, et passe en mode INSERTION|
|Shift + v			|Sélectionne la ligne/paragraphe courant|
|:1,5d				|Supprime les lignes n°1 à n°5|

## Copier/coller
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
v			Passe en mode VISUEL. Lors de la sélection de texte|
y			Copier|
p			Coller|

## Recherche / remplacement
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|/			|Recherche du texte|
|?			|Recherche dans la direction opposé|
|%			|Tapez  %  pour trouver des ), ] ou } correspondants, après avoir placé le curseur sur l'une des occurences en question|
|n			|Rechercher l'occurence suivante|
|N			|Rechercher l'occurence précédente|
|cw			|Remplacer le texte jusqu'à la fin du mot|
|ciw			|Remplacer le mot|
|C			|Remplacer jusqu'en fin de ligne|
|.			|Répéter la dernière opération d'édition|
|:s/ANCIEN/NOUVEAU	|Remplace la prochain ANCIEN par NOUVEAU, sur la ligne|
|:s/ANCIEN/NOUVEAU/g 	|Remplacer tous (g) les ANCIEN par des NOUVEAU, sur la ligne|
|:%s/ancien/nouveau/g	|Remplace toutes les occurrences dans tout le fichier|
|:%s/ancien/nouveau/gc	|Trouve toutes les occurrences dans tout le fichier avec une invite pour confirmer ou infirmer chaque substitution.|
|:#,#s/ancien/nouveau/g	|Trouve où #,# sont les numéros de lignes de la plage où la substitution doit être faite|

**EXEMPLES**  
Si vous voulez ignorer la casse uniquement pour une recherche, utilisez \c à la fin du motif à rechercher :   /test\c  <Entrée>  
(voir la leçon 6.5 de vimtutor pour activer/désactiver la sensibilité à la casse en permanence)

## Fenêtrage (split)
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|CTRL+w et s			|Diviser horizontalement|
|CTRL+w et v			|Diviser verticalement|
|CTRL+w et =			|Égaliser la taille des viewports|
|CTRL+w et w			|Passer au viewport suivant|
|CTRL+W et CTRL+<direction>	|Passer au viewport dans la direction voulu avec H, J, K et L|
|CTRL+w et n			|Ouvrir un fichier vierge dans une nouvelle fenêtre|
|CTRL+w et r			|Échange les viewports|
|CTRL+w et R			|Échange les viewports, en sens inverse|
|CTRL+w et q			|Fermer le split|

## Fenêtrage (onglets)
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|: tabnew nom_fichier	|Ouvrir le fichier nom_fichier dans un onglet|
|:tabnext 		|Aller à l'onget suivant (gt)|
|:tabprevious		|Aller à l'onglet précédebt (gT)|
|:tabclose		|Fermet l'onglet|

## Activer/désactiver une option
Taper  ":set xxx"  active l'option "xxx".
Quelques options sont :
		'ic'  'ingnorecase' pour ignorer la casse lors des recherches.
		'is'  'incsearch'   pour montrer les appariements partiels.
		'hls' 'hlsearch'    pour mettre en surbrillance les appariements.


## Ouvrir/Sauvegarder/Quitter/Changer de fichier (buffer)
| RACCOURCI | DESCRIPTION |
| :--- | :--- |
|:e <path/to/file>	|Ouvrir|
|:w			|Sauvegarder|
|:saveas <path/to/file>	|Sauvegarder sous …|
|:x, ZZ ou :wq		|Sauvegarder et quitter (:x sauvegarde seulement si nécessaire).|
|:q!			|Quitter sans sauvegarder. De même :qa! quitte même si d’autres fichiers (buffers) ont des modifications non sauvegardées.|
|:bn (resp. :bp)	|Affiche le fichier suivant (resp. précédent).|

## Répétitions en puissance
1) En mode commande, saisir le nombre de fois pour la répétition
2) i
3) Saisir du texte
4) Appuyer sur Échap autant de fois que nécessaire
5) En mode commande de nouveau, saisir un nouveau nombre de fois à répéter
6) Appuyer sur . autant de fois que nécessaire ;)

### /i\ Taper un nombre avant un mouvement le répète autant de fois

### /!\ Taper un nombre avec un opérateur le répète autant de fois


