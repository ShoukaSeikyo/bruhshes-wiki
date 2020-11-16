# Overlay `/b overlay` 

**Ce brush est [Shaped](ShapedBrush.md)**

Adapté de VS: Le brush overlay permet de recouvrir une zone d'une couche de block.

Ce block n'as pas de shape et est forcement oval.

Exemple d'utilisation: 
```
/b overlay material=minecraft:dirt h=3 size=10
/b overlay material=minecraft:snow_layer h=1 coat size=10
/b overlay material=minecraft:waterlily h=1 coat spread=.2 spread_growth=2 spread_growth_rate=.5
```

La gunpowder applique l'effet vers le ciel et non vers le sol.

## Paramètres

### - `material=<ref. block>`

Change le block utiliser pour couvrir le terrain

### - `h=(<number>, unset)`

Change la hauteur de recouvrement du brush. `h=4` indique que les 4 blocks pleins sous la zone d'action deviennent `material`.

### - `size=(<number>, unset)`

Change la taille de la zone d'effet. 

### - `coat=(true, false)`

Inverse l'effet d'overlay pour l'appliquer par dessus le sol.

### - `spread=<float>`

Valeur comprise entre 0 et 1 (Par défaut à 1). Il spécifie le pourcentage de remplissage de l'effet overlay.

### - `spread_growth=(<number>, unset)`
### - `spread_growth_rate=<float>`

Sur chaque "block" (sur le plan x, z) modifier par l'overlay, l'effet est appliquer sur chaque face adjacente. L'effet à `spread_growth_rate` (entre 0 et 1 - taux de pourcentage) chance de s'effectuer et est répété `spread_growth` fois.
