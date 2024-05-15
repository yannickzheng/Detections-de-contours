
# Suppression des yeux rouges

Supprime les yeux rouges d'une photographie donnée.


### Fonctions de Traitement d'Image

1. **Ajout de Sommets à une File**
   La fonction `ajoute_sommets` prend une file de coordonnées de pixels et une liste de coordonnées, puis ajoute tous les éléments de la liste à la file. Cette opération est utilisée pour gérer les groupes de pixels lors du traitement d'images.

2. **Calcul de Composante Connexe**
   La fonction `composante_connexe` analyse une image pour déterminer la composante connexe d'un pixel donné. Elle renvoie un tableau de booléens linéarisé où chaque case indique si le pixel correspondant fait partie de la même région connectée que le pixel de référence.

### Correction des Yeux Rouges

1. **Modification de Couleur de Pixel**
   La fonction `modif_coul` ajuste la couleur d'un pixel spécifique en remplaçant sa composante rouge par la moyenne des composantes verte et bleue. Cela permet de corriger la couleur sans altérer la luminosité ou les reflets, préservant ainsi l'aspect naturel des yeux dans l'image.

2. **Suppression des Yeux Rouges**
   La fonction `enlever_yeux_rouges` parcourt un tableau de booléens représentant les pixels à corriger (obtenu via `composante_connexe`) et modifie la couleur des pixels rouges détectés en utilisant `modif_coul`. Cette méthode élimine l'effet des yeux rouges causé par le flash photographique.

Ces fonctions constituent un ensemble d'outils pour le traitement d'images, en particulier pour la correction des yeux rouges, tout en préservant la qualité visuelle de l'image.
