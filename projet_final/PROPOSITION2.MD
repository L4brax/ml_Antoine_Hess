## Proposition de projet.

Mon projet à pour thème l'analyse de sentiment.
Le but sera d'extraire les commentaires des utilisateurs du site TripAdvisor sur différents établissements/Lieux de Nantes et
de les analyser en grand nombre afin d'en dégager des tendances.

Les données seront extraites via l'API de tripAdvisor. Ces commentaires sont accompagnés d'une note sur 5.
Le but sera en premier lieu de prédire la note d'un utilisateur basé sur le sentiment dégagé de son commentaire.

Pour cela, il sera nécéssaire d'extraire un très grand nombre de commentaires, l'objectif étant d'avoir au moins 100 000 commentaires.

La première étape sera donc le nettoyage des données, plusieurs librairies sur le nettoyage de données relatifs aux textes permettant entre-autres de retirer les ponctuations, "mots morts" et expressions régulières.

Ce projet permettra de comprendre les différentes techniques d'analyse de sentiments (Opinion Mining/Sentiment Analysis).

# 20 Février : Mise à jour sur le dataset.

L'obtention d'un dataset concernant les reviews de TripAdvisor est compliquée. L'API ne permet pas d'obtenir directement les avis des utilisateurs. En recherchant sur internet, on peut trouver rapidement deux datasets de review provenant de tripAvisor de taille conséquente (environ 250 000 reviews). L'un d'entre eux comprend seulement les review, sans la note. il est donc peu utile pour mon cas. L'autre dataset comprend les notes des utilisateurs avec leurs reviews. Il est potentiellement utilisable.

Après ces recherches, j'ai pu obtenir un dataset non traité provenant d'Amazon d'une taille de près de 900 000 reviews.
Les données sont les reviews de la rubrique des livres.
Ce dataset est composé des données suivantes :
 - UniqueId (composé de l'asin et du product_name)
 - asin (Entier)
 - product_name (Chaine de caractères)
 - product_type (Chaine de caractères)
 - helpful (une note sur 5 dans le format suivant : "4 of 5")
 - rating (une note sur 5 dans le format suivant : "3.0", de 1 à 5.)
 - Title (Chaine de caractères)
 - Date (Date)
 - reviewer (chaine de caractères)
 - reviewer_location (chaine de caractères)
 - review_text (chaine de caractères)

Malgré le fait que ce dataset ne concerne pas la cible de mon idée première ; un dataset composé de reviews de lieux et d'établissement Nantais, il contient techniquement ce que je recherche, à savoir : Les reviews avec leur note (possibilité de les catégorisée en négative ou positive) et un nombre de review conséquent.

# Le planning

* Status 1 - **lundi 30 janvier** : Extraction des données et mise en place pour utilisation avec python. Nettoyage des données.

* Status 2 - **vendredi 10 février** : Mise à jour des données. Recherche sur le dataset. 

* Status 3 - **lundi 20 février** : Choix du nouveau dataset (voir mise à jour plus haut). Avant d'avoir trouvé sur quelles données me baser, j'ai pu avancer sur plusieurs méthodes de prédiction avec d'autres datasets. J'ai pu commencé à utiliser le nouveau dataset choisi.

* Status 4 - **Mercredi 1 mars** : En cours.

Présentation finale : jeudi 9 mars
Rapport final - jeudi 16 mars
