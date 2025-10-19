# Contraintes

Liste des contraintes ne pouvant pas être représenté par le schéma de la base de données seulement. Donc les contraintes liées aux cardianlités ne seront pas traitées dans ce document.

## UTILISATEUR

- Un utilisateur doit avoir un mot de passe comportant au moins une minuscule, majuscule, un chiffre, et un symbole. Le tout en ayant une longueur minimum de 8 caractères.
- Si l’utilisateur a acheté une application X, il doit être remboursé de l’application X avant de racheter à nouveau l’application X.
- L'utilisateur n’a pas accès aux applications dont l’âge minimum accepté est supérieur à son âge.

## APPLICATION

- Le prix d'une application ne peut être négatif.
- La date de suppression d'une application doit être supérieure à sa date de publication.
- Une application visible publiquement doit avoir une date de publication valide non nulle.
- Pour un store donné, plusieurs applications ne peuvent pas avoir le même nom.

## STORE

- La date de fermeture du store doit être supérieure à la date d’ouverture.

## PLATEFORME

- Ne pas utiliser le même libellé pour une autre plateforme.

## SUIVRE

- Un utilisateur ne peut pas suivre son propre store.

## DISTRIBUTION

- Le nombre de téléchargements doit être supérieur ou égal à 0.

## EVALUER

- La note doit être comprise entre 0 et 5 inclus.
- Le titre d'un avis doit être associé du contenu, et le contenu doit avoir un titre.
- Un utilisateur ne peut publier qu'un seul avis par application.

## ACHETER

- La date de fin doit être supérieure à la date d’achat.
- Si l’achat est remboursé, la date de fin doit être renseignée.
<!-- redondant ? -->
- On ne peut pas acheter la même application si l’utilisateur n’a pas reçu de remboursement ou si l’application est déjà achetée.
