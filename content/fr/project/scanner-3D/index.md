---
title: Scanner 3D
summary: Réalisation d'un système permettant de faire de la photogrammétrie.
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
  url: https://projets.cohabit.fr/redmine/projects/projets-du-fablab/wiki/Scanner_3D
---

### Description

A partir des pièces d'un scanner 3D déjà réalisé auparavant, on réalise un système permettant de prendre plusieurs photos de manière régulière et à la même distance d'un objet. A terme, avec un logiciel, on va pouvoir construire le modèle 3D de l'objet à partir de ces photos.

J’ai décidé de garder la plaque tournante du système d'origine, mais aussi de concevoir un nouveau support pour l'appareil photo et puis de programmer l’Arduino de manière à ce que la plaque tourne d'un certain incrément toutes les tant de secondes, la photo sera prise pendant ce laps de temps (par exemple, la plaque va tourner de 15° toutes les 10 secondes).

### Réalisation

Pour commencer, j’ai démonté le scanner 3D, puis modélisé sur FreeCAD le support de l'appareil photo.
Le support était au départ composé d'un corps à imprimer, d'une plaque pour supporter l'appareil photo, qui serait fixée au corps grâce à des chevilles en bois, et de deux tubes pour stabiliser la plaque aux extrémités. Après réflexion, j’ai décidé de ne mettre qu’un seul tube car suffisant. Ce dernier serait renforcé par un pied.

J’ai imprimé le corps en PLA et découpé à la découpe laser la plaque de MDF 10 mm. J’ai ensuite percé les trous qui permettront de fixer la plaque au corps avec une perceuse à colonne. Le trou traversant au milieu de la plaque va permettre de fixer l'appareil photo à plaque. Il a été placé par rapport à la position du trou déjà présent en-dessous de l'appareil photo. J’ai ensuite scié un tube de métal de diamètre 8 mm.

||||
|:---:|:---:|:---:|
|![Support](/Portfolio/img/piece1.jpg "Corps imprimé en PLA")|![Support](/Portfolio/img/piece2.jpg "Corps imprimé en PLA")|![Support](/Portfolio/img/plaque2.jpg "Plaque support en MDF")|
|**Corps imprimé en PLA**|**Corps imprimé en PLA**|**Plaque support en MDF**|

Il y a un décalage de hauteur d'environ 6-7 mm entre l'appareil photo et la plaque support, donc pour qu'il soit parallèle à cette dernière, j’ai découpé de petites cales (dessinées sur Inkscape) de 3 mm que j’ai collées ensemble. La cale a ensuite été collée sur la plaque support.

Pour garder le tube droit, j’ai modélisé et imprimé un pied. Puis j’ai modélisé et imprimé une pièce qui s'encastre dans le tube et la plaque support pour assurer un maintien entre les deux pièces mais pour également garder l'ensemble démontable.

|||
|:---:|:---:|
|![Support](/Portfolio/img/piece-scanner3d.jpg "Pièce qui s'encastre dans le tube")|![Support](/Portfolio/img/pied.jpg "Pied support assemblé")|
|**Pièce qui s'encastre dans le tube**|**Pied support assemblé**|

Après avoir assemblé les pièces du support caméra ensemble, j’ai ensuite assemblé ce dernier avec la plaque tournante.

||||
|:---:|:---:|:---:|
|![Support](/Portfolio/img/support2.jpg "Ensemble plaque tournante/support assemblés")|![Support](/Portfolio/img/scanner.jpg "Ensemble plaque tournante/support assemblés")|![Support](/Portfolio/img/support3.jpg "Ensemble plaque tournante/support assemblés")|
|**Ensemble plaque tournante/support assemblés**|**Ensemble plaque tournante/support assemblés**|**Ensemble plaque tournante/support assemblés**|
