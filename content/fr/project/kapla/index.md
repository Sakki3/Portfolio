---
title: Construction d'une structure de Kapla
summary: Programmation de dobots avec conception et fabrication d'un support et d'une structure motorisé pour modifier l'orientation des Kaplas.
tags:
- rob
- gmp
date: "2022-02-08T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: 

image:
  caption: 
  focal_point: 
---

## Cahier des charges

Le projet s'est développé dans le cadre du semestre 4 du parcours robotique de l'IUT de Bordeaux, site de Gradignan. L'objectif est, à partir d’un tableau recensant les coordonnées (base, position, orientation) des Kapla, de réaliser une structure avec ces mêmes Kapla.

Le matériel a disposition comprend :
- 1 convoyeur,
- 2 dobots Magician (robots 4 axes),
- des [Kapla](https://www.kapla.com/fr/) de dimensions 25x20x70 mm,
- 1 caméra Intel D435i RealSense Depth,
- 1 raspberry pi,
- et divers composants comme des servomoteurs Dynamixel MX-12W, etc...

Le cycle à suivre est celui-ci : 
1. Prise d'un Kapla dans le magasin par le dobot 1
2. Dépose sur le convoyeur pour transfert vers le dobot 2
3. Reconnaissance du Kapla
4. Prise du Kapla par le dobot 2
5. Réalisation de la structure

L'effecteur des dobots est au choix : une pince pneumatique ou une ventouse.

## Planification

Pour une organisation optimale, une planification du projet est nécessaire. Il faut pour cela identifier les différentes tâches à réaliser et leur chronologie, les répartir entre les membres de l'équipe, et les répartir dans le temps de manière à respecter les jalons. Il convient alors d'établir un GANTT.

## Identification des problématiques et recherche de solutions

### Problématique 1 : l'orientation des Kapla

Dans le magasin, les Kapla ont tous la même orientation, et il faut que le Kapla puisse prendre n'importe quelle orientation suivant les besoins de la structure finale. Cependant, l’effecteur du dobot ne peux pas effectuer de rotations suivant x et y, toutes les orientations ne sont donc pas possibles. 

#### Recherche de solutions

Plusieurs solutions ont alors émergées. La première est de faire tomber le Kapla en fin de convoyeur dans une boîte avec une pente. En chutant le long de la pente, le kapla se retourne. L’inconvénient est que le Kapla peut se coincer s’il ne tombe pas directement dans la bonne position. Cette idée n’est donc pas la plus appropriée. Pour passer outre ce problème, nous avons réfléchi à une solution semblable mais plus "sûre". Nous avons donc conçu une solution motorisée en forme de “L” permettant de retourner le Kapla en activant un moteur. 

#### Choix de solution

Nous optons ainsi de développer la structure en “L” pour le système.

### Problématique 2 : détection du Kapla

Pour que le système fonctionne, les dobots doivent pouvoir trouver les Kapla pour les saisir.

#### Recherche de solutions

Nous avons donc pensé ici à trois solutions.
La première est de reposer le transport des Kapla sur l’exactitude de répétition de mouvements des robots et du convoyeur dans le but de ne pas utiliser de capteur de détection, et de tester notre convoyeur et nos dobots de manière à ce que les Kaplas puissent être posés toujours aux mêmes endroits sur le convoyeur par le dobot 1 et récupéré toujours au même endroit par le dobot 2. Or cette solution est hasardeuse. 
La deuxième est d’utiliser un capteur de présence laser pour retourner l’information de la présence du Kapla en bout de convoyeur. Avec ce système, la récupéreration du Kapla par le dobot 2 se fait au même endroit.
La troisième est d’utiliser une caméra et une intelligence artificielle de reconnaissance d’image et de détection de centre de gravité. En ayant le centre de gravité, nous pouvons déterminer précisément le point où le dobot 2 doit saisir le Kapla. L’avantage principal de ce système est de pouvoir déterminer la position du Kapla tant qu’il est dans le champ de vision de la caméra, et permet de corriger des erreurs de rotation au niveau de l’axe Z.

#### Choix de solution

Le choix s'est d'abord porté sur la troisième solution, soit une détection par caméra, solution qui par manque de temps n’as pas pu aboutir. Nous avons donc finalement opté pour le capteur de présence.

### Problématique 3 : lecture de fichier

Les Kaplas ne sont pas préalablement triés dans le fichier json fourni. La problématique qui se présente ici est donc l'ordre de pose des Kapla qui nous est inconnu.

#### Choix de solution

Il convient alors de réaliser un code de tri qui, après importation du fichier
json, renvoie le fichier dans l'ordre de dépose sur la zone de charge.

### Problématique 4 : choix de l'effecteur

Le choix nous est donné entre une ventouse ou une pince pneumatique comme effecteur des dobots. Ce choix influe sur la prise des Kapla. Ainsi, l'effecteur utilisé ici est une ventouse. 

## Modélisation et réalisation de l'ensemble du système

### Structure en "L"

Dans le but de pouvoir changer l'orientation des Kapla suivant les besoin de la structure en Kapla finale, il convient de concevoir un système. Le système conçu ici est une structure en “L”. Ce nom lui vient de la forme principale de la forme de la structure qui vue de profil ressemble à un “L”. 

|||
|:---:|:---:|
|![Dessin d'ensemble](/Portfolio/img/dess-ens-l.png "Dessin d'ensemble de la structure en L")|![Modélisation de l'ensemble](/Portfolio/img/L.png "Modélisation 3D de la structure en L sur OnShape")|
|**Dessin d'ensemble de la structure en "L"**|**Modélisation 3D de la structure en "L" sur OnShape**|

Le principe de sa structure est relativement simple. Un servomoteur Dynamixel MX-12W, commandé en angle, bascule de 90° lorsqu'on le lui demande. Le dobot 2 saisit le Kapla sur le convoyeur et le positionne à l’intérieur du “L”. Ainsi, lorsque le Kapla est allongé, nous pouvons choisir si nous voulons le positionner au sol, en longueur ou en largeur. Le "L" dispose également d’une encoche et d’un côté plus long que l’autre pour pouvoir positionner le Kapla debout. Ainsi, après avoir saisi le Kapla sur le convoyeur, la ventouse réalise une rotation suivant l’axe z pour pouvoir positionner le Kapla dans la petite encoche.

![Structure en L](/Portfolio/img/structure-l.jpg "Structure en L fabriquée")

Le système est d'abord modélisé en 3D et assemblé sur le logiciel de CAO en ligne [*OnShape*](https://www.onshape.com/en/). Ensuite, le "L" et sa fixation au moteur sont imprimésen PLA avec des imprimantes 3D à filament. On utilise une découpeuse laser pour réaliser le socle en PMMA et on scie une tige en métal qui fixera le "L" à la fixation. Enfin, on assemble le tout : les pièce du socle sont emboités, la fixation est vissée au moteur et le moteur est vissé au socle, la tige s'insert dans la fixation et le "L".

### Support de la caméra

Dans le cas de la détection de Kapla par caméra, un support pour fixer cette dernière est nécessaire. Celui-ci se fixe sur le convoyeur et est conçu de manière à ce que la caméra donne une vue du dessus du convoyeur. Les dimensions sont pensées de manière à pouvoir fixer la caméra mais également de manière à ce que le support ne gène pas les dobots pendant leurs déplacements.

||||
|:---:|:---:|:---:|
|![Dessin de définition](/Portfolio/img/support-cam-kapla.png "Dessin de définition du support caméra")|![Modélisation de l'ensemble](/Portfolio/img/support-cam.png "Modélisation 3D du support caméra sur OnShape")|![Modélisation](/Portfolio/img/supp-cam-kapla.jpg "Support caméra fabriqué")|
|**Dessin de définition du support caméra**|**Modélisation 3D du support caméra sur OnShape**|**Support caméra fabriqué**|

Le support est d'abord modélisé sur OnShape puis fabriqué. Un morceau de tôle est découpé à la cisailleuse aux dimensions voulues. La plaque est ensuite percée à la perceuse à colonne. Certains trous serviront à visser le support au convoyeur, tandis que les autres serviront à visser la caméra au support. Enfin, on plie la tôle. Afin que le support ne fléchisse pas sous le poids de la caméra, un morceau de tôle est soudé par point en renfort.

### Ensemble du système

|||
|:---:|:---:|
|![Schéma de l'ensemble](/Portfolio/img/schema-ens-kapla.jpg "Schéma du système")|![Modélisation de l'ensemble](/Portfolio/img/ens-kapla.jpg "Modélisation 3D du système sur OnShape")|
|**Schéma du système**|**Modélisation 3D du système sur OnShape**|

## Programmation

### Programmation de la structure en "L"

Dans le but de réaliser la programmation du moteur dynamixel dans la structure, à l’aide d’une Arduino, nous utilisons la librairie *ardyno* afin d’importer *“dynamixelMotor”*. La fonction *motor.goalPosition()* est ensuite utilisée pour set l’angle du moteur.

Par la suite, il nous est nécessaire de pouvoir exploiter ce programme avec des appellations dans un programme en python. On réalise donc une liaison port série afin de communiquer avec l’Arduino depuis un programme en python. Pour cela nous utiliserons la bibliothèque *pyserial* afin d’importer *“Serial”*. On pourra alors taper la commande *serial.Serial(port,baudrate,timeout)* afin de se connecter au port série de l’Arduino.

![L](/Portfolio/img/structure-l-vid2.gif "Structure en L en fonctionnement")

### Programmation de la caméra

Afin de faire une étude de la position du Kapla sur le convoyeur, il est possible d'utiliser utiliser une caméra et une intelligence artificielle de reconnaissance d’image et de détection de centre de gravité. Un logigramme est préalablement construit pour structurer le programme. En utilisant un code trouvé sur Internet permettant de régler le filtre en direct sur une image ou une vidéo, nous choisissons les valeurs en codage HSV les plus adaptées pour extraire seulement le Kapla de l'image.

Au lancement des programmes on observe l’apparition de lignes vertes qui représentent les lignes verticales du Kapla, et de lignes rouges qui représentent les lignes horizontales du Kapla. Néanmoins, par faute de temps, le programme n’est pas fini et on voit apparaître de nombreux problèmes sur la détermination des lignes. En achevant ce programme, il est possible de connaître les 4 coins du Kapla et de son centre.

Nos résultats sont les suivants : 

![Résultats](/Portfolio/img/res-cam.jpg "Résultats obtenus par la programmation de la caméra")

### Capteur laser

Comme la caméra s'est avérée plus compliquée à utiliser et à intégrer que prévu dans la limite du temps imparti, nous avons donc utilisé le capteur pour détecter le Kapla en fin de course sur le convoyeur. Lorsque le capteur le détecte, le convoyeur s'arrête.

### Code du tri des Kapla

Afin de faciliter la prise et la pose des Kapla, on passe par une étape de tri de ces derniers. On a décidé de prendre les Kapla du plus en bas au plus en haut (en les prenant à terre) en remontant progressivement. Le tri se fait donc selon l’axe z. On parcourt ainsi la liste des positions des Kapla en les sélectionnant avec le z le plus bas.

### Code principal

Le code dit principal est le code obtenu après l’intégration de tous les morceaux de code séparés. Pour la logique globale qui en découle, on établit en amont un algorithme permettant de mieux comprendre la structure et l'algorithme de notre code. Pour le code principal, on intègre les différentes parties de code faites en amont et on les rassemble sous forme de fonctions que nous avons simplement à appeler dans le *main*.

![Logigramme](/Portfolio/img/logi-kapla.jpg "Logigramme du programme")

## Système final

|||
|:---:|:---:|
|![Photo du système](/Portfolio/img/kapla.jpg "Photo du système (vue de haut)")|![Photo du système](/Portfolio/img/kapla2.jpg "Photo du système (vue de côté)")|
|**Photo du système (vue de haut)**|**Photo du système (vue de côté)**|

Ci-dessous, une vidéo du système en fonctionnement à la fin du projet :

![Système en fonctionnement](/Portfolio/img/sys-kapla.gif "Système en fonctionnement")
