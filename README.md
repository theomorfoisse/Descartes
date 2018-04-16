# Matlab ShapeContext

Ici sont répertoriés tous les codes nécessaires à l'apprentissage 
d'un réseau MLP avec comme inputs les histogrammes de shape context
calculés à partir des nuages de points des 60 000 images.

Il y a trois niveaux de profondeur dans ce code.

Le premier concerne le fichier fc_shapecontext. C'est le code qui gère l'apprentissage du réseau.
Il fait appel à une fonction: shapecontext 3,4 ou 5. C'est le deuxième niveau de profondeur.
Ces trois codes ont le même but: Le calcul des histogrammes de shape context à partir des nueages de points.

Il y en a trois. 

Shapecontext3 a été codé entièrement par moi même mais est le moins performant.
Shapecontext4 fait appel à une fonction sc_compute. C'es tune fonction crée par Serge Belongie pour calculer les shape contexts.
C'est le troisème niveau du code.
Enfin Shapecontext5, utilise aussi sc_compute, mais une version modifiée, faisant lui même appel à voisins.
Voisins permet d'adapter "l'angle de référence" des shapes contexts.

Il vaut mieux utiliser ShapeContext4. ( Attention le nombre d'inputs différe entre la version 4 et 5).

Enfin Shape permet de visualiser des histogrammes et des shapes contexts.
Malheuresement, cette fonction doit être adaptée pour pouvoir output les histogrammes 
avec les données fovéas.
