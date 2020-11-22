# Blend `/b blend` 

**Ce brush est [Shaped](ShapedBrush.md)**

Adapté de VS: Brush icônique, il permet de mixer les blocs pour rendre le terrain plus homogène.

Exemple d'utilisation: 
```
/b blend shape=shpere size=5 liquid 
/b blend shape=cube size=5 air
```

## Paramètres

### - `air=(true, false)`

Permet d'affecter les blocs d'air dans la zone de blend.

### - `liquid=(true, false)`

Permet d'affecter les blocs liquides dans la zone de blend.

## Note

Tous les paramètres considérés comme des booleans `true, false` peuvent être utilisé en écrivant seulement leurs noms.

`/b e melt` au lieu de `/b e melt=true`