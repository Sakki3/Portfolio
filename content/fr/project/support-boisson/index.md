---
title: Support de boisson adaptable à un fauteuil roulant
summary: Conception et réalisation d'un support de boisson pour une personne en situation de handicap.
tags:
- fab
date: "2022-01-13T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: 
  focal_point: 
  
links:
- name: Documentation publique
  url: https://projets.cohabit.fr/redmine/projects/projets-du-fablab/wiki/Support_de_boisson
---

## Contexte

L'objectif est de réaliser un support de boisson pour une personne en situation de handicap. Le support sera fixé à un fauteuil roulant et démontable. Le support ne doit cependant pas être trop haut pour pouvoir passer en dessous des tables. Il accueillera un gobelet et sera accompagné d'une paille.
Le modèle du fauteuil du demandeur possède des rails en-dessous de l’accoudoir, il est alors possible d’utiliser ces rails pour fixer le support au fauteuil.

## Description du système

Le système est composé de deux pièces : la première est bloc qui va glisser dans le rail de l'accoudoir gauche, et la seconde portera le gobelet. La seconde pièce sera encastrée dans la première grâce à un système de rail. Avec ce système de blocs, on peut envisager plusieurs "accessoires" personnalisés en changeant uniquement le deuxième bloc.
Les mesures utiles à la conception ont été prises directement sur le fauteuil du demandeur. La modélisation des pièces est faite sur le logiciel de CAO [FreeCAD](https://www.freecadweb.org/?lang=fr).

## Première version

||||
|:---:|:---:|:---:|
|![Modélisation](/portfolios/lea-jean/img/porte-gobelet.png "Modélisation du porte-gobelet")|![Modélisation](/portfolios/lea-jean/img/support-boisson-ensemble.png "Modélisation de l'ensemble")|![Modélisation](/portfolios/lea-jean/img/Rails.jpg "Modélisation du rail")|
|**Modélisation du porte-gobelet (vue isométrique)**|**Modélisation de l'ensemble (vue isométrique)**|**Modélisation du rail (vue isométrique)**|

Les premiers prototypes sont imprimés en PLA avec une imprimante 3D à filament, sans remplissage à l'intérieur pour gagner du temps sur l'impression et économiser le fil. Plusieurs rencontres ont lieu avec le demandeur pour tester les prototypes et ajuster les dimensions. Par ailleurs, les bords et les coins sont arrondis pour éviter de se blesser.

|||
|---:|:---:|
|![Prototype](/portfolios/lea-jean/img/proto2.jpg "Première version")|![Prototype](/portfolios/lea-jean/img/proto1.jpg "Première version")|
|**Première version du prototype imprimé en PLA**|

## Deuxième version

Le système de fixation entre les deux pièces est très hyperstatique et cela augmente les risques de défaut de fabrication qui compliquent l'assemblage. On remplace alors les deux rails par une seule en forme de queue d'aronde.

||
|:---:|
|![Prototype](/portfolios/lea-jean/img/proto3.jpg "Deuxième version")|
|**Deuxième version du prototype imprimé en PLA**|

La deuxième version du prototype est d'abord imprimé en plus petit (à droite sur la photo) pour vérifier l'assemblage des deux pièces, puis en taille réelle pour s'assurer des bonnes dimensions des rails. 

Le système fonctionne, cependant il y a un risque qu'il se démonte involontairement au niveau de l'accroche entre les deux blocs.

## Troisième version

On modifie le système d'assemblage entre les deux blocs.

||
|:---:|
|![Prototype](/portfolios/lea-jean/img/proto4.jpg "Troisième version")|
|**Troisième version du prototype imprimé en PLA**|

Le système fonctionne, est plus équilibré et plus solide au niveau de l'assemblage.

## Quatrième version

On modifie ici le design des pièces pour les rendre plus esthétiques.

|||||
|:---:|---:|:---:|:---:|
|![Modèle](/portfolios/lea-jean/img/supp2.png "Quatrième version")|![Modèle](/portfolios/lea-jean/img/supp3.png "Quatrième version")|![Modèle](/portfolios/lea-jean/img/supp4.png "Quatrième version")|![Modèle](/portfolios/lea-jean/img/supp1.png "Quatrième version")|
|**Modèle du bloc porte-boisson**|**Modèle du bloc rails**||**Modèle de l'ensemble du support boisson**|

On imprime ensuite les pièces avec une densité de 30%. L'impression a une durée estimée de 16h25 et consommera 155g de fil soit 52m.  Les pièces sont imprimées en noir, couleur souhaitée par le demandeur.

||||||
|:---:|:---:|:---:|:---:|:---:|
|![Pièces](/img/supp5.png "Quatrième version")|![Pièces](/img/supp6.png "Quatrième version")|![Pièces](/img/supp7.png "Quatrième version")|![Pièces](/img/supp8.png "Quatrième version")|![Pièces](/img/supp9.png "Quatrième version")|
|||**Support boisson imprimé en PLA**|||

Une réunion est organisée avec le demandeur. Le produit est validé.

|||
|---:|:---|
|![Pièces](/img/supp10.jpg "Quatrième version")|![Pièces](/img/supp11.jpg "Quatrième version")|
|**Support boisson**|**fixé au fauteuil roulant**|
