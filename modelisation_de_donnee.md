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

