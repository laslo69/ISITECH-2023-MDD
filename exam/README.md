# NB:
 - Le dictionnaire n'est pas dans l'ordre dût à un ajout tardif.

 - Lors de la finalisation du markdown , j'ai constaté une inversion des images MLD et MPD

 - Un fichier SQL est présent dans le dossier, syntaxe MySQL

 - Un fichier texte est présent dans le dossier, pour condenser les infos avant de les traiter

 - Explication dans le chapitre MCD de la démarche pensé de mon côté.




# Dictionnaire

![Alt text](dictionnaire-1.png) 
****************
# MCD
Pour le MCD , je part du principe que:

- 1 ou plusieurs clients peuvent effectué une ou plusieurs réservations
-1 ou plusieurs réservations peuvent être effectué par un client ( ou plusieurs )
****************
-une réservation concerne une ou pluseurs chambre
-une ou plusieurs chambres attribués a une ou plusieurs réservations
****************
-une chambre peut prendre 0 ou `n` services
-`n` service peut etre pris pas 0 ou plusieurs chambres
*****************
-le personnel peut valider une ou plusieurs réservations
- 0 ou plusieurs réservations peuvent être valider par le personnel
****************
-le personnel entretien 1 ou plusieurs chambres
- 1 ou plusieurs chambres peuvent être entretenue par 1 ou plusieurs personnel
*****************
- 1 ou plusieurs personnels peut gérer le stock
- 1 élément ou plusieurs du stock peuvent être géré par 1 ou plusieurs personnels
******************
- 1 ou plusieurs personnel peut produire des analyses
- 1 ou plusieurs analyses peuvent être produit par le personnel
*****************
- 1 ou plusieurs personnel peut contrôler les finances
- 1 ou plusieurs finances peuvent être controlé par le personnel

![Alt text](MCD-1.png) 
****************
# MLD

Toutes les relations deviennent des entités à part entière.

![Alt text](MPD-1.png)

****************
# MPD

![Alt text](MLD-1.png) 
****************
