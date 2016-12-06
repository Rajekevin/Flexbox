# Flexbox
Introduction to flexbox CSS

Déclarer une flexbox
display : flex


flex-direction

La propriété flex-direction établit l'axe principal.

flex-direction: row | row-reverse | column | column-reverse

    row (valeur par défaut): de gauche à droite si la lecture se fait dans ce sens, de droite à gauche dans le cas inverse (1).
    row-reverse : inverse le sens
    column : comme row mais du haut vers le bas
    column-reverse : comme row-reverse mais du bas vers le haut



flex-wrap

Cette propriété définit si le container comprend une seule ligne ou plusieurs et la direction sur l'axe perpendiculaire (cross-axis), qui détermine la direction dans laquelle les nouvelles lignes seront empilées.

flex-wrap: nowrap | wrap | wrap-reverse

    nowrap : (valeur par défaut) sur une seule ligne, de gauche à droite dans un système ltr, sinon l'inverse. La ligne peut déborder de son contenant.
    wrap : multiligne, de gauche à droite dans un système ltr, sinon l'inverse. Pas de débordement, on passe à la ligne.
    wrap-reverse : multiligne, de droite à gauche dans un système ltr, sinon l'inverse.


flex-flow

Cette propriété est un raccourci des propriétés "flex-direction" et "flex-wrap" qui ensemble définissent les axes "main" et "cross" du container flex. La valeur par défaut est row nowrap.

flex-flow: <‘flex-direction’> || <‘flex-wrap’>


justify-content

La propriété justify-content définit l'alignement le long de l'axe principal. Elle permet de distribuer l'espace excédentaire lorsque tous les items flex sur une ligne sont inflexibles ou lorsqu'ils ont atteint leur taille maximale. Elle contrôle aussi l'alignement des items lorsqu'ils débordent.

justify-content: flex-start | flex-end | center | space-between | space-around

    flex-start (par défaut) : les items sont regroupés en début de ligne
    flex-end : les items sont regroupés en fin de ligne
    center : les items sont centrés le long de la ligne
    space-between : les items sont répartis sur la ligne; le premier est collé du côté start, le dernier du côté end.
    space-around : les items sont répartis sur la ligne avec un espacement égal autour de chacun.


align-items

La propriété align-items définit la façon dont les items d'une ligne sont disposés le long de l'axe "cross". On peut le voir comme la version de justify-content pour "cross axis".

align-items: flex-start | flex-end | center | baseline | stretch

    flex-start : l'item est placé au début de la ligne cross-start.
    flex-end : la marge "cross-end" de l'item est placée sur la ligne cross-end
    center : les items sont centrés sur l'axe cross
    baseline : les items sont alignés sur leur ligne de base
    stretch (par défaut) : les items sont étirés jusqu'à remplir le container (tout en respectant min-width/max-width)



align-content

La propriété align-content aligne les lignes d'un container flex à l'intérieur de l'espace où il reste de l'espace sur l'axe cross, un peu comme justify-content aligne les items sur l'axe principal.

Note : cette propriété n'a pas d'effet quand la flexbox n'a qu'une seule ligne.

align-content: flex-start | flex-end | center | space-between | space-around | stretch

    flex-start : lignes regroupées au début du container
    flex-end : lignes regroupées à la fin du container
    center : lignes regroupées au centre du container
    space-between : les lignes sont réparties, la première est collée du côté start, la dernière du côté end.
    space-around : les lignes sont réparties avec un espacement égal autour de chacune.
    stretch (par défaut) : les lignes s'étirent pour remplir tout l'espace.


order

Par défaut, les items flex sont disposés par ordre d'arrivée. Cependant, la propriété order permet de contrôler l'ordre dans lequel ils apparaissent dans le container.

order: <nombre entier>
