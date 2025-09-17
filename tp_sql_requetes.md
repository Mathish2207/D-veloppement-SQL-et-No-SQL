# TP SQL - Requêtes Simples Partie 1

## 1) Sélectionner tous les employés
```sql
SELECT * 
FROM employees;
```

## 2) Sélectionner tous les employés par leurs noms et prénoms
```sql
SELECT last_name, first_name 
FROM employees;
```

## 3) Sélectionner les noms distincts des employés
```sql
SELECT DISTINCT last_name 
FROM employees;
```

## 4) Sélectionner les noms et prénoms distincts des employés
```sql
SELECT DISTINCT last_name, first_name 
FROM employees;
```

## 5) Sélectionner les noms et prénoms des employés dont le nom est « alencar »
```sql
SELECT last_name, first_name 
FROM employees
WHERE last_name = 'alencar';
```

## 6) Sélectionner les employés dont le nom est « alencar » et de sexe masculin
```sql
SELECT * 
FROM employees
WHERE last_name = 'alencar'
  AND gender = 'M';
```

## 7) Sélectionner les employés dont le prénom « Danai » ou « Leen » en utilisant « OR »
```sql
SELECT * 
FROM employees
WHERE first_name = 'Danai'
   OR first_name = 'Leen';
```

## 8) Sélectionner les employés dont le prénom « Danai » ou « Leen » en utilisant « IN »
```sql
SELECT * 
FROM employees
WHERE first_name IN ('Danai', 'Leen');
```

## 9) Sélectionner les employés dont le nom est « alencar » et le prénom « Danai » ou « Leen » en utilisant « OR »
```sql
SELECT * 
FROM employees
WHERE last_name = 'alencar'
  AND (first_name = 'Danai' OR first_name = 'Leen');
```

## 10) Sélectionner les employés dont le nom est « alencar » et le prénom « Danai » ou « Leen » en utilisant « IN »
```sql
SELECT * 
FROM employees
WHERE last_name = 'alencar'
  AND first_name IN ('Danai', 'Leen');
```

## 11) Sélectionner les employés dont le numéro d’employé est compris entre 50000 et 50150
```sql
SELECT * 
FROM employees
WHERE employee_id BETWEEN 50000 AND 50150;
```

## 12) Sélectionner les employés dont le nom est « alencar » et le numéro d’employé est compris entre 50000 et 60000
```sql
SELECT * 
FROM employees
WHERE last_name = 'alencar'
  AND employee_id BETWEEN 50000 AND 60000;
```

## 13) Sélectionner les employés dont le nom est « alencar » et le prénom est « danai » ou le numéro d’employé est compris entre 50000 et 60000
```sql
SELECT * 
FROM employees
WHERE (last_name = 'alencar' AND first_name = 'danai')
   OR employee_id BETWEEN 50000 AND 60000;
```

## 14) Sélectionner les employés dont le nom est « alencar » ou, le prénom est « danai » ou « leen » et le numéro d’employé est compris entre 50000 et 60000
```sql
SELECT * 
FROM employees
WHERE last_name = 'alencar'
   OR (first_name IN ('danai','leen') AND employee_id BETWEEN 50000 AND 60000);
```

## 15) Sélectionner les employés dont le prénom commence par un « T »
```sql
SELECT * 
FROM employees
WHERE first_name LIKE 'T%';
```

## 16) Sélectionner les employés masculin dont la deuxième lettre du prénom est un « T »
```sql
SELECT * 
FROM employees
WHERE gender = 'M'
  AND first_name LIKE '_T%';
```

## 17) Sélectionner les employés dont le nom est « alencar » et le prénom « danai » ou le numéro d’employé commence par un 5
```sql
SELECT * 
FROM employees
WHERE (last_name = 'alencar' AND first_name = 'danai')
   OR employee_id LIKE '5%';
```

## 18) Sélectionner les employés dont le prénom commence par un « T » et termine par un « B »
```sql
SELECT * 
FROM employees
WHERE first_name LIKE 'T%B';
```

## 19) Sélectionner les employés dont le prénom commence par un « T », la 3ème lettre est un « R »
```sql
SELECT * 
FROM employees
WHERE first_name LIKE 'T_R%';
```

## 20) Sélectionner les employés dont le prénom commence par un « T », la 3ème lettre est un « R » et le numéro d’employé est compris entre 50000 et 60000
```sql
SELECT * 
FROM employees
WHERE first_name LIKE 'T_R%'
  AND employee_id BETWEEN 50000 AND 60000;
```

## 21) Sélectionner les employés dont le prénom contient « TZV »
```sql
SELECT * 
FROM employees
WHERE first_name LIKE '%TZV%';
```

## 22) Sélectionner les employés masculin ou dont le numéro d’employé est compris entre 50000 et 60000 et, le prénom contient « TZV »
```sql
SELECT * 
FROM employees
WHERE (gender = 'M' OR employee_id BETWEEN 50000 AND 60000)
  AND first_name LIKE '%TZV%';
```

## 23) Sélectionner les employés dont le prénom termine par « CAL»
```sql
SELECT * 
FROM employees
WHERE first_name LIKE '%CAL';
```

## 24) Sélectionner les employés dont le prénom termine par « CAL» de genre masculin et dont le numéro d’employé est compris entre 50000 et 60000
```sql
SELECT * 
FROM employees
WHERE first_name LIKE '%CAL'
  AND gender = 'M'
  AND employee_id BETWEEN 50000 AND 60000;
```

## 25) Sélectionner les employés dont le prénom est « danai » ou « leen » et le nom se termine par « TH» ou dont le numéro d’employé est compris entre 50000 et 100000
```sql
SELECT * 
FROM employees
WHERE ((first_name IN ('danai','leen') AND last_name LIKE '%TH')
    OR employee_id BETWEEN 50000 AND 100000);
```

## 26) Sélectionner les employés dont la date de naissance est null
```sql
SELECT * 
FROM employees
WHERE birth_date IS NULL;
``` ()
# TP SQL - requêtes Siples Partie 2

## 27. Sélectionner le nombre d’employés par département
```sql
SELECT dept_no, COUNT(*) 
FROM dept_emp 
GROUP BY dept_no;
``` (9)
28. Sélectionner le salaire maximum et minimum des employés
```sql
SELECT MAX(salary), MIN(salary) 
FROM salaries;
``` (1)
29. Sélectionner le salaire maximum et minimum par employés
```sql

``` ()
30. Sélectionner la moyenne de salaire par employés
```sql

``` ()
31. Sélectionner la moyenne de salaire par employés si leur numéro contient « 150 »
```sql

``` ()
32. Sélectionner le nombre d’employés par département avec un résumé général
```sql

``` ()
33. Sélectionner le nombre d’employés par département si leur numéro d’employé est compris entre 10000 et 50000
```sql

``` ()
34. Sélectionner la moyenne, le minimum et le maximum des salaires par employé si leur numéro est compris entre 10005 et 10105 avec un résumé général
```sql

``` ()
35. Sélectionner le nombre d’employés par département pour les départements « d005 » et « d006 »
```sql

``` ()
36. Sélectionner le nombre d’employés par département s’il est inférieur à 50000
```sql

``` ()
37. Sélectionner la moyenne des salaires par employé si elle est comprise entre 40000 et 50000
```sql

``` ()
38. Sélectionner la liste des employées en ordre alphabétique inversé de nom
```sql

``` ()
39. Sélectionner la liste des employés en ordre alphabétique inversé de nom et en ordre alphabétique par prénom
```sql

``` ()
40. Sélectionner le nombre d’employés par département du plus petit au plus grand
```sql

``` ()
41. Sélectionner le salaire maximum et minimum des employés, utiliser des alias
```sql

``` ()
42. Sélectionner les 10 premiers employés
```sql

``` ()
43. Sélectionner les noms et prénoms des 10 premiers employés, utiliser des alias
```sql

``` ()
44. Sélectionner 10 employés à partir du 5ème
```sql

``` ()
45. Sélectionner les noms et prénoms des 10 premiers employés en ordre alphabétique par nom
```sql

``` ()
46. Sélectionner la somme des salaires pour les 10 premiers employés si la somme est inférieure à 50000
```sql

``` ()
47. Sélectionner la somme des salaires par employés si leur numéro est compris entre 10001 et 50000 et la somme est inférieure à 50000
```sql

``` ()
48. Sélectionner la somme des salaires pour les 10 premiers employés si leur numéro est compris entre 10001 et 50000 et la somme est inférieure à 50000
```sql

``` ()
49. Sélectionner les employés et afficher les catégories de département (d001 = « Département n°1 », d002 = « Département n°2 », …, d009 = « Département n°9 » et s’il n’y a pas de département) si le numéro d’employé est compris entre 10150 et 10200
```sql

``` ()
50. Sélectionner le nombre d’employés par département et afficher les catégories : supérieur à 50000 = « Élevé », supérieur ou égale à 20000 = « Correct », inférieur à 20000 = « Faible », utiliser des alias
```sql

``` ()
51. Sélectionner les moyennes des salaires par employés et afficher les catégories : supérieur à 100000 = « Très élevée », supérieur ou égale à 80000 = « Élevée », inférieur à 80000 = « Faible », utiliser des alias
```sql

``` ()

## Requêtes à faire obligatoirement avec des jointures

52. Sélectionner les noms, prénoms et numéros des employés et leur département actuel (INNER JOIN)
```sql

``` ()
53. Sélectionner les prénoms, noms et titres actuels des employés (INNER JOIN)
```sql

``` ()
54. Sélectionner les noms, prénoms et salaires des employés en Juin 1989 (INNER JOIN)
```sql

``` ()
55. Sélectionner les noms, prénoms et départements actuels des managers (INNER JOIN)
```sql

``` ()
56. Sélectionner les noms, prénoms et dates de début d'emploi des employés avec leur département (INNER JOIN)
```sql

``` ()
57. Sélectionner les noms et départements des employés ayant le même département que les managers ayant été embauchés après le 1er Janvier 1996 (INNER JOIN et Sous-requêtes)
```sql

``` ()
58. Sélectionner les employés et leur date d'embauche dans les départements où le salaire moyen est supérieur à 80000 (INNER JOIN et Sous-requêtes)
```sql

``` ()
59. Sélectionner les employés et les départements (CROSS JOIN)
```sql

``` ()
60. Sélectionner les postes actuels des employés avec les noms des départements (CROSS JOIN)
```sql

``` ()
61. Sélectionner les dates d'emploi des employés et les noms des départements (JOIN et CROSS JOIN)
```sql

``` ()
62. Sélectionner les noms, prénoms, dates d’embauche et départements des employés même s’ils n’ont pas de département associé (LEFT JOIN)
```sql

``` ()
63. Sélectionner les noms, prénoms et titres des employés même s’ils n’ont pas de titre associé (LEFT JOIN)
```sql

``` ()
64. Sélectionner les noms, prénoms et salaires des employés depuis 1985 (LEFT JOIN)
```sql

``` ()
65. Sélectionner les noms, prénoms et départements des employés même s’ils n’ont pas de département associé (RIGHT JOIN)
```sql

``` ()
66. Sélectionner les noms, prénoms et salaires des employés depuis 1985 (RIGHT JOIN)
```sql

``` ()
67. Sélectionner les noms, prénoms et titres des employés même s’ils n’ont pas de titre associé (RIGHT JOIN)
```sql

``` ()

## Requêtes à faire obligatoirement avec des sous-requêtes

68. Sélectionner les prénoms et noms des employés qui ne sont pas ou n’ont pas été managers, utiliser des alias
```sql

``` ()
69. Sélectionner les prénoms et noms des employés qui ont eu plus de 2 titres professionnels différents
```sql

``` ()
70. Sélectionner les numéros, prénoms et noms des employés qui ont eu un salaire compris entre 100000 et 150000
```sql

``` ()
71. Sélectionner les numéros, prénoms et noms des employés qui ont eu un salaire supérieur à 150000 et qui ne sont pas ou n’ont pas été managers
```sql

``` ()
72. Sélectionner les numéros des employés managers qui ont un salaire inférieur à 100000 et qui ont eu plus de 2 titres professionnels
```sql

``` ()
73. Sélectionner les noms des employés ayant été managers d'un département, utiliser des alias pour les résultats et l’appel des tables (EXISTS)
```sql

``` ()
74. Sélectionner les noms des employés pour qui il existe un salaire supérieur à 100000, utiliser des alias pour les résultats et l’appel des tables (EXISTS)
*```sql

``` ()
75. Sélectionner les noms des employés féminins ayant occupé un poste de manager, utiliser des alias (EXISTS)
```sql

``` ()
76. Sélectionner les noms et prénoms des employés ayant eu un salaire supérieur à 100000, utiliser des alias (EXISTS)
```sql

``` ()
77. Sélectionner les numéros, noms et prénoms des employés nés le 1er janvier 1960 pour qui il existe exactement deux titres professionnels différents au cours de leur carrière, utiliser des alias (EXISTS)
```sql

``` ()
78. Sélectionner les employés dont la date d'embauche est supérieure ou égale à la dernière prise de poste de manager, utiliser des alias (ALL)
```sql

``` ()
79. Sélectionner l’identifiant de l’employé dont le salaire est le plus élevé, utiliser des alias (ALL)
```sql

``` ()
80. Sélectionner le titre le plus donné aux employés
```sql

``` ()
81. Sélectionner les identifiants des employés dont la période d'emploi est plus longue que celle des autres employés (ALL)
```sql

``` ()
82. Sélectionner les employés qui ont le titre le plus fréquemment donné (ALL)
```sql

``` ()
83. Sélectionner les titres des employés ayant au moins un salaire supérieur à 150000$, utiliser des alias (ANY)
```sql

``` ()
84. Sélectionner le nombre d’employés managers (ANY)
```sql

``` ()
85. Sélectionner les noms des employés ayant été dans au moins un département et ayant eu un salaire supérieur à 150 000$, utiliser des alias (ANY)
```sql

``` ()
86. Sélectionner les prénoms des employés ayant le titre « Senior Engineer » (ANY)
```sql

``` ()
87. Sélectionner le nombre de salariés ayant un salaire supérieur à la moyenne (ANY)
```sql

``` ()