---
title: Ribolyser - pièce à remplacer
summary: Un professeur de l'école d'ingénieur Sciences Agro nous a demandé de refaire une pièce d'un Ribolyser, une machine d'extraction d'ADN.
tags:
- fab
date: "2022-01-13T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: Photo de la pièce en polypropylène à remplacer
  focal_point: 

links:
- name: Documentation publique
  url: https://projets.cohabit.fr/redmine/projects/projets-du-fablab/wiki/RiboLyser
---

## Contexte

Le Ribolyser est une machine d'extraction d'ADN utilisée par l'école d'ingénieur Bordeaux Sciences Agro. Cette machine doit servir sur un projet de génétique de l'Abeille Noire du Sud-Ouest qui fait l'objet d'un programme de conservation par le Conservatoire des Races d'Aquitaine qu'ils accueillent dans leurs locaux. Régulièrement des abeilles sont prélevées dans des ruchers expérimentaux pour suivre la pollution génétique par l'abeille domestique. Leur ADN doit être extrait pour qu'on puisse suivre certains gènes qui témoignent de leur lignée maternelle. Lors du processus d'extraction, la lyse mécanique doit être optimale. Cela peut être fait à la main mais s'il y a un trop grand nombre d'échantillons, c'est la tendinite assurée et/ou l'apparition de variabilité due à l'opérateur. Passer par une machine permet de lyser mécaniquement de manière standardisée. Les enseignants ont accès à des machines dernier cri mais pas les étudiants, or ce sera leur projet de standardiser l'extraction d'ADN d'abeille.

Les étudiants devront donc utiliser le FastPrep 120 Hybaid Ribolyser détenu par l'école, cependant l'une des pièces qui doit supporter beaucoup de contrainte est cassée. Un enseignant a donc demandé au Fablab Coh@bit de refaire cette pièce pour que les étudiants puissent utiliser la machine.

## Début du projet

Initialement, l'enseignant qui a contacté le Fablab voulait retirer la pièce de la machine et nous l'amener pour qu'on puisse la refaire. Or, la pièce éatant coincée, nous sommes directement allé sur place pour voir quel est le problème, discuter des solutions, et prendre des photos et des mesures.

La pièce est maintenue par trois vis. Deux d'entre elles ont été retirées avec succès mais la dernière est restée coincée. Pour cause, ces vis ont été rodées sur une partie du filetage pour qu'elles ne se dévissent pas lorsque la machine est en marche. La dernière vis est ainsi bloquée au niveau du deuxième filet.

La machine a directement été déplacée au Fablab pour pouvoir plus confortablement sortir la pièce avec les moyens nécessaires à disposition.

## Extraction de la pièce à remplacer

Lorsque nous étions dans les locaux de Bordeaux Sciences Agro, nous avons contraint la pièce pour déboulonner au-dessous et pouvoir sortir le disque auquel la pièce est fixé, pour finalement pouvoir enlerver la vis plus facilement. Le risque d'abîmer plus la pièce a été pris car cette dernière ayant une forme simple et répétitive, nous avons jugé que ce n'était pas un problème pour la modélisation de celle-ci.

![La pièce à remplacer est coincée par la vis](/portfolios/lea-jean/img/ribo1.jpg "La pièce à remplacer est coincée par la vis")

Cependant, l'opération n'a pas fonctionné car l'axe tourne simultanément. Il faut donc le maintenir lors du dé-assemblage. Les moyens sur place et le temps nous limitant, la décision a été prise d'amener la machine dans les locaux du Fablab afin de pouvoir prendre le temps d'extraire la pièce en essayant de ne pas trop endommager les vis.

Nous avons dévissé la pièce verte du carter ce qui nous a permis de sortir l'ensemble motorisé et ainsi de maintenir l'axe du rotor pour déboulonner au dessus de la pièce bleue. Nous avons ensuite détaché le ressort de la pièce bleue puis la pièce bleue de l'axe du rotor.

![Ensemble motorisé](/portfolios/lea-jean/img/ribo2.jpg "Ensemble motorisé") 
![Pièce bleue et pièce à remplacer extraites](/portfolios/lea-jean/img/ribo3.jpg "Pièce bleue et pièce à remplacer extraites (vue du dessus à gauche et du dessous à droite)")

La pièce à remplacer n'étant plus fixée à la machine et les éléments autour ayant été limités, nous avons une meilleure vision de la manière de procéder pour l'extraction de cette pièce et cette opération sera menée de manière plus confortable avec moins de risques d'endommager une pièce.

Après observation, il a été constaté que le pas de vis est endommagé. La vis a été sciée et la pièce libérée. 

![Pièce à remplacer](/portfolios/lea-jean/img/ribo4.jpg "Pièce à remplacer") 

Pour remplacer la vis endommagée, ses dimensions ont été prises. Nous avons pu ensuite en commander de nouvelles.

![Vis](/portfolios/lea-jean/img/visribo.jpg "Dessin de définition de la vis (à gauche) et nouvelles vis commandée (à droite)") 

Le diamètre de la tête de la nouvelle vis est supérieur de 1 mm au diamètre requis. Au tour conventionnel, on effectue un chariotage de la tête de vis pour l'ajuster. On chariote ensuite le filet vers le bout de la vis en utilisant un outil à tronçonner. Lors du test de la vis dans l'assemblage, il est observé qu'il faut forcer pour visser. On suppose que le problème vient du pas de vis. Ainsi, on procède à l'ajustage à l'aide d'un taraud pour la vis et d'une filière pour le trou qui l'accueillera. Un test est de nouveau effectué et l'assemblage est validé. Enfin, on colle le capuchon orange à la vis.

## Modélisation de la pièce à remplacer

Il s'agit d'une pièce qui sera très contrainte et qui doit résister en fatigue. Le département SGM de l'IUT de Bordeaux nous a ainsi fourni des bruts de polyéthylène.

![Brut](/portfolios/lea-jean/img/brutribo.jpg "Bruts fournis par le département SGM") 

Il convient de d'abord modéliser sur FreeCAD la pièce après avoir pris les mesures nécessaires sur la pièce existante.

![Modélisation](/portfolios/lea-jean/img/piece-poly-V2.png "Modélisation de la pièce à remplacer avec FreeCAD (vue du dessus à gauche et de dessous à droite)") 

La première modélisation n'a pas été faite de manière optimale. Ainsi, après avoir reçu des conseils d'une personne expérimentée, une deuxième modélisation de la pièce plus propre est entreprise puis le paramétrage de l'usinage est effectué.

## Réalisation de la pièce à remplacer

Pour commencer, de premiers tests sont entrepris afin de vérifier les trajectoires outils programmées et l'enchainement des opérations. Pour limiter les coûts et acheter uniquement la quantité de matière nécessaire, les tests ont été réalisés sur du MDF (médium).

En parallèle, on imprime la pièce avec une imprimante 3D à filament. Pour cause, pouvoir imprimer la pièce rend sa fabrication plus accessible. On teste ainsi une impression en PETG.
