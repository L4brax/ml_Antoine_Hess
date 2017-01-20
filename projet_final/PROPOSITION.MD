# Proposition de projet

Mon projet s'appuie sur un projet déjà existant. Il s'agit d'un projet portant sur un dataset provenant du Modified National Institute of Standards and Technology (MNIST).
Les données sont récupérée depuis le site Kaggle, proposant une compétition sous la forme d'un tutoriel sur les différents algorithmes utilisés aujourd'hui en ML.

Le but de ce projet est d'analyser un ensemble d'image représentant des chiffres écrits à la main et de déterminer ces chiffres.
Le dataset comprend 28 000 images en dégradé de noir sous forme de csv. (La valeur du dégradé de chaque pixel est représenté dans une colonne,
  les images font 28px/28px, soit 784 pixels par images. On a donc 784 colonnes + 1 colonne de label.)

Ce projet possède pour moi les avantages suivants :

* Il permet de mettre en pratique plusieurs algorithmes vus en cours.
* C'est un cas de ML apparement classique pour apprendre, on a donc beaucoup d'information et d'aide de la communauté.
* Il est applicable et facilement et compréhensible dans la vie courante, on peut donc par exemple généraliser le projet sur tous les caractères existants
  et essayer d'utiliser des caractères que l'on aurait écrit soit-même.

Au vu des informations trouvées sur des forums et le site Kaggle, on pourra mettre en pratique les algorithmes suivants :
* Random Forest
* k Near Neighbors (kNN)

Le but sera de comprendre comment fonctionne ces algorithmes, comment les mettre en pratique avec Python et ainsi de pouvoir les expliquer lors de la soutenance.

D'autres algorithmes sont évidemment utilisés dans les différents projets que l'on peut trouver :
* k Mean, pour réduire la taille des données
* Les classifiers
* PCA (Principal Component Analysis)
* CNN (Convolutional Neural Network)

On pourra donc continuer à travailler sur le projet lorsque les deux premiers algorithmes auront été assimilés avec d'autres algorithmes. Il sera alors intéréssant de comparer
 les résultats obtenus avec ces différentes méthodes et essayer de comprendre les différences si il y en a.
Certains de ces algorithmes étant complexes voire encore trop inconnus pour moi, il sera sûrement difficile de tous les utiliser.
Le projet sera sous la forme habituelle d'un notebook iPython, avec des images voire des vidéos pour comprendre les algorithmes


# Le planning :

* Status 1 - **lundi 30 janvier** : Prise en main du dataset, mise en place de la structure du notebook et de sa présentation, visualisation des images avec python/plot
* Status 2 - **vendredi 10 février** : Etude sur l'algorithme Random Forest et application de celui-ci sur notre dataset afin d'obtenir un premier résultat
* Status 3 - **lundi 20 février** : Etude sur l'algorithme k Near Neighbors et application de celui-ci sur notre dataset afin d'obtenir un second résultat
* Status 4 - **Mercredi 1 mars** : Utilisation d'autres algorithmes avec le temps qu'il reste et mise en comparaison des différents résultats - conclusions.
* Présentation finale : **jeudi 9 mars**
* Rapport final - **jeudi 16 mars**

*Note : N'ayant encore jamais mis en pratique ces algorithmes, le planning est peut-être "large" concernant les deux premiers algorithmes (20 jours) et court pour la 4eme partie*
