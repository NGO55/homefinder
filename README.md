# Projet homefinder

## CONTRAINTES

* 1 ou 2 personnes
* 1 site de vente en ligne (peu importe ce qui est vendu)
* 3 zones : anonyme, utilisateur, administrateur
* 4 entités minimum, associées les unes aux autres

** ENVOYER VOS NOMS ET LA DESCRIPTION DE VOTRE PROJET (ENTITES + COLONNES + ASSOCIATION)à emmanuel.ballery@gmail.com **

## SUJET

Nous allons développer une solution de vente immobilière en ligne.

Des utilisateurs peuvent s'inscrire, se connecter et ajouter leurs biens immobiliers à vendre. 

Des administrateurs peuvent tout consulter et tout modifier.

## Nos entités seront :

  * Des utilisateurs (User) : id, email, firstname, lastname, password, role
  * Des biens immobiliers (Estate) : id, title, description, address, zip, city, country, dpe, ges, rooms, bedrooms, surface, groundSurface, created
  * Des types de biens (Type) : id, name
  * Des options immobilières (Option) : id, name, uri (image)
  * Des photos (Photo) : id, name, uri (image)

## Nos associations d'entités seront :
  
  * Un utilisateur aura plusieurs biens immobiliers
  * Un bien immobilier aura un type de bien
  * Plusieurs biens immobiliers auront plusieurs options
  * Un bien immobilier aura plusieurs photos

## L'administrateur pourra :
  
  * CRUD utilisateurs
  * CRUD biens immobiliers
  * CRUD options
  * CRUD photos

## La structure de notre site sera la suivante :

### /page d'accueil, dernières annonces
  * /annonces -> moteur de recherche des annonces
  * /annonces/{id} -> consultation d'une annonce

---------------

### /user -> zone utilisateur
   * / -> dashboard de l'utilisateur
   * /account -> compte de l'utilisateur
   * /pasword -> gestion du mot de passe
   * /estate -> liste des biens de l'utilisateur
   * /estate/create -> créer un bien
   * /estate/{id} -> modifier un bien
   * /estate/{id}/delete -> supprimer un bien
   * /estate/{id}/photo/create -> créer une photo du bien
   * /estate/{id}/photo/delete -> supprimer une photo du bien

---------------

### /admin -> zone administrateur
   * / -> dashboard de l'administration
   * /password -> gestion du mot de passe
   * /user
    * / -> liste des utilisateurs
    * /create -> créer un utilisateur
    * /{id} -> modifier un utilisateur
    * /{id}/delete -> supprimer un utilisateur
      
 ### /estate
   * / -> liste des biens
   * /create -> créer un bien
   * /{id} -> modifier un bien
   * /{id}/delete -> supprimer un bien
   * /{id}/photo -> liste des photos d'un bien
   * /{id}/photo/create -> ajouter une photo à un bien
   * /{id}/photo/{id}/delete -> supprimer une photo d'un bien
 
 ### /type
   * / -> liste des types de bien
   * /create -> créer un type de bien
   * /{id} -> modifier un type de bien
   * /{id}/delete -> supprimer un type de bien
 
 ### /option
   * / -> liste des options des biens
   * /create -> créer une option de bien
   * /{id} -> modifier une option de bien
   * /{id}/delete -> supprimer une option de bien

## Les évolutions possibles :

  * location, vente, échange
  * géolocalisation
  * recherche sur une carte
  * paiement en ligne
