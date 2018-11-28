![Logo](__img/PowerShell_5.0_icon.png__)
# TERMINAL : SOME SHORTCUTS 
## TABS 
| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + SHIFT + T	|New tab|
|CTRL + SHIFT + W	|Close active tab|
|CTRL + PAGE UP		|Previous tab|
|CTRL + PAGE DOWN	|Next tab|

## AUTOCOMPLETE
| SHORTCUT | DESCRIPTION |
| --- | --- |
|TAB			|Complete the line if a choice is possible|
|CTRL + I		|IDEM|
|TAB + TAB		|Proposes a list of possible correspondence|

## COMMAND LINE HISTORY
| SHORTCUT | DESCRIPTION |
| --- | --- |
|history		|Historical of commands in reverse order|
|!n			|Execute the command with the number of command "n"|
|!!			|Execute the last command|
|!bla			|Execute the command starting with "bla"|

## HISTORY AND EXECUTION OF ORDERS
| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + M		|Validate the order, [ENTER]|
|FLÈCHE HAUT		|Navigate in historic, -1 line (command line more and more ancient)
|CTRL + P		|P for previous|
|FLÈCHE BAS		|Navigate in historic, +1 line (command line more and more recent)|
|CTRL + N		|N for next|

Search a command in the history :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + R		|Search in the historic|
|ALT + R		|if, in command prompt, you have modified a line recalled of historic, this shortcut puts back in state (as it is in the hstoric|

When you search in history with CTRL+r and that multiple occurences are found, press CTRL+r repeatedly to switch between them. The search is from the most recent to the oldest.

When writing a command, you can insert the first word of the previous command executeda. for that :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|ALT + .		|Recall the first word of the previous command|

## MANIPULATE THE CURSOR
| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + A		|Go to the beginning of the line|
|CTRL + E		|Go to the end of the line|
|ALT + B		|Moves back, word by word|
|ALT + F		|Moves forward, word by word|
|CTRL + B		|Moves back, character by character|
|CTRL + F		|Moves forward, character by character|
|CTRL + XX		|Alternate between the actual cursor position and the start of the command|

## MANIPULER LE TEXTE
It is possible to delete a character before or after the cursor with the shortcuts :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + D		|Delete the current character and, if the line is blank, close the terminal|
|CTRL + H		|Delete the character which is before the cursor|

These functions are also available for delete the words and the lines :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|ALT + D		|Delete the word at right of cursor, or the rest of word from cursor and towards right|
|CTRL + W		|Delete yhe word at left of cursor, or the rest of word towards left|
|CTRL + K		|Delete from cursor until the end of command|
|CTRL + U		|Delete from cursor until start of command|

Note that words or lines deleted with previous commands will be in the Bash clipboard.
This clipboard is different that the one in the desktop, with which he doesn't communicate !

When you fill the clipboard, he does not forget what he contains. Everything is kept in memory and you can choose what you want to paste. 

The shortcuts of clipboard of Bash are :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + Y		|Paste the last element into the clipboard, deleted by CTRL+U, CTRL+W ou CTRL+K|
|ALT + Y		|After using CTRL+Y, invert the text pasted with what was previously in the clipboard|

Bash also allows you to swap two letters or two words :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + T		|Invert the letter under cursor with the one that precedes it|
|ALT + T		|Same, with 2 words|

Finally, it is possible to transform the case of a word :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|ALT + U		|Convert a word in uppercase, from the cursor|
|ALT + L		|Convert a word in lowercase, from the cursor|
|ALT + C		|Capitalize a word (the first letter of word in uppercase)|

## COPY/PASTE
| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + SHIFT + C	|Copy|
|Sélectionnez le texte	|Copy|
|CTRL + SHIFT + V			|Paste|
|Clic avec la roulette de la souris	|Paste|

## CANCEL 

There are 2 shortcuts to cancel :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + /		|Undo the last action (equivalent to CTRL+Z)|
|CTRL + G		|Leave a search into historic|

## MANAGE THE PROCESSES
When a process is started in the foreground from Bash, the following shortcuts are available :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + C		|Finish the process. Do not worry, he will not suffer ;)|
|CTRL + Z		|Pause the process. Can be revived in the foreground or background with the commands "fg" or "bg". The command "jobs" list the processes in pause.|

## CLEAN AND MANAGE THE DISPLAY
It is possible to manipulate what Bash shows on the screen with these three shortcuts :

| SHORTCUT | DESCRIPTION |
| --- | --- |
|CTRL + L		|Cleans the screen to show only a command prompt blank|
|CTRL + S		|Stop the display ; very useful when a very verbose program runs|
|CTRL + Q		|Resumes the display stopped with CTRL+S|

## END OF FILE
There is a shortcut to send the EOF (End Of File) character: CTRL + D
If you send this character on a command line, this is equivalent to the exit command.

