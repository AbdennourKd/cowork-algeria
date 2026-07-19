# Espaces de coworking à Alger

⚠️ **Limitation importante** : l'accès direct à Google Maps (et aux principaux
sites annuaires : Coworker.com, Workin.space, DaVinci Meeting Rooms, etc.) est
bloqué par la politique réseau de l'environnement d'exécution utilisé pour
produire ce tableau. Il n'a donc **pas été possible de récupérer les notes et
le nombre d'avis Google réels**. Les données ci-dessous proviennent de
recherches web publiques (pages officielles, Facebook, CoworkBooking...) et
sont classées, à défaut de note Google, selon le meilleur signal d'avis
positif disponible trouvé pour chaque espace. Beaucoup d'espaces n'ont aucune
donnée d'avis publique trouvée (`N/D`).

Pour obtenir un classement fiable basé sur les vraies notes Google, il faut
une clé API Google Places (voir section méthodologie en bas de page).

## Classement (meilleur signal d'avis disponible en premier)

| # | Nom | Quartier | Adresse | Note Google Maps | Signal d'avis alternatif trouvé | Source |
|---|-----|----------|---------|:---:|---|---|
| 1 | Sylabs | Alger Centre | Près de la Grande Poste / station Tafoura | N/D | 96 % de recommandation, 60 avis (Facebook) | [Facebook](https://www.facebook.com/SylabsDZ/) |
| 2 | Space X Coworking | Bordj El Kiffan | Lot N, Cité, 28 Rue Daib Aissa (relocalisé 2023) | N/D | 70 % de recommandation, 8 avis (Facebook) | [Facebook](https://www.facebook.com/SX.coworking/) |
| 3 | The Address Coworking Space | Alger Centre / El Mohammadia | El Mohammadia Mall (4e ét.) + Sidi Yahia | N/D | 9,9/10 sur CoworkBooking (1 note) | [CoworkBooking](https://www.coworkbooking.com/africa/algeria/algiers/the-address-coworking-space) |
| 4 | Orbit Coworking & Training Space | Sidi M'Hamed | 21 Rue Mercurie, Bd Mohamed V | N/D | Avis qualitatifs positifs, pas de note chiffrée | [Coworker.com](https://www.coworker.com/algeria/sidi-mhamed/orbit-coworking-training-space) |
| 5 | 95 | Alger Centre | 95 Rue Didouche Mourad | N/D | Page Facebook créée, non notée (1 avis) | [Facebook](https://www.facebook.com/95didouchemourad/) |
| 6 | Horizon Business Space | Bir Mourad Raïs | P2MH+2RP, Bir Mourad Raïs 16000 | N/D | Page Facebook non notée (0 avis) | [Facebook](https://www.facebook.com/Horizonbusinessspace/) |
| 7 | Regus | Alger Centre / Hydra / Bab Ezzouar | Plusieurs sites | N/D | Avis épars, pas de note consolidée | [Trustpilot](https://fr.trustpilot.com/review/regus.com/location/alger-bab-ezzouar) |
| 8 | La Bulle Space | El Mouradia | 04 Rue Abdou Mohamed | N/D | Aucune note formelle | [CoworkBooking](https://www.coworkbooking.com/africa/algeria/algiers/la-bulle-space) |
| 9 | Bab 08 | Alger Centre | 08 Rue Didouche Mourad / Place Audin | N/D | N/D | [Site officiel](https://bab08.com/) |
| 10 | L2C Space | Baba Hassen | Baba Hassen | N/D | N/D | [Facebook](https://www.facebook.com/l2cspace/) |
| 11 | Comet Coworking | Baba Hassen | Lotissement 19 mai 1956 N°16 Bis, 16081 | N/D | N/D | [Facebook](https://www.facebook.com/CometCoworking/) |
| 12 | Emir Synergy | Alger Centre (près Place Emir Abdelkader) | Non précisée | N/D | N/D | [Facebook](https://www.facebook.com/Emirsynergy/) |
| 13 | Perfect Space Coworking | Bordj El Kiffan | Cité Saidi Mohamed N°61 | N/D | N/D | [Facebook](https://www.facebook.com/p/Perfect-Space-Coworking-100032868234210/) |
| 14 | IncubMe | Alger | Non précisée | N/D | N/D | [Site officiel](https://incubme.com/) |
| 15 | FADAA Coworking | Alger | 3 sites à Alger (non précisés) | N/D | N/D | [Site officiel](https://fadaa.dz/) |
| 16 | Ikosim Tech Hub | Alger | Non précisée | N/D | N/D | [Site officiel](https://ikosim-tech-hub.com/workspace/coworking/) |
| 17 | IN NETWORK | Hydra | Entrée autoroute de Hydra | N/D | N/D | [Site officiel](https://www.in-network.dz/coworking/) |

Données brutes : [`coworking-algiers.csv`](./coworking-algiers.csv)

## Méthodologie et limites

- Liste compilée à partir de recherches web (annuaires de coworking, pages
  Facebook officielles, sites des espaces eux-mêmes) — pas d'accès direct à
  l'API ou aux pages Google Maps depuis cet environnement.
- Les pourcentages « recommandation Facebook » ne sont **pas** des notes
  Google et ne sont pas directement comparables entre elles (bases d'avis
  très différentes : 1 à 60 avis selon l'espace).
- La liste peut être incomplète et les adresses/statuts (fermeture,
  déménagement) peuvent avoir changé depuis la collecte.
- Pour un classement fiable basé sur de vraies notes et vrais volumes d'avis
  Google, il faut interroger la **Google Places API** avec une clé API
  valide (créable gratuitement sur console.cloud.google.com, quota gratuit
  mensuel disponible). Cet environnement peut atteindre
  `maps.googleapis.com` en réseau mais n'a pas de clé API configurée.
  Si une clé est fournie, un script peut être écrit pour interroger l'API
  Places (Text Search + Place Details) sur chaque quartier d'Alger et
  produire un classement basé sur `rating` × `user_ratings_total` réels.
