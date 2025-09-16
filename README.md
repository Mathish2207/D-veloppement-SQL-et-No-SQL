# D-veloppement-SQL-et-No-SQL

## TP 1
En individuel, vous allez devoir continuer, ce fichier readme :

Vous créez votre propre fichier, a part
Vous traitez un maximum de cas de figure sur le site sql.sh
Vous ne faites ni de jointure, ni de procédures stockées, ni de trigger
Vous allez devoir pour chaque instruction que l'on n'a pas vu :

expliquer l'instruction rapidement
en vous servant de la base de données "SAKILA", vous allez créer 1 à 3 cas defigure nécessitants une requete. Par exemple :"Récupérer tous les state_code de la table cities sans aucun doublon". Vous devrez ensuite écrire la requete SQL correspondante, par exemple : SELECT DISTINCT state_code FROM cities;. Notez le nombre de résultats obtenus par exemple (1185).

- "GROUP BY" : Permet de regrouper dans une table les valeurs en fonction d'une colonne.<br>
Ex : SELECT actor_id, COUNT(film_id) FROM film_actor GROUP BY actor_id;

- "HAVING" : Permet de filtrer les résultats.<br>
Ex : SELECT actor_id, COUNT(film_id) FROM film_actor GROUP BY actor_id;