# Formateur de bases élèves — EcolePay

Outil autonome (une seule page HTML, aucun serveur requis) qui convertit les
exports d'élèves de n'importe quelle école — CSV, Excel, plusieurs fichiers,
en-têtes variables — vers le format attendu pour l'import en masse EcolePay :
`nom, prenom, classe, telephone` (+ matricule en option).

## Utiliser en ligne
Ouvrez `index.html` dans un navigateur (Chrome ou Firefox recommandés).
Aucune donnée n'est envoyée à un serveur : tout le traitement se fait dans le
navigateur, sauf le bouton "Suggestion IA" (optionnel) qui appelle l'API
Anthropic uniquement si vous cliquez dessus.

## Déployer
Ce dossier ne contient qu'un seul fichier statique (`index.html`) : il peut
être hébergé tel quel sur GitHub Pages, Hostinger, Netlify, Vercel, ou tout
hébergement statique.

## Fonctionnalités
- Détection automatique des colonnes (nom/prénom séparés ou fusionnés, classe,
  téléphone, matricule) sur CSV (`,` ou `;`) et Excel (`.xls`/`.xlsx`, une ou
  plusieurs feuilles)
- Mapping manuel + suggestion IA quand un format n'est pas reconnu
- Normalisation téléphone (espaces, +225, 00225, 0 manquant)
- Filtres : NAFF/AFF, avec/sans téléphone
- Cellules éditables pour corriger une valeur avant export
- Rapport : effectif par classe, doublons potentiels, téléphones à vérifier
- Export CSV ou XLSX, nom de fichier personnalisable
