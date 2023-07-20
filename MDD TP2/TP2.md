![Alt text](<MCD TP2-1.png>) 
![Alt text](<MLD TP2-1.png>)


```sql
DROP TABLE IF EXISTS ensemble ; 
CREATE TABLE ensemble 
(
    codeEnsemble_ensemble INT AUTO_INCREMENT NOT NULL, 
    designation_ensemble VARCHAR(40), PRIMARY KEY (codeEnsemble_ensemble)
) ENGINE=InnoDB;

 DROP TABLE IF EXISTS sous_ensemble ; 
 CREATE TABLE sous_ensemble 
 (
    codeSousEnsemble_sous_ensemble INT AUTO_INCREMENT NOT NULL, designation_sous_ensemble VARCHAR(40), 
    longueur_sous_ensemble INT, 
    largeur_sous_ensemble INT, 
    hauteur_sous_ensemble INT, 
    prix_unitaire_sous_ensemble FLOAT, PRIMARY KEY (codeSousEnsemble_sous_ensemble)
 ) ENGINE=InnoDB;


DROP TABLE IF EXISTS composant ; 
CREATE TABLE composant 
(
    codeComposant_composant INT AUTO_INCREMENT NOT NULL, designation_composant VARCHAR, 
    prixUnitaire_composant FLOAT, PRIMARY KEY (codeComposant_composant)
) ENGINE=InnoDB;


DROP TABLE IF EXISTS lienEnsComposant ; 
CREATE TABLE lienEnsComposant 
(
    codeEnsemble_ensemble **NOT FOUND** AUTO_INCREMENT NOT NULL, codeComposant_composant **NOT FOUND** NOT NULL, #codeEnsemble_lienEnsComposant INT, 
    #codeComposant_lienEnsComposant INT, 
    quantite_lienEnsComposant INT, PRIMARY KEY (codeEnsemble_ensemble,  codeComposant_composant)
) ENGINE=InnoDB


DROP TABLE IF EXISTS lienSeComposant ; 
CREATE TABLE lienSeComposant 
(
    codeComposant_composant **NOT FOUND** AUTO_INCREMENT NOT NULL, codeSousEnsemble_sous_ensemble **NOT FOUND** NOT NULL, #codeSousEnsemble_lienSeComposant INT, 
    #codeComposant_lienSeComposant INT, 
    quantite_lienSeComposant INT, PRIMARY KEY (codeComposant_composant,  codeSousEnsemble_sous_ensemble)
) ENGINE=InnoDB;


DROP TABLE IF EXISTS lienEnsComposant ; 
CREATE TABLE lienEnsComposant 
(
    codeEnsemble_ensemble **NOT FOUND** AUTO_INCREMENT NOT NULL, codeComposant_composant **NOT FOUND** NOT NULL, #codeEnsemble_lienEnsComposant INT, 
    #codeComposant_lienEnsComposant INT, 
    quantite_lienEnsComposant INT, PRIMARY KEY (codeEnsemble_ensemble,  codeComposant_composant)
) ENGINE=InnoDB; 



DROP TABLE IF EXISTS lienSeComposant ; 
CREATE TABLE lienSeComposant 
(
    codeComposant_composant **NOT FOUND** AUTO_INCREMENT NOT NULL, codeSousEnsemble_sous_ensemble **NOT FOUND** NOT NULL, #codeSousEnsemble_lienSeComposant INT, 
    #codeComposant_lienSeComposant INT, 
    quantite_lienSeComposant INT, PRIMARY KEY (codeComposant_composant,  codeSousEnsemble_sous_ensemble)
) ENGINE=InnoDB;


DROP TABLE IF EXISTS lienEnsSe ; 
CREATE TABLE lienEnsSe 
(
    codeEnsemble_ensemble **NOT FOUND** AUTO_INCREMENT NOT NULL, codeSousEnsemble_sous_ensemble **NOT FOUND** NOT NULL, #codeEnsemble_lienEnsSe INT, 
    codeSousEnsemble_lienEnsSe INT, 
    quantite_lienEnsSe INT, PRIMARY KEY (codeEnsemble_ensemble,  codeSousEnsemble_sous_ensemble)
) ENGINE=InnoDB;



ALTER TABLE lienEnsComposant ADD CONSTRAINT FK_lienEnsComposant_codeEnsemble_ensemble FOREIGN KEY (codeEnsemble_ensemble) REFERENCES ensemble (codeEnsemble_ensemble);

ALTER TABLE lienEnsComposant ADD CONSTRAINT 
FK_lienEnsComposant_codeComposant_composant FOREIGN KEY (codeComposant_composant) REFERENCES composant (codeComposant_composant);

 ALTER TABLE lienSeComposant ADD CONSTRAINT FK_lienSeComposant_codeComposant_composant FOREIGN KEY (codeComposant_composant) REFERENCES composant (codeComposant_composant);
 
  ALTER TABLE lienSeComposant ADD CONSTRAINT FK_lienSeComposant_codeSousEnsemble_sous_ensemble FOREIGN KEY (codeSousEnsemble_sous_ensemble) REFERENCES sous_ensemble (codeSousEnsemble_sous_ensemble); 

ALTER TABLE lienEnsSe ADD CONSTRAINT FK_lienEnsSe_codeEnsemble_ensemble FOREIGN KEY (codeEnsemble_ensemble) REFERENCES ensemble (codeEnsemble_ensemble); 

ALTER TABLE lienEnsSe ADD CONSTRAINT FK_lienEnsSe_codeSousEnsemble_sous_ensemble FOREIGN KEY (codeSousEnsemble_sous_ensemble) REFERENCES sous_ensemble (codeSousEnsemble_sous_ensemble); 

```