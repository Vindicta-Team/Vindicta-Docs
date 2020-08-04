---
layout: default
title: Arsenal
parent: Guide
nav_order: 8
---

# Arsenal
{: .no_toc }

The Arsenal (Jeroens Limited Arsenal&trade;) functions as a store for all your equipment.  
It has infinite capacity, and an interface for viewing, changing, loading, and saving load outs.  

## Table of contents
{: .no_toc .text-delta }

1. TOC
{:toc}

---

## Building an Arsenal

The various available Arsenal objects appear in the Storage category in the [Build UI](building).  
Currently there is no functional difference between them.  

## Interacting with an Arsenal

Note that an Arsenal is an extra function that is assigned to a standard Arma container. As such the Arsenal crate 
will have both a standard inventory (accessed as per usual), *and* an Arsenal which can be accessed 
with the scroll menu. These two things have no connection other than that they are accessed through the same crate.  

### Opening the Arsenal

This is done simply using the scroll wheel on the Arsenal crate and selecting "Arsenal".  
It will open up (it can take a few seconds to load) on a third person view of your character, with surrounding UI.  
If you can't see your character then try rotating the camera by dragging your mouse (like moving the map) in the middle of the screen. 
Sometimes the camera will start inside a wall or some other occlusion.  

### The Arsenal UI

The basic UI components in the Arsenal are:
- The Left panel: this shows the available categories of equipment you can select from. Red indicates that you do not have any item from that category equipped.   
- The Right panel: this shows available items you can transfer into the equipment you have currently selected on the Left panel. 
e.g. If you have the backpack category selected on the Left Panel *and a backpack from it equipped*, any selections you make on the Right panel 
will be loaded into our out of that backpack. If you unequip the backpack those selections will be lost.  
- The Player view: this shows your character with labels for the various categories of equipment you can select from. You can click the labels directly to switch
to that category.  

### Transferring to the Arsenal

You can transfer the entire contents of an object (crate or vehicle) inventory to the Arsenal in one go by doing the following:
1. Ensure the object is within 10m or so of the Arsenal
2. On the Arsenal create select `Inventory to Arsenal`
3. Now go to the object and choose `Select` from the scroll menu
4. All items in the inventory of the object will be transfered into the Arsenal
Note: the source crate for this operation can be the Arsenal itself! This will load the *inventory* of the Arsenal crate into
the Arsenal itself.  

### Transferring from the Arsenal

You can transfer items from the Arsenal to the inventory of an object (crate or vehicle) directly by doing the following:
1. Ensure the object is within 10m or so of the Arsenal
2. On the Arsenal crate select `Arsenal to Inventory`
3. Now go to the object and choose `Select` from the scroll menu
4. The Arsenal UI will open, and you can move items to the objects inventory as you would your own

### Merging Arsenals

Sometimes you will want to merge the contents of two Arsenals together. This can be done like so:
1. Ensure the Arsenals are within within 10m of each other
2. On the *target* Arsenal crate (the one you want all items to end up in) select `Inventory to Arsenal`
3. Now go to the *source* Arsenal crate (the one you want to take items from) and choose `Select` from the scroll menu
4. The contents of the source Arsenal will now be in the target Arsenal

### Splitting Arsenals

This is done using a combination of `Arsenal to Iventory` followed by `Inventory to Arsenal`.
