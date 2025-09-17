## Table des matières
- [TP 2](#tp-2)
- [Instructions SQL](#instructions-sql)
  - [LEFT INCLUSIVE](#left-inclusive)
  - [RIGHT INCLUSIVE](#right-inclusive)
  - [LEFT EXCLUSIVE](#left-exclusive)
  - [RIGHT EXCLUSIVE](#right-exclusive)
  - [FULL OUTER INCLUSIVE](#full-outer-inclusive)
  - [FULL OUTER EXCLUSIVE](#full-outer-exclusive)
  - [INNER](#inner)

---

## TP 2
Refaire les requêtes dans la BDD **World** (des requêtes qui font sens !) pour qu’on les intègre dans le cours.  
Idem que TP1, mais cette fois **avec des jointures** (BDD `SAKILA`).  

---

## Instructions SQL

### LEFT INCLUSIVE
Permet de récupérer toutes les lignes de la table A et aussi celles de la table B qui correspondent.  
Exemple : SELECT * FROM film_actor LEFT JOIN film ON film_actor.film_id = film.film_id;    

---

### RIGHT INCLUSIVE
Permet de récupérer toutes les lignes de la table B et aussi celles de la table A qui correspondent.  
Exemple : SELECT * FROM film_actor RIGHT JOIN film ON film_actor.film_id = film.film_id;    

---

### LEFT EXCLUSIVE
Permet de récupérer uniquement les lignes de la table A qui n’ont pas de correspondance dans la table B.  
Exemple : SELECT * FROM film_actor LEFT JOIN film ON film_actor.film_id = film.film_id WHERE film.film_id IS NULL;    

---

### RIGHT EXCLUSIVE
Permet de récupérer uniquement les lignes de la table B qui n’ont pas de correspondance dans la table A.  
Exemple : SELECT * FROM film_actor RIGHT JOIN film ON film_actor.film_id = film.film_id WHERE film_actor.film_id IS NULL;    

---

### FULL OUTER INCLUSIVE
Permet de récupérer toutes les lignes de la table A et toutes les lignes de la table B (peu importe si elles correspondent ou non).  
Exemple : SELECT * FROM film FULL JOIN language ON film.language_id = language.language_id; (marhce po avec phpmyadmin) ou SELECT f.film_id, f.title, fa.actor_id FROM film f LEFT JOIN film_actor fa ON f.film_id = fa.film_id UNION SELECT f.film_id, f.title, fa.actor_id FROM film_actor fa RIGHT JOIN film f ON f.film_id = fa.film_id;  

---

### FULL OUTER EXCLUSIVE
Permet de récupérer uniquement les lignes des deux tables qui n’ont pas de correspondance.  
Exemple : SELECT * FROM film FULL JOIN language ON film.language_id = language.language_id WHERE film.language_id IS NULL; (marhce po avec phpmyadmin) ou SELECT f.film_id, f.title, fa.actor_id FROM film f LEFT JOIN film_actor fa ON f.film_id = fa.film_id WHERE fa.film_id IS NULL UNION SELECT f.film_id, f.title, fa.actor_id FROM film_actor fa RIGHT JOIN film f ON f.film_id = fa.film_id WHERE f.film_id IS NULL;    

---

### INNER
Permet de récupérer uniquement les lignes des deux tables qui correspondent (FK non nulle).  
Exemple : SELECT * FROM film INNER JOIN film_actor ON film.film_id = film_actor.film_id;  

---

**Fin du TP 2**
