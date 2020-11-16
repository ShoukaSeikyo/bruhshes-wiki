# Bruhshes

Bruhshes est un plugin Bukkit visant à remplacer VoxelSniper (VS) avec un code plus performant et modulable.

## Lexique

*Chad*: Le joueur utilisant Bruhshes;

*ShapedBrush*: Brush ayant les paramètres de formes;

## Permissions

`bruhshes.brush` Utiliser la commande Brush.

`bruhshes.presets.global.use` Utiliser les presets globaux.

`bruhshes.presets.global.create` Créer des presets globaux.

`bruhshes.presets.perchad.use` Utiliser les presets personnels.

`bruhshes.presets.perchad.create` Créer des presets personnels.

`bruhshes.worldguard.outside` Utiliser en dehors d'un plot WorldGuard.

`bruhshes.plotsquared.outside` Utiliser en dehors d'un plot PlotSquared.

## Commandes

### Brush /brush, /b
De la même façon que VS, il est possible de modifier la taille du brush directement avec la commande. *( /b 5 )*

La différence majeure avec VS est l'autocompletion des brushes et la façon d'indiquer la forme du brush.

La plupart des brushes sont des ShapedBrush qui ont la possibilité d'avoir une forme indiquée directement dans la commande, celà permet donc de réduire drastiquement le nombre de brush qui existent dans le code, n'ayant pas à créer un brush différent pour chaque forme qui est possible.

`/b erode melt size=20 shape=sphere`

Les brushes sont donc plus modulables par le chad qui cherche à flex le terrain.

Référez-vous à la section Brush pour plus d'informations concernant chacun d'eux.

Il est aussi possible de créer des presets globaux de la même façon que la commande Brush Preset. Il suffit de remplacer le `/bp` par `/b`:

`/bp eb sequencer name=ErodeBlend brush=erode melt shape=sphere brush=blend shape=sphere reverse=normal`

### Height /brush_height, /voxel_height, /vh
Équivalent de la même commande sous VS, mais correspond au paramètre `h=` de certains brushes (ex.: overlay).

`/b overlay size=20 h=3 material=minecraft:grass`

### Brush Information /binfo, brush_toolkit, /btool, /voxel_sniper, /vs
Retourne les paramètres actuellement assignés au brush.

### Material /v, /voxel
Équivalent de la même commande sous VS, mais ne fonctionnent qu'avec certains brushes; correspond au paramètre `material=`.

`/b voxel shape=sphere size=3 material=minecraft:air`

### Reset /reset, /default, /r, /d
Rétablit les paramètres par défaut du brush selon son alias.

### Undo /undo, /u
Annule le dernier brush dans les **tâches terminées**.

Prendre note que si une tâche n'est pas terminée, elle ne peut pas être annulée avant de l'être.

### Brush Preset /brush_preset, /bp
Un des ajouts majeur de Bruhshes est la possibilité de créer des presets pour vos brushes.

Cette commande ajoute des presets **personnels** et vous permet de les utiliser par la suite.

`/bp nom_du_preset erode melt size=10 shape=sphere`

`/bp eb sequencer name=ErodeBlend brush=erode melt shape=sphere brush=blend shape=sphere reverse=normal`

## Brushes

Tous les paramètres considérés comme des booleans `true, false` peuvent être utilisé en écrivant seulement leurs noms.

`/b e melt` au lieu de `/b e melt=true`

Les brushes ont la plupart du temps deux modes: normal et reverse.

Le mode normal correspondant à un clic avec la flèche et le mode reverse correspondant à un clic avec la gunpowder.

Tous les brushes notés comme ShapedBrush auront tous les arguments noté dans [Shaped Brush](brushes/ShapedBrush.md)

### Liste de brushes

- [Voxel](brushes/voxel.md)
- [Blend](brushes/blend.md)
- [Erode](brushes/erode.md)
- [Overlay](brushes/overlay.md)
- [Sequencer](brushes/sequencer.md)