# TERMINAL : QUELQUE RACCOURCIS CLAVIERS

## ONGLETS
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + MAJ + T		|Nouvel onglet|
|CTRL + MAJ + W		|Ferme l'onglet actif|
|CTRL + PAGE UP		|Onglet précédent|
|CTRL + PAGE DOWN	|Onglet suivant|

## AUTO-COMPLÉTION
| RACCOURCI | DESCRIPTION |
| --- | --- |
|TAB			|Complète la ligne si un choix est possible|
|CTRL + I		|IDEM|
|TAB + TAB		|Propose une liste de correspondance possibles|

## HISTORIQUE DES COMMANDES
| RACCOURCI | DESCRIPTION |
| --- | --- |
|history		|Historique des commandes en ordre inverse|
|!n			|Exécute la commande avec le numéro de commande "n"|
|!!			|Exécute la dernière commande|
|!bla			|Exécute la commande commençant par bla|

## MANIPULER LE CURSEUR
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + A		|Va au début de la ligne|
|CTRL + E		|Va à la fin de la ligne|
|ALT + B		|Se déplace en arrière, mot par mot|
|ALT + F		|Se déplace en avant, mot par mot|
|CTRL + B		|Se déplacer en arrière, caractère par caractère|
|CTRL + F		|Se déplacer en avant, caractère par caractère|
|CTRL + XX		|Alterner entre la position actuelle du curseur et le début de la commande|

## HISTORIQUE ET EXÉCUTION DE COMMANDES
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + M		|Retour charriot, [ENTRÉE]|
|FLÈCHE HAUT		|Naviguer dans l'historique, -1 ligne (ligne commandes de + en + ancienne)|
|CTRL + P		|(P pour previous)|
|FLÈCHE BAS		|Naviguer dans l'historique, +1 ligne (ligne de commandes de + en + récente)|
|CTRL + N		|(N pour next)|

Rechercher une commande dans l’historique :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + R		|Recherche dans l’historique|
|ALT + R		|Si, dans l’invite de commande, vous avez modifié une ligne rappelée de l’historique, ce raccourcis la remet en l’état (telle qu’elle se trouve dans l’historique).|

Lorsque vous recherchez dans l’historique avec CTRL+r et que plusieurs occurrences sont trouvées, appuyez plusieurs fois sur C-r pour passer de l’une à l’autre. La recherche se fait de la commande la plus récente à la plus ancienne.

Lors de l’écriture d’une commande, vous pouvez insérer le premier mot de la précédente commande exécutée. Pour cela :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|ALT + .		|Rappelle le premier mot de la précédente commande.|

## MANIPULER LE TEXTE
Il est possible de supprimer un caractère avant ou après le curseur avec les raccourcis :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + D		|Supprime le caractère courant, et si la ligne est vide, ferme la console|
|CTRL + H		|Supprimer le caractère qui se trouve avant le curseur.|

Ces fonctions sont également disponibles pour supprimer les mots et les lignes :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|ALT + D		|Supprime le mot à droite du curseur, ou le reste du mot à partir du curseur et vers la droite|
|CTRL + W		|Supprime le mot à gauche du curseur,  ou le reste du mot à partir du curseur et vers la gauche|
|CTRL + K		|Supprimer du curseur jusqu’à la fin de la commande|
|CTRL + U		|Supprimer du curseur jusqu’au début de la commande|

À noter que les mots ou lignes supprimés avec les commandes précédentes se retrouveront dans le presse‐papiers de Bash.
Ce presse‐papiers est différent de celui du bureau, avec lequel il ne communique pas !
Il offre toutefois la fonction de Kill‐ring, comme Emacs : lorsque vous remplissez le presse‐papiers, ce dernier n’oublie pas ce qu’il contient. Tout est gardé en mémoire et vous pouvez choisir ce que vous voulez « coller ».

Les raccourcis du presse‐papiers de Bash sont :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + Y		|« colle » le dernier élément présent dans le presse‐papiers, supprimé par CTRL+U, CTRL+W ou CTRL+K|
|ALT + Y		|Après avoir utilisé CTRL+Y, intervertit le texte collé avec ce qui se trouvait précédemment dans le presse‐papiers|

Bash permet également d’intervertir deux lettres ou deux mots :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + T		|Intervertit la lettre sous le curseur avec celle qui la précède|
|ALT + T		|Pareil, avec deux mots|

Enfin, il est possible de transformer la casse d’un mot :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|ALT + U		|convertit un mot en majuscules, à partir du curseur|
|ALT + L		|Convertit un mot en minuscules, à partir du curseur|
|ALT + C		|Capitalise un mot (la 1ère lettre d'un mot en majuscule)|

|CTRL + MAJ + C		|Copier|
|Sélectionnez le texte	|Copier|

|CTRL + MAJ + V		|Coller|
|Clic avec la roulette de la souris	|Coller|

## ANNULER
Il existe deux raccourcis pour annuler :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + /		|Annule la dernière action (équivalent de CTRL+Z)|
|CTRL + G		|Quitte une recherche dans l’historique.|

## GÉRER LES PROCESSUS
Quand un processus est lancé en premier plan depuis Bash, les raccourcis suivants sont disponibles :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + C		|Terminer le processus. Ne vous inquiétez pas, il ne souffrira pas ;)|
|CTRL + Z		|Mettre en pause le processus. Peut être relancé en premier plan ou en arrière‐plan avec les commandes fg ou bg. La commande jobs liste les processus en pause.|

À noter que lors de l’écriture d’une commande, CTRL+C fait sauter le curseur sur une nouvelle ligne de commande vide.

## NETTOYER ET GÉRER L'AFFICHAGE
Il est possible de manipuler ce que montre Bash à l’écran avec ces trois raccourcis :
| RACCOURCI | DESCRIPTION |
| --- | --- |
|CTRL + L		|Nettoie l’écran, pour ne montrer qu’une invite de commande vide ; similaire à la commande clear|
|CTRL + S		|Stoppe l’affichage ; très utile quand un programme très verbeux s’exécute|
|CTRL + Q		|Reprend l’affichage stoppé avec CTRL+S|

## END OF FILE
Il existe un raccourci pour envoyer le caractère EOF (End Of File) : CTRL + D
Si l’on envoie ce caractère sur une ligne de commande, cela équivaut à la commande exit

