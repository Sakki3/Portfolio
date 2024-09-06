---
title: Projet défi - Distributeur de bonbons
summary: Conception et réalisation d'un distributeur de bonbons à partir d'un cahier des charges donné.
tags:
- gmp
date: "2022-01-09T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: Photo du distributeur de bonbons conçu et réalisé par Pierre CAILLAUD, Eneko CARRERE, Thomas FEUGAS, Rémi GONDOUIN, Théo GUEGAN, Lucas HUBERT et Léa JEAN
  focal_point: 
---

*Dates du projet : 21/10/2019 - 25/10/2019*

## Contexte

Le projet s'est déroulé dans le cadre de la formation **Génie Mécanique et Productique (GMP)**. Chaque groupe a quatre jours (hors temps de présentation) pour concevoir et réaliser un système suivant le cahier des charges donné en début de semaine. Le dernier jour, les groupes doivent faire une présentation de leur système à un jury.

## Cahier des charges

L'objectif est de fabriquer un **distributeur** capable de distribuer *un bonbon toutes les 4 secondes*. Celui-ci doit pouvoir *stocker* une *vingtaine d'éléments* et l'encombrement du système ne doit pas excéder *350x350x450 mm*. Le mouvement d'entrée atteint une vitesse de rotation de *30 tr/min*.

## Recherche de solution

Un brainstorming entre les membres de l'équipe est organisé durant lequel plusieurs solutions ont émergées.

### Solution 1

La première solution utilise une vis sans fin. Le bonbon est entrainé par la vis sans fin en rotation, voyageant dans son filet jusqu'à la sortie.

![Solution1](/Portfolio/img/sol1.jpg "Solution utilisant une vis sans fin")

L'avantage de ce système est qu'il est peut encombrant. En revanche, la roue sans fin est difficile à usiner et un problème de positionnement et d'orientation du bonbon peut survenir.

### Solution 2

La deuxième solution utilise une roue encochée. Cette dernière est enfermée dans un boitier. Le bonbon est pris dans l'encoche en entrée, la roue tourne et le bonbon est libéré en sortie. 

![Solution2](/Portfolio/img/sol2.jpg "Solution utilisant une roue encochée")

Le système est un peu encombrant mais est simple et l'intervalle de temps de chute des bonbons est facilement ajustable.

### Solution 3

La troisième solution pensée fonctionne avec un système de bielle manivelle. Une tige poussoir est fixé au mécanisme bielle / manivelle. Ainsi, le bonbon est libéré puis poussé par la tige dans l'orifice de sortie tout en bloquant le bonbon suivant.

![Solution3](/Portfolio/img/sol3.jpg "Solution utilisant une bielle/manivelle")

Le mécanisme est facilement réalisable mais gérer la course du poussoir peut être une difficulté.

## Conception

Il convient de réaliser le dessin d'ensemble du système et les dessins de définition des pièces, notamment de la roue encochée et des arbres de trasmissions. Un dessin du sous-ensemble de transmission est également réalisé.

![Dessin d'ensemble](/Portfolio/img/dess-ens.jpg "Dessin d'ensemble du distributeur")

## Fabrication

### Roue à encoche

**Brut : 500x500 / contre-plaqué**
- Phase 100 :  perceuse colonne / scie cloche 105 mm - Découpage d'un rond de Ø105 mm
- Phase 200 : perceuse à main / forêt Ø6mm - Perçage d'un trou centrale de Ø6 mm
- Phase 300 : scie sauteuse - Découpage de l'encoche

### Arbre 1

**Brut :  longueur 150 mm diamètre 8 mm / acier**
Usinage au tour
- Phase 100 :
    - Op 1 & 2 :  outil à charioter dresser
    - Op 3 : outil à chanfreiner
    - Op 4 : outil à tronçonner
- Phase 200 :
    - Op 1 & 2 :  outil à charioter dresser
    - Op 3 : outil à chanfreiner
    
### Assemblage

On assemble le système.

|||
| :--- | :--- |
| ![Assemblage](/Portfolio/img/assemblage1.jpg "Roue encochée et du système de transmission assemblés") | ![Assemblage](/Portfolio/img/distributeur.jpg "Distributeur assemblé") |

## Tests

Des tests sont effectués et le système est ajusté.

Des améliorations sont encore possibles :
- Pérennité : utiliser de l'aluminium
- Esthétique
- Stabilité
- Améliorer la coaxialité des perçages et utiliser des roulements pour fluidifier le système
