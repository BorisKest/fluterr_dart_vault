Widgets its just configuration of part of layout. Widgets are a central class hierarchy in flutter. Widget is immutable description of part of a user interface. Widgets can be inflated into elements, which mange the underlaying render tree. 

The Key property controls how one widget replace another widget it the tree. If in runTime we have tow widgets whit same key then new widget will replace the old one by update the underlayer element. Otherwise, old element is remuved from the tree, the new widget is inflated into an element, and new element is inserted into the tree.

We have 3 trees 
widget tree
tree of Elements -  tracks the status of widgets 
tree of Render Objects - they responsible for how our UI will looks like 

Steps of rendering: 
1 User input 
2 Animation
3 Build
4 Layout
5 Paint
6 Composite
7 Rasterize

Render Object its visual element on the screen, it has borders, color ect. and they go to the midl level. 

Flutter responsible for di