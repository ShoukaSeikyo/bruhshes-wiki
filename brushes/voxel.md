# Voxel `/b voxel` 

**Ce brush est [Shaped](ShapedBrush.md)**

Adapté de VS: Le brush le plus basique qui soit. Place des blocs du matériel choisi sur le terrain lors d'un clic.

Exemple d'utilisation: 
```
/b voxel shape=sphere size=5 material=minecraft:stone
/b voxel shape=pyramid size=4 h=10 material=minecraft:stone
```

## Paramètres

### - `material=<ref. block>`

Modifie le type des blocks à transformé dans la zone d'action.

## Note

la commande `/v <ref. block>` permet de modifier rapidement le type du block.