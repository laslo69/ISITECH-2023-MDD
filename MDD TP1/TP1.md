# MCD
![Alt text](<MCD TP1.png>)
# MLD
![Alt text](<MLD TP1.png>)
# MPD
![Alt text](<MPD TP1.png>)

```sql
DROP TABLE IF EXISTS famille ; 
CREATE TABLE famille 
(
    famille_id INT AUTO_INCREMENT NOT NULL, 
    famille_type VARCHAR, PRIMARY KEY (famille_id)
    ) ENGINE=InnoDB;  
    
    DROP TABLE IF EXISTS produit ; 
    CREATE TABLE produit 
    (
        produit_id INTEGER AUTO_INCREMENT NOT NULL, 
        produit_poids FLOAT, 
        produit_nom VARCHAR, 
        produit_quantite BIGINT, 
        #famille_id_produit INT, PRIMARY KEY (produit_id)
    ) ENGINE=InnoDB; 
        
         DROP TABLE IF EXISTS vente ; 
         CREATE TABLE vente 
         (
            vente_id INT AUTO_INCREMENT NOT NULL, 
            vente_poids FLOAT, 
            vente_date DATETIME, PRIMARY KEY (vente_id)
    ) ENGINE=InnoDB;  
    
    DROP TABLE IF EXISTS conteneur ; 
    CREATE TABLE conteneur 
    (
        conteneur_id_conteneur INT AUTO_INCREMENT NOT NULL, 
        #vente_id_contient INT, 
        #famille_id_contient INT, PRIMARY KEY (conteneur_id_conteneur)
    ) ENGINE=InnoDB;
```