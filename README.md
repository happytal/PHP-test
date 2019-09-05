# PHP-test
Test PHP pour les candidats

# Enoncé
Créer une API permettant de :

A. Lister les images d'une page web à partir d'une URL donnée.

| Verbe  | Chemin | Paramètres                                         |
|--------|--------|----------------------------------------------------|
| GET    | /scan/images | ?url=xxx                                     |

- Pour chaque image trouvée, l'API devra fournir les informations suivantes:

| Noms   | Types  | Descriptions                                         |
|--------|--------|------------------------------------------------------|
| url    | String | Url de l'image                                       |
| width  | Number | Largeur de l'image                                   |
| height | Number | Hauteur de l'image                                   |
| size   | Number | Taille de l'image (octets, ex: *128000*)             |

B. Récupérer toutes les meta-données de la page :

- La liste des metas : https://gist.github.com/kevinSuttle/1997924

| Verbe  | Chemin | Paramètres                                         |
|--------|--------|----------------------------------------------------|
| GET    | /scan/metas | ?url=xxx                                      |

Pour chaque meta trouvé, l'API devra fournir les informations suivantes:

| Noms   | Types  | Descriptions                                         |
|--------|--------|------------------------------------------------------|
| name   | String | Nom du meta                                          |
| value  | String | Données du meta                                      |

## Contraintes
- Les retours de l'API devront être au format `JSON`.
- Protéger l'API avec une authentification basique.
- Prévoir un système de cache pour stocker les données trouvées.
- Prévoir des tests avec `PHPUnit`.
