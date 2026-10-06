# Predictor

Logiciel d'analyse de données et de prédiction sur un monde réel virtualisé, développé par **F.S.M Game House**.

Version actuelle : **v0.6**

## Ce que fait Predictor

1. **Collecte** : carte OpenStreetMap d'une zone (via Overpass Turbo, GeoJSON ou fichier régional `.osm.pbf` de Geofabrik) et prévisions météo Open-Meteo (CSV ou JSON).
2. **Monde virtualisé** : rues et lieux redessinés, classés en 9 familles.
3. **Analyse** : densité, répartition des lieux, services essentiels, réseau de voies.
4. **Prédictions** : météo 7 jours, fréquentation estimée par heure et par jour, tendances entre relevés, chacune avec un indice de fiabilité.
5. **Mémoire en ligne** et **agent Claude** : disponibles quand Predictor est ouvert dans Claude.

## Utilisation

Ouvrir `index.html` dans un navigateur. Hors de Claude, la mémoire en ligne et l'agent Claude sont désactivés.

## Sources de données

- OpenStreetMap © contributeurs OpenStreetMap, licence ODbL
- Open-Meteo, licence CC BY 4.0
- Extraits régionaux : Geofabrik

Predictor ne collecte ni n'analyse aucune donnée sur des personnes.
