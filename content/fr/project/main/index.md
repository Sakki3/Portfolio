---
title: Main articulée
summary: Planification et mise en place du cahier des charges fonctionnel. (Projet inachevé cause COVID-19)
tags:
- gmp
date: "2022-02-10T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: 
  focal_point: 
---

## Contexte

Ce projet s'est déroulé dans le cadre des projets semestriels du département Génie Mécanique et Productique de l'IUT de Bordeaux, et évolue en lien avec le parcours robotique. 

Dû au contexte de la crise sanitaire du COVID-19, seules la planification et la mise en place du cahier des charges fonctionnel ont été réalisées. La planification a malgré tout été menée comme si 

## Présentation générale du projet

Le projet consiste à réaliser une **main articulée** dont l'objectif est de **démontrer différentes technologies de liaison utilisables pour les articulations**. 

Les articulations seront purement mécaniques mais le système peut être amélioré par la motorisation de celui-ci.

## Planification

Afin d'organiser au mieux le projet, il faut le **planifier**. Il convient alors d'établir la **liste des tâches** à réaliser afin de mener à terme le projet, en définissant leurs antécedents (et donc leur chronologie) ainsi que leur durée.

On établit ensuite un **GANTT** et un **PERT**.

## Cahier des charges

On procède à une **analyse fonctionnelle**. 

On établit une *bête à corne* qui illustre le besoin du système. 

![Bête à corne](/portfolios/lea-jean/img/bac.png "Bête à corne")

La main articulée devra :
- bouger selon les commandes de l’utilisateur via des commandes extérieures à la main, commandes mécaniques mais qui peuvent évoluer sur des commandes électriques ;
- pouvoir être montrée à un public par l’utilisateur.

Cependant, elle devra aussi s’adapter aux contraintes des éléments environnants. Étant un démonstrateur, la main sera exposée et devra donc s’adapter à un support, mais aussi à son public. En effet, les différentes technologies de liaisons devront être visibles. Par extension, elle devra aussi s’adapter à l’utilisateur, c’est-à-dire, pouvoir être utilisée par ce dernier. Enfin, elle devra s’adapter à l’environnement dans lequel elle sera exposée.

On établit ainsi les fonctions de service et les fonctions contraintes du système, qu'on représente dans un *diagramme pieuvre*.

| **Fonctions de service** | **Contraintes d’adaptation** |
| :--------------- | :--------------- |
| FS23 : Obéir aux commandes de l’utilisateur | Ca1 : S’adapter au support |
| FS34 : Montrer la main au public | Ca2 : S’adapter à l’utilisateur |
|             | Ca3 : S’adapter au public |
|             | Ca4 : S’adapter à l’environnement |

![Diagramme pieuvre](/portfolios/lea-jean/img/diag-pieuvre.png "Diagramme pieuvre")

On regroupe le **besoin fondamental**, les **fonctions services** et les **contraintes d'adaptation** dans un diagramme FAST.

![FAST](/portfolios/lea-jean/img/FAST.png "FAST")

Contraintes générales : 
- Le système doit être défini dans un format A4 ; 
- Respecter les normes de sécurité ;
- Utiliser des technologies différentes ;
- Age minimum d’utilisation : 11 ans ;
- Matériaux : utilisation de matières plastiques et d’alliages d'aluminium ;
- Énergie : énergie mécanique uniquement ; en cas d’évolution, énergie électrique : 24V max ;
- Masse : le système doit être facilement transportable.

Il est important décrire les **éléments environnants** au système.vLe projet étant un démonstrateur, il sera exposé dans un environnement sec et sera utilisé par plusieurs personnes lors des présentations.

On **caractérise** enfin les fonctions.

| **FS23 : Obéir aux commandes de l'utilisateur** | **Critères de l'action** | **Niveaux** | **Flexibilité** |
| :--------------- | :--------------- | :--------------- | :--------------- |
| Éléments environnants influents: Environnement, public, utilisateurs | Commander : Tension (fils) | A définir par des essais | Maxi |

| **FS34 : Montrer la main au public** | **Critères de l'action** | **Niveaux** | **Flexibilité** |
| :--------------- | :--------------- | :--------------- | :--------------- |
| Éléments environnants influents: Environnement, commandes, utilisateurs | Montrer : Liaisons  | 7  | Mini |
| Éléments environnants influents: Environnement, commandes, utilisateurs |Résister à l'usure : Cycles d’utilisation (tension/relâchement des fils)| 500/jour | Maxi |
