### Sequencer

Le Sequencer est le brush permettant d'exécuter plusieurs brush les uns à la suite des autres. Il peut paraître un peu complexe, mais est très puissant.

Le début d'une séquence se déroule par la commande brush suivi du paramètre `brush=` déterminant le premier brush dans la séquence:

`/b sequencer brush=erode`

Les paramètres du brush seront alors proposés pour l'autocompletion avec l'ajout de deux arguments:

`normal=(normal, reverse)`: mode du brush qui sera utilisé lors du mode normal du sequencer;

`reverse=(normal, reverse)`: mode du brush qui sera utilisé lors du mode reverse du sequencer;

Remettre le pramètre `brush=` ajoute un nouveau brush à la séquence:

`/b sequencer brush=erode melt shape=sphere brush=blend`

Les paramètres du brush blend seront alors proposés avec l'ajout des paramètres `normal=` et `reverse=`

`/b sequencer brush=erode melt shape=sphere brush=blend reverse=normal shape=sphere`
