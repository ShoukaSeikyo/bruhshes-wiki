# ShapedBrush

Un shaped brush possède une forme lors de son utilisation. C'est à dire que la zone d'affectation peut être modifier grâce à une forme.

Exemple d'utilisation: 
```
/b voxel shape=cylinder size=2 h=10 direction=positive
/b blend shape=shpere size=5 axis=x h=3
```

## Paramètres

### - `shape=(sphere, cube, cylinder, cone, pyramid)`

Représente la forme général du brush.

La forme `sphere` est en réalité une ellipsoïde si le `x`, `y`, `z` sont différents. De même pour les autres formes, elles sont déformé en fonction des paramètres.

### - `size=(<nombre>, unset)`

Définis la taille du brush sur tous les axis.

La commande `/b <nombre>` est un allias vers `/b size=<nombre>`.

Exemple : `/b 20`

### - `h=(<nombre>, unset)`

Définis la taille du brush sur l'axis `axis` uniquement (par défaut `y`). Ce paramètre permet de faire des sphères écrasér ou des cylindre de hauteur variable.

La commande `/vh (<nombre>, unset)` change la valeur. Exemple : `/vh 20`

### - `axis=(<nombre>, unset)`

Définition de l'axis sur lequel est appliqué le `h`.

Sur les formes asymétrique (cylinder, cone, pyramid) il définis l'orientation de la forme

### - `direction=(negative, positive, both)`

Par défaut `both`. Si la forme est sur `positive` ça coupe tout ce qui est négatif relatif au centre de la forme et à `axis`. Exemple : une sphère en `direction=positive axis=y` crée un dôme. Ça peut aussi être utile pour créer des pilliers avec un cylindre en `positive`.

### - `x=(<nombre>, unset)`
### - `y=(<nombre>, unset)`
### - `z=(<nombre>, unset)`

Définition de la taille du brush sur l'axis sélectionné. Ce paramètre écrase la valeur de `size` ou `h` si il est défini.

### - `ox=(<nombre>, unset)`
### - `oy=(<nombre>, unset)`
### - `oz=(<nombre>, unset)`

(Offset X,Y,Z) Désaxement du centre sur l'axe choisis. Peut être positif ou négatif.