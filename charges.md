# Cahier des charges

## Description générale

L'application que va servir la base de données est un marketplace d'application. C'est une plateforme qui permet à des éditeurs d'y publier des applications pour que des utilisateurs puissent les acheter ou les télécharger.

Pour vendre des applications, un utilisateur doit ouvrir un compte éditeur. Ce même compte peut également être fermé ultérieurement. Pour publier une application, un store doit obligatoirement fournir une distribution initiale, le cas échéant, l'application sera créée, mais pas visible publiquement tant que cette distribution n'est pas fournie. En effet, il n'est pas possible de vendre d'applications "vides".

## Besoins

### Gestion

La base de données doit pouvoir gérer la publication, la mise à jour, les achats et la suppression d'applications. La création, suppression et modifications des utilisateurs et des comptes éditeurs doit également être assurée par la base de données.

L'accès aux données confidentielles doit être contrôlée et limitée.

### Historique

Dans l'objectif de garantir une certaine intégrité des données et un historique cohérent, les données jugées importantes peuvent ne pas être supprimée mais simplement marquée comme supprimée.

Par exemple les données relatives à des achats ne peuvent pas être effacées de la base de données car elles représentent des transferts d'argent. À la place elles seront masquées en quelques sortes.

## Descriptions détaillées

### Utilisateurs

Un utilisateur est un acteur qui achète des applications sur le marché et les évalue éventuellement par la forme de notes sur 5 accompagnées de commentaires rédigés. Il est caractérisé par un nom, une adresse mail, un mot de passe, la date de création de son compte, et un indicateur de validation de son adresse mail.

Quand un utilisateur achète une application, cet achat est symbolisé par une licence. Un utilisateur peut avoir plusieurs licences. Cependant, certaines applications ont une restriction sur l'âge. Ça signifie que l'achat est confirmé seulement si l'utilisateur à l'âge attendu par la restriction.

Chaque utilisateur peut ajouter une ou plusieurs applications dans sa liste de souhaits pour la mettre de côté dans le but de l'acheter plus tard.

#### Avis

Comme mentionné plus haut, un utilisateur peut évaluer une application via un avis. Un avis est constitué d'une note sur 5, d'une date de publication et de suppression, d'un titre et optionnellement de son contenu. Un avis ne peut être rédigé que par un utilisateur. Mais un utilisateur peut rédiger plusieurs avis, tant qu'ils concernent des applications différentes.

---

### Store

Un store est un acteur qui vend des applications sur le marché. Il appartient à un utilisateur qui peut l'ouvrir pour une durée déterminée ou non. Ceci dit, la durée de vie d'un store ne peut pas dépasser celle de son gérant. Un store peut être suivi par des utilisateurs, ce qui les fait monter dans les recommandations.

Pour qu'un utilisateur puisse ouvrir il store, il doit avoir atteint l'âge de majorité définit dans son pays.

Un store est caractérisé par un nom, une adresse email de contact, et du pays où il est établit.

---

### Applications

C'est le bien (ou service pour un SaaS) vendu sur le marché par des éditeurs pour des utilisateurs. Une application est caractérisée par un nom, sa description, sa date de publication et de suppression, la catégorie à laquelle elle appartient, son prix de vente et un indicateur d'achats intégrés. Elle dispose également d'un indicateur permettant sa visibilité publique ou non.

Le rôle de ce concept est avant tout de contenir des informations décrivant une application. Il ne représente pas l'application téléchargeable, c'est le rôle des **distributions**.

Le prix par défaut d'une application est *0.00€* si elle est gratuite. Une application n'a pas forcément de description.

Chaque application doit supporter au moins une plateforme du marché. Une application peut être concernée par plusieurs licences. Et chaque application ne peut avoir qu'un avis par utilisateur.

#### Distribution

Une distribution représente la publication d'une nouvelle version de l'application pour toutes les plateformes que cette dernière supporte. C'est ce que l'utilisateur sera amené à télécharger une fois l'application achetée, ou obtenue dans le cas où elle est gratuite.

Elles sont caractérisés par un numéro unique, leur date de publication, le nombre de téléchargement. Pour une application donné, le numéro de ses distribution doit être croissant si on trie ces dernières par date croissante.

#### Plateforme

Il s'agit tout simplement d'une plateforme pour laquelle une application a été développée et est commercialisé. Une plateforme est caractérisée par son nom. De plus, une plateforme peut concerner aucune ou plusieurs applications.
