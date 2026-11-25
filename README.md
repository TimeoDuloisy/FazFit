# FazFit

Application web d'entraînement sportif personnalisé, en français, pensée pour le mobile. Tout tient dans un seul fichier : `index.html`.

## Fonctionnalités

- **Questionnaire** en 6 étapes : profil, objectifs, blessures, lieu et matériel, planning, style et split, muscles prioritaires, exercices favoris ou exclus.
- **Programme de 4 à 12 semaines** avec progression automatique par blocs de 4 semaines (3 semaines de montée, 1 semaine allégée).
- **Séances construites par rôle** : chaque exercice a un rôle précis (développé à plat, incliné, écarté, triceps en isolation…). Une séance ne mélange pas les groupes musculaires.
- **Modèles de séances** : full body, haut / bas, push / pull / legs et split par muscle, adaptés au nombre de séances.
- **Plus de 110 exercices**, chacun avec ses consignes, une variante plus facile et une plus difficile, et un bouton pour le remplacer par un équivalent.
- **Animation du mouvement** pour chaque exercice, avec les muscles travaillés en rouge.
- **Mode séance** : ordre des exercices au choix pendant la séance, chronomètre, minuteur de repos avec bip, saisie des charges et répétitions, charge conseillée.
- **Suivi** : jours actifs d'affilée, calendrier sur 12 semaines, poids corporel, charges, volume, historique.
- **Montre Garmin (facultatif)** : import des fichiers exportés depuis Garmin Connect (CSV, TCX, FIT ou .zip) pour ajouter fréquence cardiaque, calories et courbe cardiaque aux séances.
- Thème clair ou sombre, 6 couleurs d'accent, kg ou lb.

## Lancer l'appli

Ouvre `index.html` dans un navigateur. Il n'y a ni installation ni étape de build. Il faut une connexion internet au premier chargement, pour récupérer React, htm, fflate et les polices.

## Données

Tout est enregistré dans le navigateur (`localStorage`, clés `fazfit:*`). Rien n'est envoyé à un serveur. Les données ne passent pas d'un appareil à l'autre.

## Technique

- React 18 (UMD) avec [htm](https://github.com/developit/htm) à la place de JSX, donc sans compilation.
- [fflate](https://github.com/101arrowz/fflate) pour lire les .zip Garmin.
- Graphiques et animations en SVG, dessinés à la main.
