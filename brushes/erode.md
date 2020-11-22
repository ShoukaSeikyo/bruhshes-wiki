# Erode `/b erode` 

**Ce brush est [Shaped](ShapedBrush.md)**

Adapté de VS: Ce brush permet de faire des actions de suppression / additions de blocks répété.

Exemple d'utilisation: 
```
/b erode shape=sphere melt
/b erode shape=cube ef=3 ec=2 ff=6 fc=0 
```

## Explication

Le brush va déterminer sur chaque bloc de la zone d'action si il doit être supprimer ou ajouter le block. 

Il démare par la phase de suppression. Si le cube est entouré de `ef` cube vide, alors il est supprimer. Il répète l'action `ec` fois. Puis passe à la phase d'ajout. 

Si le cube vide est entouré de `ff` cube remplis, alors il est remplis du bloc le plus commun autour. Il répète l'action d'ajout `fc` fois

La gunpowder inverse l'effet de fill et d'erode. `ef` est inversé avec `ff` et `ec` est inversé avec `fc`

## Paramètres

### - `ef=(<number>, unset)` (erode faces)
### - `ff=(<number>, unset)` (fill faces)

Indique le nombre de faces sur le cube pour qu'il soit affecté par la suppression (erode) ou l'ajout (fill). 

Si négatif, prend la valeur de manière aléatoire entre 1 et la valeur inversé + 1. (exemple : `ef=-3`; Valeur aléatoire entre 1 et 4 )

Un cube ne peux pas avoir plus de 6 faces donc c'est limité à [-5; +6]

### - `ec=(<number>, unset)` (erode count)
### - `fc=(<number>, unset)` (fill count)

Nombre de fois où l'action de suppression (erode) ou d'ajout (fill) est effectuer.

Exemple `ec=3` indique d'effectuer 3 fois l'action de suppression dans la zone.

## Presets

Les presets sont sous la forme d'arguments booleen dans la commande. `melt=(true, false)`

Exemple `/b erode melt`. 

| Preset | effet |
| :- | :- |
| `melt` | `ef=2 ec=1 ff=5 fc=1` |
| `fill` | `ef=5 ec=1 ff=2 fc=1` |
| `lift` | `ef=6 ec=0 ff=1 fc=1` |
| `dig` | `ef=1 ec=1 ff=6 fc=0` |
| `smooth` | `ef=3 ec=1 ff=3 fc=1` |
| `floatclean` | `ef=6 ec=1 ff=6 fc=1` |
| `random_melt` | `ef=-2 ec=-5 ff=-5 fc=-3` |
| `random_lift` | `ef=-5 ec=-3 ff=-2 fc=-5` |

## Note

Tous les paramètres considérés comme des booleans `true, false` peuvent être utilisé en écrivant seulement leurs noms.

Exemple : `/b e melt` au lieu de `/b e melt=true`