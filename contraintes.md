# Contraintes

Liste des contraintes ne pouvant pas être représenté par le schéma de la base de données seulement. Donc les contraintes liées aux cardianlités ne seront pas traitées dans ce document.

## Utilisateur

* Un utilisateur doit avoir un mot de passe comportant au moins une minuscule, majuscule, un chiffre, et un symbole. Le tout en ayant une longueur minimum de 8 caractères;
* Le nom d'un utilisateur doit forcément comporter des lettres, et éventuellement des chiffres;
* L'adresse email d'un utilisateur doit être valide;

## Application

* Le prix d'une application ne peut être négatif;
* Le nom d'une application peut comporter des lettres ou des chiffres;
* Le nombre de téléchargement d'une application ne peut être négatif;

## Editeurs

* Le chiffre d'affaires d'un éditeur ne peut être négatif;
* Le nom d'un éditeur doit forcément comporter des lettres, et éventuellement des chiffres;

## Avis

* La note d'un avis doit être comprise entre 0 et 5 inclus;

## Licence

* Il ne peut pas y avoir deux licences actives sur le même produit;
* La date de fin ne peut être inférieure à la date de début;

## Suspensions

* Il ne peut pas avoir 2 suspensions actives simultanément pour un éditeur;
* La date de fin ne peut être inférieure à la date de début;
