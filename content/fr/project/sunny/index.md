---
title: Sunny, le tracker solaire
summary: Conception et réalisation d'un tracker solaire, et programmation du site de présentation.
tags:
- lycee
date: "2022-01-20T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: Logo du projet Sunny réalisé par Adélaïde LOUIS
  focal_point: 
  
links :
- icon: ![Sunny](./img/logo-sunny.png)
  name: Site de présentation
  url: https://lostsh.github.io/sunny/
---

**Sunny le tracker solaire** est un projet qui est né en 2019 dans le cadre d'un projet en groupe pour valider les compétences acquises dans la spécialité _Informatique et Créations Numériques_ de Terminale S SI. Ainsi, avec deux autres collègues, Adélaïde LOUIS et Yohann VERNHES, nous avons décidé de réaliser un tracker solaire.

Notre projet s'est construit sur deux axes : d'une part la *réalisation de Sunny* et d'autre part la *construction d'un site de présentation*.

Nous avons d'abord fait des recherches sur le fonctionnement d'un tracker solaire et sur la trajectoire du soleil. Après avoir discuté sur comment construire le tracker avec nos moyens, nous avons dégagé trois méthodes de fonctionnement.

**La première méthode consiste à faire fonctionner le tracker avec des photorésistances** Le système est équipé de photorésistances. Ainsi, pour suivre les positions du soleil, une pièce projette son ombre sur une plaque équipée de photorésistances permettant de comparer les valeurs d’intensité lumineuse reçues pour savoir où se trouve l’ombre.
Pour cette méthode, nous nous sommes renseignés sur le fonctionnement des photorésistances. Nous avons ensuite construit le tracker avec du carton et programmé le système avec une Arduino Uno.

Les deux méthodes suivantes n'ont pas pu êtres réalisées physiquement.

**La deuxième méthode consiste à faire fonctionner le tracker en utilisant les équations de la trajectoire du Soleil.** On équipe ici le système  d'un GPS. Pour suivre les positions du soleil, le système s’appuie sur un algorithme qui calcule la position du soleil en fonction de son positionnement spatial et temporel. Pour mettre en oeuvre cette méthode, nous avons d'abord cherché comment calculer la trajectoire du soleil en fonction du temps puis nous avons fait des recherches approfondies pour comprendre les équations.

**La troisième méthode consiste à faire fonctionner le tracker en utilisant une caméra.** On équipe le système d'une caméra qui serait orientée vers le ciel. Pour savoir où est le soleil, il faut faire en sorte que le point le plus lumineux que la caméra voit, soit toujours au centre. 

*Le projet est présenté sur ce site : [site de présentation](https://lostsh.github.io/sunny/index.html#presentation).*
