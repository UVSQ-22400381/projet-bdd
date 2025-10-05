# Définition des besoins

## Description de l'appli

L'application que va servir la base de données est un marketplace d'application. C'est une plateforme qui permet à des éditeurs d'y publier des applications pour que des utilisateurs puissent les acheter ou les télécharger.

## Besoins

### Utilisateurs

Un utilisateur est un acteur qui achète des applications sur le marché et les évalue éventuellement par la forme de notes sur 5 accompagnées de commentaires rédigés. Il est caractérisé par un nom, une adresse mail, un mot de passe, la date de création de son compte, et un indicateur de validation de son adresse mail.

Chaque utilisateur peut ajouter une ou plusieurs applications dans sa liste de souhaits pour la mettre de côté dans le but de l'acheter plus tard.

#### Avis

Comme mentionné plus haut, un utilisateur peut évaluer une application via un avis. Un avis est constitué d'une note, d'une date de publication, d'un titre et optionnellement de son contenu.

---

### Editeurs

Un éditeur est l'acteur qui publie des applications sur le marché et rédige des articles sur ces applications. Il est caractérisé par un nom, une date d'établissement, un pays et son chiffre d'affaire généré par ses ventes d'application.

Dans le cadre de la modération sur le marché, un éditeur peut se trouver suspendu pour une durée déterminée ou non pour divers motifs.

#### Suspensions

Une suspension définit la durée de suspension d'un éditeur et le motif pour lequel il est suspendu. La durée peut être finie ou non. Elle est caractérisé par un motif, une date de début et optionnellement une date de fin. Une suspension ne concerne seulement un éditeur, mais un éditeur peut être suspendu plusieurs fois, dans que les précédentes suspensions ont pris fin.

Le motif est d'ailleurs indiqué par un code qui renvoie vers la description textuelle du motif d'exclusion.

#### Articles

Un article représente du contenu rédigé par un éditeur au sujet d'une des applications que ce dernier vend sur le marché. Ces articles peuvent annoncer des nouveautés à venir ou avertir d'une maintenance imminente. Un article est caractérisé par un titre, son contenu, sa date de publication, et un indicateur définissant sa visibilité publique ou non. Un article ne peut avoir qu'un seul auteur, alors qu'un auteur peut en rédiger aucun ou plusieurs.

---

### Applications

Une application est caractérisé par un nom, sa description, sa date de publication, la cétagorie à laquelle elle appartient, son prix de vente, sa version courante et son nombre de téléchargement. Elle dispose également d'un indicateur de si elle est visible publiquement ou non.

Le prix par défaut d'une application est *0.00€* si elle est gratuite. Une application n'a pas forcément de description.

Enfin, chaque application supporte un ensemble de plateformes.

#### Version

Comme les applications ont amenées à évoluer dans le temps, elles ont plusieurs versions, cependant elles ont une seule version courante, les autres servant d'historique. Une version est caractérisé par son numéro unique, sa date de publication et éventuellement un changelog.

---

### Licence

Une licence représente la preuve d'achat d'une application par un utilisateur et lui confère les droits d'utilisation le temps d'une période déterminée ou non. Elle est caractérisé par une date de début et de fin.

Une licence associe un utilisateur, une application avec l'environnement cible de l'application.

#### Environnement

Un environnement englobe plusieurs plateformes par grande catégories, par exemple l'environnement "Mobile" concernerait les plateformes iOS et Android par exemple.
