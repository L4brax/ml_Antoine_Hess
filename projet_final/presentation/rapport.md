# Projet Machine Learning.

Mon projet à pour thème l'analyse de sentiment.
Ce projet permettra de comprendre les différentes techniques d'analyse de sentiments (Opinion Mining/Sentiment Analysis).

Le but sera d'extraire des reviews afin de les analyser en grand nombre afin d'en dégager des tendances.
Ces reviews sont accompagnés d'autres données dont une note sur 5.
Le but de prédire la tendance du review d'un utilisateur basé sur le sentiment dégagé de son commentaire.

Pour cela, il faut d'abord extraire un très grand nombre de commentaires, l'objectif au départ est d'avoir 100 000 commentaires.
La première étape sera donc le nettoyage des données, plusieurs librairies existent sur le nettoyage de données relatifs aux textes permettant entre-autres de retirer les ponctuations, "mots morts" et expressions régulières.

## Le dataset.

L'obtention d'un premier dataset concernant les reviews de TripAdvisor a été compliquée. L'API ne permet pas d'obtenir directement les avis des utilisateurs. En recherchant sur internet, on peut trouver rapidement deux datasets de reviews provenant de tripAvisor de taille conséquente (environ 250 000 reviews). L'un d'entre eux comprend seulement les reviews, sans la note. il est donc peu utile pour mon cas. L'autre dataset comprend les notes des utilisateurs avec leurs reviews. Il est potentiellement utilisable. Cependant, celui est partiellement traité et le fichier s'est avéré difficile pour moi à parser.
Désirant un dataset non préalablement traité et arpès un long moment de recherches, j'ai pu obtenir un dataset non traité provenant d'Amazon d'une taille de près d'environ 100 000 reviews.

Les données sont les reviews de la rubrique des livres.
Ce dataset est composé des données suivantes :
 - reviewScore (une note sur 5 dans le format suivant : "3.0", de 1 à 5.)
 - link (Un lien concernant le review, inutile ici)
 - reviewTitle (Le titre du du review)
 - reviewText (le commentaire)

Malgré le fait que ce dataset ne concerne pas la cible de mon idée première ; un dataset composé de reviews de lieux et d'établissement Nantais, il contient techniquement ce que je recherche, à savoir : Les reviews avec leur note (possibilité de les catégorisée en négative ou positive) et un nombre de review conséquent.

# Le nettoyage

Un premier nettoyage est effectué avec la librairie BeautifulSoup afin de retirer les différentes balises HTML des reviews.

Sachant que la méthode bag of words sera utilisée, il n'est pas nécéssaire de garder la ponctuation. En effet, avec la ponctuation, le mot "livre," sera différent du mot "livre."
L'utilisation d'une expression regulière avec la librairie 're' est utilisé pour y parvenir.

Le texte et ensuite transformé en un tableau de mots afin d'être géré par la librairie 'nltk'.
Cette librairie va nous permettre, grâce à une de ses fonctionnalité, de retirer les stop-words.

Ces différentes actions sont regroupées dans une fonction et appliquée sur chaque reviews.

# L'algorithme

Afin de créer les bag of words, la librairie 'sklearn' est utilisée avec sa fonctionnalité 'CountVectorizer'.
La taille maximum du dictionnaire sera de 5000 mots. On obtiendra donc dans ce dictionnaire les 5000 mots les plus fréquents.

Un classifier Random Forest de 100 arbres est préparé sur une première partie des données.
Une fois le classifier préparé sur ces données, il est utilisé sur le test set.
On obtient un tableau contenant le score prédit par le random forest.

# Les résultats

Avec ce premier algorithme, on peut observer que les résultats sont déjà intéréssants. On obtient une prédiction correcte pour environ 80% des commentaires, ce qui est je trouve assez élevé compte tenu du fait que le nettoyage de nos données reste très simple.

Une première amélioration envisagée est d'utiliser l'algorithme Word2Vec afin d'obtenir un sac de mot plus précis sur le sentiment dégagé du review. Cet algorithme permet aussi de rassembler les expressions de plusieurs mot en un seul mot, comme par exemple "san francisco" en "san_francisco".

# Conclusion

Le lancement d'un premier algorithme fonctionnel a été difficile pour moi car j'ai eu du mal à obtenir des données utilisables. Je me suis retrouvé souvent avec un jeu de données que je n'arrivais pas à utiliser, plus précisemment à parser correctement. Je n'ai ainsi pas travaillé sur mon projet pendant plusieurs jours par manque de motivation et pris un retard conséquent. Je suis quand même en partie satisfait du peu que j'ai pu faire car l'implémentation de mon algorithme fonctionne et produit un résultat correct. En point d'amélioration, je pense que j'aurais dû mesurer la difficultée d'obtention des données et m'autoriser plus rapidement à chercher des données qui ne sont pas forcément du thème que j'avais choisi mais qui sont du même type. Si je devais me noter, je me donnerais un 10/20. Cette note prendrait en compte le fait que j'ai compris plusieurs principes en machine learning, que j'ai pu en appliquer un. Elle prendrait cependant aussi en compte que je n'ai pas pu appliquer la plupart de ces principes dans les temps, avec un manque de motivation et donc de travail au cours du projet.
