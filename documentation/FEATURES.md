# Features

We will omit most command syntax. However, a detailed overview of all commands can be found in the [official documentation](http://wiki.sk89q.com/wiki/WorldEdit).

## Region Operations

It's possible to perform a long range of region operations with World Edit.

To perform those kind of operations, the user is required to select a Cuboid area. This is done by selecting two points which will create a rectangular selecion (other shapes and formats can also be used).

Using the selected area, we can perform changes like:

* Setting Blocks
* Replacing Blocks (example below)
* Create walls
* Place overlays over a range of blocks
* Stacking (example below)
* Move a set of blocks
* Smooth an area, for example, a rough mountain
* Naturalize, make an area look more natural with grass and dirt
* Placing flora, scatter tall grass and flowers for grass or cactus for sand
* Deform regions, applying a user defined equation

**Region Selection**
```
Usage: //wand [Gives user an item that can be used to flag first position (left click) and second position (right click)]
Usage: //pos1 or //pos2 [Selects first and second positions]
```

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/cuboid.png)

### Setting/Replacing Blocks
`//replace [list-of-blocks-to-replace] [block-to-replace-with]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/replaceblocks.png)

### Stacking
`//stack [count] [direction]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/stacking.jpg)

## Clipboard

WorldEdit provides the ability to have a clipboard that allows users to copy, paste and even save an area. These cuboid areas can be saved into a file (*schematic files*) under a storage at `\plugins\WorldEdit\schematics\` and loaded at any time with a simple command. The copy-paste functionality saves the cuboid area in cache, in the user Local Session until we decide to paste it.

Some examples of clipboard operations are:

### Copy/Paste Areas
`//copy //paste [-aso]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/copypaste.png)

### Schematics
`//schematic|schem save|load [format] [filename]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/schematic.png)

## Generation

Generation tools provide us the ability to create a set of shapes (can be generated with mathematics) up to a full forest.

This section is focused in creating architectural elements, like for example a sphere or a pyramid. WorldEdit is also able to generate a forest like `/forestgen 10`:

> The command searches the area around you, controlled by the size parameter, and it will descend in elevation a bit in order to find grass or dirt (trees will only be generated on top of those two blocks), but it will not ever go up above your feet.

The generation algorithm was made clever to develop a forest according to surrouding area conditions. However, it is not possible to get 100% density (a tree in every spot) as Notch's (creator of Minecraft) tree algorithm won't permit that.

### Generate a sphere/ellipsoid
`//hsphere [block] [radius],[radius],[radius] [raised?]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/hsphere.png)

### Forest Generation
`//forestgen [size] [type] [density]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/forestgen.png)

## Utility

If we saw a lot of interesting features, it doesn't end here! Utility joins a lot of useful functions we often manually struggle for. In sum, we want to distinguish tools like:

* Draining liquids
* Filling pits
* Removing annoying mobs
* Extinguish fire
* Brushes: build from far away
* 
One of the most interesting ones is the brushes. As the name says, we cannot only paint with it but we can also generate blocks or shapes to where we are pointing to (terraforming). It also allows us to smooth rough mountains and level terrains.

### Generate spheres with a click
`//brush sphere [-h] [block] [radius]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/brushsphere.png)

### Smooth an area
`//brush smooth [-n] [size] [iterations]`

![alt-text](https://raw.githubusercontent.com/joaolrpaulo/WorldEdit/introduction/documentation/img/ingame/brushsmooth.png)
