# Predictor

Logiciel d'analyse de données et de prédiction sur un monde réel virtualisé, développé par **F.S.M Game House**.

Version actuelle : **v1.1**

## Ce que fait Predictor

1. **Collecte** : recherche de n'importe quel lieu dans le monde (ville, quartier, adresse), puis carte OpenStreetMap de la zone avec bascule automatique sur des serveurs de secours (collecte directe, Overpass Turbo, GeoJSON ou fichier régional `.osm.pbf` de Geofabrik) et prévisions météo Open-Meteo.
2. **Enrichissement** : démographie INSEE (geo.api.gouv.fr), météo des 92 derniers jours, précision météo mesurée (prévisions passées comparées au réel), comptages réels vélo et trafic (open data Ville de Paris).
3. **Monde virtualisé** : rues et lieux redessinés, classés en 9 familles, sur fond Plan, Satellite ou Mixte (photos aériennes IGN en France, Esri World Imagery ailleurs).
4. **Analyse** : densité, services essentiels, équipements publics, population, réseau de voies, lignes de transport (intervalles OSM ou estimés).
5. **Danger probable** : probabilité relative d'incidents par secteur (accidents de la route BAAC 2022-2024 géolocalisés, événements Actu17 localisés, facteurs de terrain), jour ou nuit, avec contrôle sur les accidents de 2024 ; délinquance enregistrée de la commune (SSMSI).
6. **Événements en cours** : lecture du flux d'Actu17, classement par type et gravité, localisation à la rue ou à la commune (geo.api.gouv.fr, Base Adresse Nationale), affichage sur la carte. Aucun nom de personne n'est relevé.
7. **Prédictions** : météo 7 jours avec fiabilité mesurée, fréquentation par heure et par jour, modèle calé sur mesures réelles et testé sur des jours qu'il n'a jamais vus, effet mesuré de la pluie, suivi de la précision des prévisions dans le temps.
8. **Mémoire en ligne** et **agent Claude** : disponibles quand Predictor est ouvert dans Claude. La version web exporte des paquets de zone que la version Claude importe.

## Utilisation

Ouvrir la page web, taper une adresse précise ou un lieu, puis « Charger la zone » : Predictor localise l'adresse et télécharge automatiquement la carte, la météo et les données réelles. Les prédictions s'affichent d'abord en bref, en phrases simples avec leur fiabilité, puis en détail. Hors de Claude, la mémoire en ligne et l'agent Claude sont désactivés ; le suivi de précision est conservé sur l'appareil.

## Robot Actu17

Le fichier `.github/workflows/actu17.yml` recopie toutes les heures le flux RSS public d'Actu17 dans `data/`, car le site n'autorise pas la lecture directe depuis une autre page web. Predictor lit cette copie automatiquement.

## Sources de données

- OpenStreetMap © contributeurs OpenStreetMap, licence ODbL
- Open-Meteo, licence CC BY 4.0
- INSEE via geo.api.gouv.fr, Licence Ouverte
- Ville de Paris, open data (comptages vélo et routiers), licence ODbL
- Extraits régionaux : Geofabrik
- Accidents corporels de la circulation (BAAC, ONISR) et délinquance enregistrée (SSMSI) via data.gouv.fr, Licence Ouverte
- Actualité : flux RSS public d'Actu17 (titres, liens et extraits, lien vers l'article d'origine)
- Photos aériennes : IGN Géoplateforme (Licence Ouverte) ; Esri World Imagery (© Esri, Maxar, Earthstar Geographics)

Predictor ne collecte ni n'analyse aucune donnée sur des personnes.
