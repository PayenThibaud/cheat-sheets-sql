# Cheat sheet postgreSQL  
  
## Outils de base  
  
### Alias
`alias psql='sudo -u postgres psql'`  
  
### Prendre un fichier window à Ubuntu  
 `mv "/mnt/c/Users/Thibaud Payen/Downloads/person.sql" ~/sites`  

### commande basique  
psql => ouvrir psql utilisateur postgres dans postgres  
pgcli => ouvrir pgcli utilisateur thibaud dans thibaud  
\l => Voir toute les databases  
\q => quitter  
psql => allez dans le mode psql  
CREATE DATABASE (nom) => créer une database  
psql -h (localhost / ip) -P (Port 5432) -U (nom Utilisateur) (database) => entré directement dans une database  
\c (nom database) => rentrer dans la database  
DROP DATABASE (nom database) => efface la database  
CREATE TABLE (nom table) ( (nom colonne) (type(chiffre)), nom...); => créer une table  
\d => voir les tables de la database  
\d (nom) => voir la table  
INSERT INTO (nom table) ( (nom colonne),(nom colonne2), ...) VALUES ( (valeur), (valeur2) ); => ajouter des donnée aux table  
WHERE (nom colonne) IN ('valeur1', valeur2,...) => ne pas s'embêter avec OR sur la même colonne  

  
## Type de donnée  
  
| Type de Données | Alias | Description |
|------------------|-------|-------------|
| bigint           | int8  | Entier signé sur huit octets |
| bigserial        | serial8 | Entier sur huit octets à incrémentation automatique |
| bit [ (n) ]      |       | Suite de bits de longueur fixe |
| bit varying [ (n) ] | varbit [ (n) ] | Suite de bits de longueur variable |
| boolean          | bool  | Booléen (Vrai/Faux) |
| bytea            |       | Donnée binaire (« tableau d'octets ») |
| character [ (n) ] | char [ (n) ] | Chaîne de caractères de longueur fixe |
| character varying [ (n) ] | varchar [ (n) ] | Chaîne de caractères de longueur variable |
| cidr             |       | Adresse réseau IPv4 ou IPv6 |
| circle           |       | Cercle dans le plan |
| date             |       | Date du calendrier (année, mois, jour) |
| double precision | float8 | Nombre à virgule flottante de double précision (sur huit octets) |
| inet             |       | Adresse d'ordinateur IPv4 ou IPv6 |
| integer          | int, int4 | Entier signé sur quatre octets |
| interval [ champs ] [ (p) ] |       | Intervalle de temps |
| json             |       | Données texte JSON |
| jsonb            |       | Données binaires JSON, décomposées |
| line             |       | Droite (infinie) dans le plan |
| lseg             |       | Segment de droite dans le plan |
| macaddr          |       | Adresse MAC (pour Media Access Control) |
| macaddr8         |       | Adresse MAC (pour Media Access Control) (format EUI-64) |
| money            |       | Montant monétaire |
| numeric [ (p, s) ] | decimal [ (p, s) ] | Nombre exact dont la précision peut être spécifiée |
| path             |       | Chemin géométrique dans le plan |
| pg_lsn           |       | Séquence numérique de journal (Log Sequence Number) de PostgreSQL |
| pg_snapshot      |       | Image (snapshot) de l'identifiant de transaction niveau utilisateur |
| point            |       | Point géométrique dans le plan |
| polygon          |       | Chemin géométrique fermé dans le plan |
| real             | float4 | Nombre à virgule flottante de simple précision (sur quatre octets) |
| smallint         | int2  | Entier signé sur deux octets |
| smallserial      | serial2 | Entier sur deux octets à incrémentation automatique |
| serial           | serial4 | Entier sur quatre octets à incrémentation automatique |
| text             |       | Chaîne de caractères de longueur variable |
| time [ (p) ] [ without time zone ] |       | Heure du jour (sans fuseau horaire) |
| time [ (p) ] with time zone | timetz | Heure du jour, avec fuseau horaire |
| timestamp [ (p) ] [ without time zone ] |       | Date et heure (sans fuseau horaire) |
| timestamp [ (p) with time zone | timestamptz | Date et heure, avec fuseau horaire |
| tsquery   
