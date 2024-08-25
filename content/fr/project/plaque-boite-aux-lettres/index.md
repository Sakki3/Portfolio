---
title: Chaîne numérique d’une plaque de boîte aux lettres
summary: Conception d'une pièce exemple, réalisation à la fraiseuse numérique Charly Robot, et rédaction de la procédure.
tags:
- fab
date: "2021-10-01T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: 
  focal_point: 
  
links:
- name: Documentation publique
  url: https://projets.cohabit.fr/redmine/projects/documentation-machines/wiki/Exemple_d'un_processus_complet
---

L’objectif du projet est, d’une part, de construire la chaîne numérique d’une pièce usinée, et d’autre part d’être capable, pour le Fablab, de faire de la CFAO sans passer par le logiciel du Charly Robot.

La pièce souhaitée est une plaque gravée pour boîtes aux lettres aux dimensions standards 100x25x3 mm (l’épaisseur correspond à l’épaisseur de la plaque utilisée) et percée aux quatre coins. On y grave dessus un nom et un petit logo. On utilise par ailleurs une plaque en Dibond d'épaisseur 3 mm.

Il convient de d’abord modéliser la pièce sur FreeCAD, puis avec le module path de FreeCAD, de construire les trajectoires outils et fixé les paramètres d’usinage pour pouvoir ensuite exporter le [G-code](https://en.wikipedia.org/wiki/G-code) généré par le logiciel. Pour que cela fonctionne, il faut préalablement télécharger le post-processeur du Charly Robot et le ranger dans un dossier du logiciel pour que le fichier puisse être lu par celui-ci [(comment installer le post-process du Charly Robot)](https://projets.cohabit.fr/redmine/projects/documentation-machines/wiki/Charly_Robot_2U#section-10). Une fois les fichiers contenant le code ISO générés, il sont chargés dans le logiciel de pilotage du Charly Robot. Après avoir fixé les paramètres nécessaires, on lance l’usinage. J’ai fait plusieurs essais pour trouver les bons paramètres d’usinage. Après avoir eu un résultat satisfaisant, d'autres essais ont été faits avec d’autres noms et d’autres dessins.

En parallèle, une notice est rédigée, contenant chaque étape du processus de la CAO à la fabrication. Un tuto vidéo de la CFAO pour compléter la notice écrite.

