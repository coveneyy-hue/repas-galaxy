# Correction PWA Repas sans calories

Fichiers à téléverser dans GitHub.

## Changements

- Retrait du champ Calories dans la saisie d'une entrée
- Retrait des calories dans les cartes de repas
- Retrait des filtres minimum / maximum de calories
- Retrait des statistiques de calories
- Retrait des tendances de calories
- Retrait des calories par défaut dans la gestion des repas
- Conservation de la note sur 10 avec incréments de 0.5
- Service worker en cache v7

## Vérification après upload

Dans GitHub, ouvrir `index.html` et rechercher :

```text
Calories
```

Il ne devrait plus y avoir de libellé fonctionnel lié aux calories dans l'interface.
