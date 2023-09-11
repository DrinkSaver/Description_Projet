# Drink Saver Project
## Description
Drink Saver est un site web / application mobile qui a pour fonctionnalité principale de rechercher une boisson et de voir le prix auquel les bars à proximité proposent ladite boisson. Permettant ainsi de faire des économies.
Les utilisateurs connectés pourront eux-mêmes encoder les prix des boissons, voire les différents évènements prévus comme des concours, happy Hour, barathon, etc… Noté et commenté les bars et participé à des concours.
Cette application a été demandée par un « Client » à qui il faudra soumettre régulièrement l’avancement du projet et toute modification que l’on souhaite apporter aux Users Story qui seront décrits plus tard dans ce document.
Le « Client » sera celui qui prendra la décision finale.

## Technique
Des exemples du projet existent déjà avec des parties de code qui peuvent être réutilisées, mais il est préférable de recommencer le projet.
Nom de domaine : drinksaver.be 
Hébergement : OVH perso
Base de données : MySQL (OVH Web Cloud Databases, 8Go) 
Front :  expo with React native, Scss, HTML.
Back : API (exemple d’api php déjà présent mais à refaire) avec CRUD DB, clé privée et envoie de mail. La sécurité est très importante ici.

## Equipe
1 Frontend (styles, fonctionnalité, appel api).
1 Fullstack (Création de maquettes, de l’api et de la DB).
1 backend ? (Aide pour la partie BD et l’api). 
Users Story

## US 1 :  Register
L’utilisateur doit être capable de s’enregistrer via un formulaire, les informations seront envoyées (chiffrer si nécessaire) à la DB. Le formulaire doit posséder les champs suivants :
-	Username (unique)
-	Mot de passe (+ vérification)
-	Adresse mail.
-	Possibilité de s’enregistrer avec un service tiers (Google, Facebook, Apple et/ou autre).
Une confirmation d’inscription sera envoyée par mail (le mail d’envoi sera créé à partir de l’hébergement).



## US 2 : Login
L’utilisateur, une fois enregistrer (US 1), sera capable de se connecter avec son username ou email et son mot de passe ou via un service tiers (Google, Facebook, Apple et/ou autre).



## US 3 : CRUD Profile
L’utilisateur doit pouvoir accéder à ses informations personnelles via une page de profile qui lui permettra de les modifier. Il doit aussi avoir la possibilité de supprimer son compte. En cas de changement d’adresse mail, un mail de confirmation sera envoyé

## US 4 : Sélection de produits
 L’utilisateur peut sélectionner un produit dans la liste des produits présents en DB, L’utilisateur peut écrire le nom du produit et une autocomplétion est présente pour l’aider. (Input select with datalist ?).
Exemple (Selectize.js) :
![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/b6ac7562-f3f1-455a-898f-d51df15d90ab)
![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/91e1bc6f-3647-457e-9230-0d804cc26aab)


 
## US 5 : Affichage des prix et des informations relative aux bars
Une fois que l’utilisateur a sélectionné un produit, les informations des bars et le prix auquel ils proposent le produit est affiché.
Les informations à afficher :
-	Nom du bar
-	Distance actuelle entre l’utilisateur et le bar (algorithme déjà codé).
-	Le prix du produit sélectionner dans ce bar
-	 ? Image de l’entrée 
-	Intérieur/extérieur
-	Toilettes, payante ou non
-	Coin fumeur
-	Wi-Fi
-	Ouvert ? + heure de fermeture
-	Minimum par carte 
-	 ? Autre
Exemple :
![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/63f5f389-0664-45c2-8977-e111c0a4640d)

 
## US 6 : Filtre des bars
Un système de tris/filtre doit être proposé à l’utilisateur lui permettant de réduire la liste des résultats.
Option de Filtre :
-	Toilettes
-	Zone fumeurs
-	Ouvert
-	Intérieur
-	 ? Autre

Exemple :


![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/be5890d1-e0b0-4368-82ce-abf95bbe1f91)



## ? US 6-2 : Tris des bars
L’utilisateur doit pouvoir choisir dans quel ordre les bars seront affichés
Option de tris :
-	Prix du produit
-	Distance du bar
-	 ? Nom du bar
## US 7 : Redirection google map
Lorsque l’utilisateur clique sur un bar, cela ouvre la page du bar sur google map pour pouvoir s’y rendre facilement.
Exemple :

![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/7aa74b35-1fd8-4118-982e-c36b6907b062)
=>
![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/0227f3e6-ee9d-429e-98ed-b7b2336a32cf)



## US 8 : Menu principal
Un menu composé d’icones doit permettre la navigation entre les différentes pages
Les pages :
-	Home/ Accueil 
-	Event
-	Games
-	Profile/Connection/register
-	 ??? Tourner des bars

Exemple : 
![image](https://github.com/DrinkSaver/Description_Projet/assets/55028792/7bf0cb16-b162-468b-8c1f-b5400db0bded)

 
##  9 : Soumission prix 
L’utilisateur peut soumettre des prix pour les boissons des bars
Il faudra un système de vérification automatique, exemple quand 4 utilisateurs différents donnent le même prix pour une boisson d’un bar, ce prix est validé et modifier, quand le prix est validé, les utilisateurs qui ont soumis le prix reçoivent des Bacchus.

## US 10 : Game Page
Une page permettant de voir / débloquer des règles de jeux à partir de points (Bacchus) que possède l’utilisateur.
La page doit afficher la liste des jeux (pdf ?), une partie de ceux-ci sont déjà débloqué et l’autre nécessite de dépenser des points pour y avoir accès.

## US 10-2 : Filtre
L’utilisateur peut filtrer les jeux en fonction du matériel requis pour jouer au jeu.
Option de filtre :
-	Dés
-	Cartes
-	Balle de ping-pong
-	Connexion internet
-	Support d’écriture
-	 ? Autres

## US 11 : Event Page
Une page permettant de voir les différents évènements à proximité triée en plusieurs catégories :
-	Happy Hours
-	Social
-	Jeux Concours
-	 ? Autres
## ? US 11-2 : Types of évents
Les différents types d’évents :
-	Textuel : uniquement un texte descriptif de l’évènement.
-	Joignable : l’utilisateur peut rejoindre l’évènement et voir le nombre de participants.
-	Questionnaire : l’utilisateur répond à un questionnaire pour participer à un concours (gagne des prix ou des Bacchus).
-	Premuim : l’utilisateur doit dépenser des Bacchus pour pouvoir participer à l’évènement/concours.
## ? US 12 : Forum 
Les utilisateurs peuvent mettre des commentaires et des notes aux bars

## ? US 13 : Shop 
L’utilisateur peut acheter des Bacchus via Paypal, Bancontact, Apple pay, etc…

Trigger bd pour verif push prix.


