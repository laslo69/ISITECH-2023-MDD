# 1. utilisation git

``` bash
git init
``` 
initialise un depot git vide

**********************

``` bash
git status
```
Permet de consulter l'état d'un dépot git

**********************

``` bash
git add .
``` 
Permet d'ajouter un fichier au fichier suivi par le depot

**********************

``` bash
git commit -m "message du commmit"
```
l'option -m permet d'ajouter un message au commit
Lors du premier commit , il sera nécessaire de renseigner une addesse mail et un nom d'utilisateur pour le tracking

# 2. Merise

Merise est une méthode de modélisation de données.Elle permet de représenter les données d'un système d'informations.
Merise est un acronyme de : Méthode d'Etude et de Réalisation Informatique pour les Systèmes d'Entreprise.

Présentation générale
Cette méthode se caractèrise par trois point clés:

- une approche dite systèmique:
on transforme les processus de l'entreprise en système d'information.

- une séparation des données et des traitements

- une approche nivelée

### l'approche systèmique

![Alt text](image.png)

le systeme de pilotage:

- Il est l'ensemble des acteurs qui vont **piloter** le système d'informations

le système d'informations:

- il est compose de l'ensemble des acteurs qui vont **utiliser** le système d'informations

le système opérant:

- il est composé de l'ensemble des acteurs qui vont **produire** les données du système d'informations

### La separation des donnees et des traitements

La séparation des données et des traitements permet de séparé les données du système d'information et les traitements effectués sur ces données.

cette démarche se fait en 3 étapes:

- L'analyse des flux: On analyse les flux d'informations entre les acteurs du système d'information et les acteurs du système opérant.

- L'étude des documents interne (factures, bon de livraison, etc...)

- L'étude des documents en externe (fournisseurs, clients, etc...)

Les différents types d'informations:

- Les infos de bases ou élémentaires : Ce sont les données de base du systèmes d'information

- Les informations calculées : ce sont les données calculées à partir des données de base

- Les traitements ou les fonctions : Ce sont les traitements effectués sur les données de base pour obtenir les données calculées

En résumé: Vous devez identifiées les données et les traitements effectués sur ces données

### L'approche nivelée

Pour effectuer la conception d'un SI, on va utiliser une approche nivelée. Cette approche se compose de 4 niveaux:

- Le niveau conceptuel
- Le niveau organisationnel
- Le niveau logique
- Le niveau physique

#### Le niveau conceptuel

Le niveau conceptuel permet de modéliser les données de l'entreprise.
On va utiliser le modèle conceptuel de données (MCD) pour modéliser les données de l'entreprise, et le MCT pour modéliser les traitements effectués sur ces données.

#### Le niveau organisationnel

Le niveau organisationnel va permettre d'intrégrer à l'analyse précédente toutes les notions de temporalité, de chronologie des opérations, de contraintes géographiques, niveau d'accès. On va utiliser le modele organisationnel des traaitements (MOT) et le modéle organisationnel des données (MOD) pour modéliser les traitements de l'entreprise.

En résumé on se pose les questions suivantes à partir des données recueillis au niveau conceptuel :

- **Quand** les traitements sont effectués ?
- **Où** les traitements sont-ils effectués ?
- Par **qui** les traitements sont effectués ?

#### Le niveau logique

Le niveau logique va permettre de modéliser les données de l'entreprise en utilisant le modèle logique de données (MLD) et les traitements de l'entreprise en utilisant le modèle logique des traitements (MLT)

le MLD est indépendant des langages de programmations des SGBD

On répon à la question suivantes : **Avec quoi** les traitements sont-ils effectués?

#### Le niveau physique

Il s'agit de l'organisation `réelle` des données. On va utiliser le modèle physique de données (MPD) et le modèle des traitements (MPT)

Ici, on apporte les solutions techniques de stockage des données et de traitement des données.

On répond à la question: **Comment** les traitements sont-ils effectués.

#### Résumé: Les 4 niveaux de Merise

![Alt text](image-1.png)

### Des données aux dépendances fonctionnelles

Pour être intégrées dans un système d'information, les données doivent être triées et organisées. On va souvent tenter de les classer par type de données : 

- chaines de caractères: format texte
- type alphanumérique: format texte
- le type numérique: entier,float.
- le type date (date, datetime, timestamp)
- le logique ou boolean (true,false)


création d'un dictionnaire de données

![Alt text](image-2.png)
![Alt text](image-3.png)

### Les dépendances fonctionnelles

une dépendence fonctionnelle est une relation entre deux attributs d'une tablee. Elle permet de définir une relation de dépendance entre deux attributs d'une table.

LE role d'une dépendence fonctionelle est de permettre de définir une relation de dépendence entre deux attributs d'une table : une donnée A dépend fonctionnellement d'une donnée B lorsque la valeur de B détermine la valeur de A

Pour formaliser une dépendance fonctionnelle on utilise la notation suivante :
`Numéro adhérent (nom, prenom, code postal, ville, telephone, date adhesion, mail)`

La partie gauche ( numéro adhérent) est la `source` de la dépendance fonctionnelle.
La partie droite désigne le `but` de la dépendance.

### Les dépendances fonctionnelles composées

Si une dépendance fonctionnelle qui fait intervenir plus de deux  attributs, on parle de dépendance fonctionnelle composées.

Exemple: Pour connaitre le temps d'un coureur sur une étape donnée , il nous faut son numéro ou son nom ainsi que le nom ou le numéro de l'étape

### Les dépendances fonctionnelles élémentaires

Une dépendance A -> B est élémentaire s'il n'existe pas une donnée C, sous-ensemble de A, décrivant une dépendance fonctionnelle type c -> B.

Exemple:
- RefProduit -> libelleProduit
- NumCommande RefProduit -> QuantitéCommande
- <strike>NumCommande RefProduit -> DesignationProduit</strike>

### Dependance fonctionnelle élémentaire directe

On dit que la dépendence fonctionnelle A -> B est directe s'il n'existe aucun attribut C tel que l'on puisse avoir A -> C et C -> B. En d'autre termes, cela signifie que la dépendence fonctionnelle entre A et B ne peut pas être obtenue par transitivité.

exemple:
- RefPromo -> NumApprenant
- NumApprenant -> NomApprenant
- RefPromo -> NomApprenant

********************************************************

le but de l'exercise est d'élaborer un MCD à partir d'un dictionnaire de données

Ici on va introduire les notions d'entité, de relation et de propriétés.

Les propriétés sont les informations de bases d'un SI

### Les entités sont les objets du SI

![Alt text](image-8.png)

QUelques définitions:
- entités fortes: une entité qui ne dépend pas d'une autre entité pour exister.
- entités faible: une entité qui dépend d'une autre entité pour exister.

### Les relations 

![Alt text](image-9.png) 


#### Les relations "porteuses"

Une relation est dite porteuse si elle posséde des propriétés.



#### Les relations reflexives

Une relation est dite réfléxives si elle reslie une entité à elle même.


**Les cardinalités** : Elles permettent de définir le nombre d'occurences d'une entité par rapport à une autre entité dans le cadre d'une relation.

![Alt text](image-13.png)


### Les contraintes d'intégrité fonctionnelle (CIF)

Définition: Une CIF est définie par le fait qu'une des entités de l'association est complétement déterminée par la connaissance d'une ou de plusieurs entités participant à l'association.

Exemple:
Une salle peut contenir 0 ou plusieurs ordinateurs.Un ordinateur exist dans une et une seule salle.
Dans ce type de relation, une CIF exsite si on a une cardinalité 1,1 


Quelques règles de conception : 

- Toutes entités doit avoir un identifiant
- Toutes les propriétés dépendent fonctionnellement de l'identifiant
- Le nom d'une propriété ne doit apparaitre qu'une seule fois dans le MCD : Si vous avez une entité professeur et un entité élève, vous ne pouvez pas avoir une propriété nom dans les deux entités, il faut donc renommer la propriété nom de l 'entité professeur en nomProfesseur par exemple.
- Les propriétés issues d'un calcul ne doivent pas apparaitre ans le MCD.

### Modèles logiques de données

Le MLD est la suite du processus Merise, on se rapproche un peu plus de la base de données du MCD suivant.

#### cas simple

Partons du MCD suivant:

ajout image 19

Nous arrivons au MLD suivant

ajout image 20

L'`entité` qui posséde la cardinalité 1,1 ou 0,1 absorde l'indentifiant de l'entité la plus forte (0,n ou 1,n).
Cet identifiant devient alors une clé étrangére.



#### cas (0,n),(0,n) ou (1,n),(1,n)

Partons du MCD suivant

ajout image 21

Dans le cas ou la `cardinalité max` est n des deux cotés, on crée une entité intermédiaire qui va contenir les deux clés étrangéres des deux entités.

ajout image 22

Continuons avec le MCD suivant:

ajout image 23

On obtient le MLD suivant en suivant la même logique

ajout image 24

#### cas d'une relation reflexive

Partons du MCD suivant :

ajout image 25

ajout image 26

### Régle de passagege du MCD au MLD




### Sujet TP/TD MCD jour 1

![Alt text](image-14.png)
![Alt text](image-5.png)
![Alt text](image-6.png)
![Alt text](image-7.png)