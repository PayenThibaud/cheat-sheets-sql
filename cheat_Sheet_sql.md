# Cheat sheet SQL
  
## Outils de base  
  
SELECT => Choisir une colonne  
FROM => Choisir une table  
    * => tout  
WHERE => Condition :   
BETWEEN => entre valeur1 AND valeur2  
SELECT DISTINCT => affiche les données mais retirer les duplication.
WHERE ... ORDER BY ( ASC/DESC)=> trie dans l'ordre abc / cba  
... LIMIT (nombre de donné à envoyé) OFFSET (à partir de ou)

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


## Vocabulaire   
  
Query => requête
