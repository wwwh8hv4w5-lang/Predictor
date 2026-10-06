# Predictor

Logiciel d'analyse de données et de prédiction sur un monde réel virtualisé, développé par **F.S.M Game House**.

Version actuelle : **v0.9**

## Ce que fait Predictor

1. **Collecte** : recherche de n'importe quel lieu dans le monde (ville, quartier, adresse), puis carte OpenStreetMap de la zone avec bascule automatique sur des serveurs de secours (collecte directe, Overpass Turbo, GeoJSON ou fichier régional `.osm.pbf` de Geofabrik) et prévisions météo Open-Meteo.
2. **Enrichissement** : démographie INSEE (geo.api.gouv.fr), météo des 92 derniers jours, précision météo mesurée (prévisions passées comparées au réel), comptages réels vélo et trafic (open data Ville de Paris).
3. **Monde virtualisé** : rues et lieux redessinés, classés en 9 familles, sur fond Plan, Satellite ou Mixte (photos aériennes IGN en France, Esri World Imagery ailleurs).
4. **Analyse** : densité, services essentiels, équipements publics, population, réseau de voies, lignes de transport (intervalles OSM ou estimés).
5. **Prédictions** : météo 7 jours avec fiabilité mesurée, fréquentation par heure et par jour, modèle calé sur mesures réelles et testé sur des jours qu'il n'a jamais vus, effet mesuré de la pluie, suivi de la précision des prévisions dans le temps.
6. **Mémoire en ligne** et **agent Claude** : disponibles quand Predictor est ouvert dans Claude. La version web exporte des paquets de zone que la version Claude importe.

## Utilisation

Ouvrir la page web, choisir une zone, puis « Tenter la collecte directe » (qui enchaîne l'enrichissement). Hors de Claude, la mémoire en ligne et l'agent Claude sont désactivés ; le suivi de précision est conservé sur l'appareil.

## Sources de données

- OpenStreetMap © contributeurs OpenStreetMap, licence ODbL
- Open-Meteo, licence CC BY 4.0
- INSEE via geo.api.gouv.fr, Licence Ouverte
- Ville de Paris, open data (comptages vélo et routiers), licence ODbL
- Extraits régionaux : Geofabrik
- Photos aériennes : IGN Géoplateforme (Licence Ouverte) ; Esri World Imagery (© Esri, Maxar, Earthstar Geographics)

Predictor ne collecte ni n'analyse aucune donnée sur des personnes.
