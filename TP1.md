## Table des matières
- [TP 1](#tp-1)
- [Instructions SQL](#instructions-sql)
  - [GROUP BY](#group-by)
  - [HAVING](#having)
  - [AS](#as)
  - [LIMIT](#limit)
  - [CASE](#case)
  - [ON DUPLICATE KEY UPDATE](#on-duplicate-key-update)
  - [MERGE](#merge)
  - [TRUNCATE](#truncate)
  - [ALTER TABLE](#alter-table)

---

## TP 1
En individuel, vous allez devoir compléter ce fichier **README** :

- Créez votre propre fichier à part.  
- Traitez un maximum de cas de figure sur le site [sql.sh](https://sql.sh).  
- **Restrictions** : pas de jointures, pas de procédures stockées, pas de triggers.  

Pour chaque instruction non vue en cours, vous devrez :
1. **Expliquer l’instruction** rapidement.  
2. **Donner un exemple concret** en utilisant la base de données `SAKILA`.  
   - Exemple : Récupérer tous les `state_code` de la table `cities` sans aucun doublon.  
   - Écrire ensuite la requête SQL correspondante.  
   - Noter le nombre de résultats obtenus.

---

## Instructions SQL

### GROUP BY
Permet de regrouper les valeurs dans une table en fonction d’une colonne.  
Exemple : SELECT actor_id, COUNT(film_id) FROM film_actor GROUP BY actor_id;

---

### HAVING
Permet de filtrer les résultats après un regroupement généralement avec un GROUP BY.  
Exemple : 

---

### AS
Permet de renommer une colonne ou une table pour simplifier la lecture des résultats.  
Exemple : SELECT name as n from category;

---

### LIMIT
Permet de limiter le nombre de résultats renvoyés par une requête.  
Exemple : SELECT name FROM category LIMIT 2;

---

### CASE
Permet d’afficher un message ou une valeur en fonction d’une condition.  
Exemple :  
    SELECT customer_id, amount, CASE  
	    WHEN amount < 10 THEN 'Radin'  
        WHEN amount < 40 THEN 'Ok'  
        ELSE 'Richou'  
        END  
    FROM payment;  

---

### ON DUPLICATE KEY UPDATE
Permet d’éviter de décider entre `INSERT` ou `UPDATE`.  
Exemple : INSERT INTO `staff` (`staff_id`, `first_name`, `last_name`, `address_id`, `picture`, `email`, `store_id`, `active`, `username`, `password`, `last_update`) VALUES (147, 'test', 'test', '73', NULL, NULL, '1', '1', 'test', NULL, CURRENT_TIMESTAMP(3)) ON DUPLICATE KEY UPDATE last_update = CURRENT_TIMESTAMP(3);


---

### MERGE
Permet de fusionner deux tables.  
Exemple :  

---

### TRUNCATE
Permet de vider une table rapidement, sans supprimer sa structure.  
Exemple : TRUNCATE TABLE test;

---

### ALTER TABLE
Permet de modifier la structure d’une table :  
Exemple :  
    - pour ajouter : ALTER TABLE actor ADD test_nom varchar(255);  
    - pour modiffié : ALTER TABLE actor CHANGE test_nom test_nbr INT;  
    - pour supprimer : ALTER TABLE actor DROP test_nbr;  

---

**Fin du TP 1**

