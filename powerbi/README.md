# Rapport Power BI

Le rapport partageable est `Euro_2024_Dashboard.pbix`. Il contient trois pages :

- **1. Analyse Équipes** : efficacité offensive et tirs.
- **2. Scouting Joueurs** : comparaison des joueurs et indicateurs par 90 minutes.
- **3. Analyse Matchs** : nombre de matchs, buts totaux, écart buts–xG, taux de conversion et buts par phase.

Les indicateurs de la page 3 utilisent les scores globaux de la compétition. Le graphique par phase n’isole pas les équipes « à domicile » et « à l’extérieur », ce qui évite de donner un sens de terrain à une compétition disputée sur sites neutres.

Le thème `theme_euro_2024.json` utilise une palette inspirée de l’Euro 2024. Les visuels de logo ont été retirés du PBIX inclus. Le logo StatsBomb est placé dans le README du dépôt pour créditer la source, conformément aux consignes d’attribution.

## Données et actualisation

Les tables sont fournies dans `../data/`. Pour actualiser le rapport sur une autre machine, ouvrir **Transformer les données > Paramètres des sources de données** et reconnecter les CSV du dépôt. Les colonnes décimales utilisent le point comme séparateur. Vérifier les types et la relation `dim_matches[match_id]` → `shots_data[match_id]` après le déplacement du dossier.

Le PBIX contient un instantané du modèle importé. La copie des CSV ne reconfigure pas automatiquement les chemins de Power Query.

## Publication

Les données sont issues de StatsBomb Open Data. Lire `../THIRD_PARTY_NOTICES.md` et les conditions officielles StatsBomb avant toute publication ou réutilisation. Le projet n’est pas affilié à StatsBomb, Hudl ou l’UEFA.