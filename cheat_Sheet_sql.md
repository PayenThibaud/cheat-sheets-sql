# Cheat sheet SQL
  
## Outils de base  
  
SELECT => Choisir une colonne  
FROM => Choisir une table  
* => tout  
WHERE => Condition : 
BETWEEN => entre valeur1 AND valeur2  
| Opérateur              | Condition                                                  | Exemple SQL                   |
|------------------------|------------------------------------------------------------|-------------------------------|
| =, !=, <, <=, >, >=     | Opérateurs numériques standards                             | col_name != 4                 |
| BETWEEN ... AND ...    | Le nombre est dans la plage de deux valeurs (inclusivement) | col_name BETWEEN 1.5 AND 10.5 |
| NOT BETWEEN ... AND ...| Le nombre n'est pas dans la plage de deux valeurs (inclusivement) | col_name NOT BETWEEN 1 AND 10 |
| IN (...)               | Le nombre existe dans une liste                              | col_name IN (2, 4, 6)         |
| NOT IN (...)           | Le nombre n'existe pas dans une liste                        | col_name NOT IN (1, 3, 5)     |

## Vocabulaire   
  
Query => requête
