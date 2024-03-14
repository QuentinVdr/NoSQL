# NoSQL Course

## Exo

### TP 1

Mettez au point un schéma relationnel pour stocker des données
de films qui comprendraient :

- le nom du film
- l'année
- le pays
- le réalisateur (nom, prénom, date de naissance)
- les acteurs (nom, prénom, date de naissance, rôle)
- le de film
- le résumé

```mermaid
classDiagram

  class Film {
    id_film : Int
    nom_film : String
    annee_sortie : Int
    pays_origine : String
    id_realisateur : Int
    type_film : String
    resume : Text
  }

  class Realisateur {
    id_realisateur : Int
    nom_realisateur : String
    prenom_realisateur : String
    date_naissance_realisateur : Date
  }

  class Acteur {
    id_acteur : Int
    nom_acteur : String
    prenom_acteur : String
    date_naissance_acteur : Date
  }

  class Role {
    id_film : Int
    id_acteur : Int
    nom_role : String
  }

  Film -- Realisateur
  Film -- Role
  Role -- Acteur
```
