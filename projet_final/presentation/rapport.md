## Projet Machine Learning.

Mon projet à pour thème l'analyse de sentiment.
Ce projet permettra de comprendre les différentes techniques d'analyse de sentiments (Opinion Mining/Sentiment Analysis).

Le but sera d'extraire des reviews afin de les analyser en grand nombre afin d'en dégager des tendances.
Ces reviews sont accompagnés d'autres données dont une note sur 5.
Le but de prédire la tendance du review d'un utilisateur basé sur le sentiment dégagé de son commentaire.

Pour cela, il faut d'abord extraire un très grand nombre de commentaires, l'objectif au départ est d'avoir 100 000 commentaires.
La première étape sera donc le nettoyage des données, plusieurs librairies existent sur le nettoyage de données relatifs aux textes permettant entre-autres de retirer les ponctuations, "mots morts" et expressions régulières.

# Le dataset.

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
