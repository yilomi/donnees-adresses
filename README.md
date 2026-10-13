# Données d'adresses prêtes à l'emploi

Copies d'un géocodeur Nominatim déjà importé (base PostgreSQL), à restaurer
telles quelles pour qu'une installation dispose des adresses et de la
recherche de lieux dès son premier démarrage, sans import de 20 à 60 minutes.

Chaque publication porte :

- `adresses-<pays>-<date>.tar.zst` : le dossier de données du géocodeur ;
- `adresses-<pays>-<date>.tar.zst.sha256` : son empreinte, contrôlée avant toute restauration.

Image attendue : `mediagis/nominatim:4.4` (même version de PostgreSQL que
celle qui a produit la copie). Après la restauration, le géocodeur rattrape
lui-même chaque nuit les changements publiés par OpenStreetMap.

## Licence et attribution

Ces bases sont dérivées d'OpenStreetMap.
© les contributeurs d'OpenStreetMap, données disponibles sous la licence
Open Database License (ODbL) 1.0 : https://www.openstreetmap.org/copyright
Les extraits ont été obtenus auprès de Geofabrik (https://download.geofabrik.de).
