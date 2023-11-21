# Cheat sheet SQL
  
## Outils de base  
  
### Vocabulaire  

*= tout  
 Querry = requête
  
### Nouvelle Colonne  
```SELECT (A+B) AS (Nom de la nouvelle colonne)```  
  
### Nouvelle Ligne  
```INSERT INTO (Nom de la table) (Nom Colonne, Nom Colonne, ...) values (valeur, valeur, ...)```  
  
### Corrigé une valeur
```UPDATE (Nom de la table) SET (Nom colonne) = (Nouvelle Valeur) WHERE (Nom colonne) = (Ancienne Valeur)```  

### Supprimé des Ligne  
```DELETE FROM (Nom de la table) WHERE (condition) ```  
  
### Créer une Table  
```CREATE TABLE (Nom de la table) (Nom colonne FLOAT, Nom colone TEXT, ...) ```  
  
### Ajouter une Colonne  
```ALTER TABLE (Nom de la table) ADD column (Nom de la nouvelle colonne) FLOAT/TEXT/...  DEFAULT (valeur par default de la colonne) ```  
  
### Supprimer une Colonne  
``ALTER TABLE (Nom de la table) DROP (Nom Colonne)  ``  
  
### Renommé une Table
```ALTER TABLE (Nom de la table) RENAME TO (Nom Nouveau) ```  
  
### Supprimer une Table  
```DROP TABLE IF EXISTS (Nom de la table)  ```  
  
## L'ordre  
  
- FROM and JOIN...ON    (Indique la table et Rassemble 2 tableau à partir d'une colonne commune)
- WHERE                 (condition)
- GROUP BY              (Regroupe ou affiche tout les groupes identique)
- HAVING                
- SELECT                (Choisir une colonne)
- DISTINCT              (Fait la même chose que GROUP BY)
- ORDER BY              (ASC Trié par ordre croissant, DESC pour décroissant)
- LIMIT / OFFSET        (Combien de donné, à partir de, Attention, tableau commence à 0)
  
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
  
## Type  
  
| Type de données | Description                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| INTEGER, BOOLEAN | Les types de données entiers peuvent stocker des valeurs entières comme le nombre d'une quantité ou l'âge. Dans certaines implémentations, la valeur booléenne est simplement représentée comme une valeur entière de 0 ou 1. |
| FLOAT, DOUBLE, REAL | Les types de données à virgule flottante peuvent stocker des données numériques plus précises telles que des mesures ou des valeurs fractionnaires. Différents types peuvent être utilisés en fonction de la précision à virgule flottante requise pour cette valeur. |
| CHARACTER(num_chars), VARCHAR(num_chars), TEXT | Les types de données basés sur le texte peuvent stocker des chaînes de caractères et du texte dans toutes sortes de langues. La distinction entre les différents types dépend généralement de l'efficacité sous-jacente de la base de données lors de la manipulation de ces colonnes. Les types CHARACTER et VARCHAR (caractère variable) sont spécifiés avec le nombre maximum de caractères qu'ils peuvent stocker (les valeurs plus longues peuvent être tronquées), ce qui peut être plus efficace pour stocker et interroger de grandes tables. |
| DATE, DATETIME | SQL peut également stocker des dates et des horodatages pour suivre les séries temporelles et les données d'événements. Ils peuvent être délicats à manipuler, en particulier lors de la manipulation de données à travers les fuseaux horaires. |
| BLOB | Enfin, SQL peut stocker des données binaires sous forme de blobs directement dans la base de données. Ces valeurs sont souvent opaques pour la base de données, donc vous devez généralement les stocker avec les bonnes métadonnées pour les requêter ultérieurement. |
| PRIMARY KEY      | Cela signifie que les valeurs de cette colonne sont uniques, et chaque valeur peut être utilisée pour identifier une seule ligne dans cette table.   |
| AUTOINCREMENT    | Pour les valeurs entières, cela signifie que la valeur est automatiquement remplie et incrémentée à chaque insertion de ligne. Non pris en charge dans toutes les bases de données. |
| UNIQUE           | Cela signifie que les valeurs de cette colonne doivent être uniques, vous ne pouvez donc pas insérer une autre ligne avec la même valeur dans cette colonne comme une autre ligne de la table. Diffère de la `PRIMARY KEY` en ce qu'elle n'a pas besoin d'être une clé pour une ligne dans la table. |
| NOT NULL         | Cela signifie que la valeur insérée ne peut pas être `NULL`.                                                                                      |
| CHECK (expression) | Cela vous permet d'exécuter une expression plus complexe pour tester si les valeurs insérées sont valides. Par exemple, vous pouvez vérifier que les valeurs sont positives, supérieures à une taille spécifique, ou commencent par un certain préfixe, etc. |
| FOREIGN KEY      | Il s'agit d'une vérification de cohérence qui garantit que chaque valeur de cette colonne correspond à une autre valeur dans une colonne d'une autre table. Par exemple, s'il existe deux tables, l'une répertoriant tous les employés par ID et l'autre répertoriant leurs informations de paie, la `FOREIGN KEY` peut garantir que chaque ligne dans la table de paie correspond à un employé valide dans la liste principale des employés. |
