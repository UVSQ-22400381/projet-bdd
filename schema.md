# Schéma Relationel

Réécriture du diagramme en schéma relationnel:

Utilisateur(**id**, pays, nom, mot_de_passe, email, date_création, email_valide, date_naissance)
Store(**id**, email, pays, date_ouverture, date_fermeture, nom, <ins>id_gestionnaire</ins>)
Plateforme(**id**, libelle)
Application(**id**, nom, description, categorie, public, date_pub, prix, achat_integre, <ins>id_store</ins>)
Distribution(**num**, changelog, date_pub, public, telechargement, <ins>id_application</ins>)
Restriction(**num**, limite, <ins>id_application</ins>)

Suivre(**id**, <ins>id_utilisateur</ins>, <ins>id_store</ins>)
Evaluer(**id**, <ins>id_utilisateur</ins>, <ins>id_application</ins>, titre, date_pub, note, contenu)
Acheter(**id**, date_achat, rembourse, date_fin, <ins>id_utilisateur</ins>, <ins>id_application</ins>, <ins>id_plateforme</ins>)
Supporter(**id**, <ins>id_application</ins>, <ins>id_plateforme</ins>)

