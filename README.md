# METROPOLIS — World Transit

Prototype jouable de gestion d'un réseau de transport urbain, avec une direction artistique minimaliste : traits, points et rectangles.

## Lancer le jeu

Ouvre simplement [index.html](./index.html) dans un navigateur récent. Aucune installation ni dépendance externe n'est nécessaire.

## Prototype 0.1

- Carte schématique de Paris.
- Réseau initial avec huit stations et une ligne.
- Construction de stations et de lignes.
- Liaison de stations et sélection sur la carte.
- Dépôts construits séparément des stations.
- Achat de trains avec capacité de dépôt.
- Simulation journalière simplifiée : voyageurs, revenus, dépenses et satisfaction.
- Sauvegarde locale dans le navigateur via `localStorage`.

## Commandes

- **Réseau** : consulter l'état de l'exploitation et avancer d'une journée.
- **Construire** : ajouter des stations, créer une ligne et relier des stations.
- **Trains** : acheter du matériel roulant.
- **Dépôts** : construire des dépôts indépendants.
- **Gestion** : consulter les finances et sauvegarder la partie.

## État du développement

Cette version est un premier prototype jouable. La carte de Paris est volontairement schématique : elle ne prétend pas encore représenter précisément la géographie ou les tracés réels. Les prochaines étapes sont le vrai fond cartographique, les données ouvertes correctement attribuées, le déplacement continu des trains, une simulation de trajets plus fine, puis la progression vers d'autres villes.

## Publication avec GitHub Pages

Le workflow `.github/workflows/pages.yml` publie automatiquement le contenu du dépôt sur GitHub Pages à chaque push sur `main`. Dans **Settings → Pages**, sélectionne **GitHub Actions** comme source de déploiement si ce n'est pas déjà fait.

## Licence et données

Le code de ce prototype est fourni sans données cartographiques tierces embarquées. Lors de l'intégration future d'OpenStreetMap ou de jeux de données de transport, leurs licences et obligations d'attribution seront documentées ici.


## Données géographiques de Paris (version 0.2)

La carte utilise désormais :
- les limites administratives de la commune de Paris via l'API officielle geo.api.gouv.fr ;
- les gares et stations par ligne d'Île-de-France Mobilités : `emplacement-des-gares-idf` ;
- les tracés des lignes d'Île-de-France Mobilités : `traces-des-lignes-de-transport-en-commun-idfm` ;
- le fond cartographique OpenStreetMap.

La vue filtre les stations de métro, RER A à E et tramway situées dans les limites de Paris. Les tracés des lignes sont ceux publiés par IDFM et restent visibles sur leur parcours régional autour de Paris. Les stations desservies par plusieurs lignes sont regroupées pour afficher leurs correspondances.

Les jeux de données IDFM sont publiés sous licence ODbL. Attribution affichée dans la carte : « © Île-de-France Mobilités ». Le fond de carte porte l'attribution © OpenStreetMap.
