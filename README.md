# Repas PWA

Application PWA statique en HTML pour recenser les repas mangés par plusieurs personnes.

## Principe d'hébergement

- Le code source peut être stocké dans GitHub.
- L'application peut être publiée avec GitHub Pages.
- Les données ne sont pas stockées dans GitHub.
- Les données restent localement sur le téléphone dans IndexedDB.
- Les backups sont exportés manuellement en JSON.
- Le restore remplace les données locales par le contenu du backup choisi.

## Fichiers

- `index.html` : application complète
- `manifest.json` : configuration PWA Android
- `service-worker.js` : cache hors ligne
- `icons/icon-192.png` et `icons/icon-512.png` : icônes PWA

## Installation sur GitHub Pages

1. Créer un dépôt GitHub, par exemple `repas-pwa`.
2. Ajouter les fichiers du dossier à la racine du dépôt.
3. Aller dans `Settings` puis `Pages`.
4. Source : `Deploy from a branch`.
5. Branch : `main`, folder : `/root`.
6. Ouvrir l'URL GitHub Pages sur le Galaxy avec Chrome.
7. Utiliser `Ajouter à l'écran d'accueil`.

## Données locales

Les données sont dans IndexedDB du navigateur Android. Elles peuvent être perdues si :

- le site est supprimé des données Chrome;
- l'application installée est supprimée;
- le téléphone est réinitialisé;
- le navigateur nettoie les données du site.

Il faut donc utiliser régulièrement le bouton Backup.

## Fonctionnalités incluses

- Thème sombre par défaut
- Liste des repas du plus récent au plus vieux
- Personnes pilotables
- Repas pilotables
- Description pour chaque repas
- Catégories pilotables
- Calories par défaut par repas
- Calories facultatives et modifiables par entrée
- Portions
- Notes
- Note sur 10 par entrée
- Notes sur 10 par incrément de 0.5
- Filtres
- Backup JSON
- Restore JSON
- Tendances
- Mode hors ligne après chargement initial


## Installation PWA Android

Important : l'application ne peut pas s'installer comme vraie PWA si tu ouvres directement `index.html` depuis les fichiers du téléphone.

Il faut l'ouvrir depuis une adresse HTTPS, par exemple :

```text
https://ton-utilisateur.github.io/repas-pwa/
```

Étapes recommandées sur Galaxy avec Chrome :

1. Publier le dépôt avec GitHub Pages.
2. Ouvrir l'URL HTTPS de GitHub Pages dans Chrome Android.
3. Attendre que la page soit complètement chargée.
4. Appuyer sur l'icône d'installation dans l'application, ou utiliser le menu Chrome `⋮`.
5. Choisir `Installer l'application` ou `Ajouter à l'écran d'accueil`.

Si Chrome affiche seulement `Ajouter à l'écran d'accueil`, l'icône sera quand même ajoutée. Selon la version de Chrome et l'état du manifest/service worker, le libellé peut varier.

## Vérification rapide

Ouvre ces URL dans Chrome Android :

```text
https://ton-utilisateur.github.io/repas-pwa/manifest.json
https://ton-utilisateur.github.io/repas-pwa/service-worker.js
```

Les deux fichiers doivent s'afficher sans erreur 404.
