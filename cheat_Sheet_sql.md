# Cheat sheet SQL
  
## Outils de base  
  
SELECT => Choisir une colonne  
FROM => Choisir une table  
    * => tout  
WHERE => Condition :   
BETWEEN => entre valeur1 AND valeur2  
SELECT DISTINCT => affiche les données mais retirer les duplication.  
WHERE ... ORDER BY ( ASC/DESC)=> trie dans l'ordre abc / cba  
order ... LIMIT (nombre de donné à envoyé) OFFSET (à partir de ou)  
from ... Join (nom du tableau2) On (tableau1.nom = tableau2.nom)  
il existe aussi left/right/full Join...  
SELECT ... , (A + B) / 10 AS (nom de la nouvelle colonne) ou (a) AS (nom)  
GROUP BY => réunis toute les lignes sur les différents nom  
  
## L'ordre  
  
- FROM and JOIN...ON
- WHERE
- GROUP BY
- HAVING
- SELECT
- DISTINCT
- ORDER BY
- LIMIT / OFFSET
  
## Fonction  
  
| Fonction            | Description                                                                                                           |
|---------------------|-----------------------------------------------------------------------------------------------------------------------|
| COUNT(*), COUNT(column) | Compte le nombre de lignes dans le groupe si aucun nom de colonne n'est spécifié. Sinon, compte le nombre de lignes dans le groupe avec des valeurs non NULL dans la colonne spécifiée. |
| MIN(column)         | Trouve la plus petite valeur numérique dans la colonne spécifiée pour toutes les lignes du groupe.                   |
| MAX(column)         | Trouve la plus grande valeur numérique dans la colonne spécifiée pour toutes les lignes du groupe.                   |
| AVG(column)         | Trouve la valeur numérique moyenne dans la colonne spécifiée pour toutes les lignes du groupe.                       |
| SUM(column)         | Trouve la somme de toutes les valeurs numériques dans la colonne spécifiée pour les lignes du groupe.                |



## Opérateur  
  
| Opérateur              | Condition                                                  | Exemple SQL                   |
|------------------------|------------------------------------------------------------|-------------------------------|
| =, !=, <, <=, >, >=     | Opérateurs numériques standards                             | col_name != 4                 |
| BETWEEN ... AND ...    | Le nombre est dans la plage de deux valeurs (inclusivement) | col_name BETWEEN 1.5 AND 10.5 |
| NOT BETWEEN ... AND ...| Le nombre n'est pas dans la plage de deux valeurs (inclusivement) | col_name NOT BETWEEN 1 AND 10 |
| IN (...)               | Le nombre existe dans une liste                              | col_name IN (2, 4, 6)         |
| NOT IN (...)           | Le nombre n'existe pas dans une liste                        | col_name NOT IN (1, 3, 5)     |
| =                      | Correspondance exacte sensible à la casse                           | col_name = 'abc'              |
| != or <>               | Inégalité exacte sensible à la casse                                | col_name != 'abcd'            |
| LIKE                   | Correspondance exacte insensible à la casse                          | col_name LIKE 'ABC'           |
| NOT LIKE               | Inégalité exacte insensible à la casse                               | col_name NOT LIKE 'ABCD'      |
| %                      | Utilisé n'importe où dans une chaîne pour correspondre à une séquence de zéro ou plusieurs caractères (uniquement avec LIKE ou NOT LIKE) | col_name LIKE '%AT%' (correspond à "AT", "ATTIC", "CAT", voire même "BATS") |
| _                      | Utilisé n'importe où dans une chaîne pour correspondre à un seul caractère (uniquement avec LIKE ou NOT LIKE) | col_name LIKE 'AN_' (correspond à "AND", mais pas à "AN") |
| IN (...)               | La chaîne existe dans une liste                                      | col_name IN ('A', 'B', 'C')   |
| NOT IN (...)           | La chaîne n'existe pas dans une liste                                 | col_name NOT IN ('D', 'E', 'F')|
| IS NULL                | La valeur de la colonne est NULL                               | col_name IS NULL              |
| IS NOT NULL            | La valeur de la colonne n'est pas NULL                         | col_name IS NOT NULL          |


## Vocabulaire   
  
Query => requête
