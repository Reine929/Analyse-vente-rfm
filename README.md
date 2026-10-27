# Analyse de ventes et segmentation RFM

TP réalisé individuellement pendant mon Bachelor Business Intelligence & Data à Nexa Digital School, sur un jeu de données de ventes fourni en cours.

## Le jeu de données

10 320 lignes de commandes (février 2023 à février 2025) dans 5 pays (France, Suisse, Portugal, Belgique, Espagne), 11 clients entreprises, 3 catégories de produits : ventes, profit, quantités, magasin, segment.

## Ce que fait le notebook

1. **Nettoyage** : formats des dates et des variables catégorielles, valeurs manquantes (mode pour la sous-catégorie, médiane pour les variables numériques), 58 doublons supprimés, valeurs aberrantes plafonnées avec la méthode IQR.
2. **Analyses univariées, bivariées et multivariées** : histogrammes, boîtes à moustaches, matrice de corrélation, test du Chi², pairplot.
3. **Séries temporelles** : tendances mensuelles et saisonnalité, pour l'ensemble des ventes, un magasin et un pays.
4. **Indicateurs de performance (KPI)** : chiffre d'affaires, profit et marge par pays, catégorie, segment et produit.
5. **Segmentation RFM** des clients (récence, fréquence, montant) et pistes d'actions marketing par client.

## Quelques résultats

- Chiffre d'affaires total : environ 14,3 millions, pour un profit représentant environ 8,7 % du chiffre d'affaires.
- La France réalise le plus fort chiffre d'affaires hebdomadaire cumulé (environ 4,8 millions, le double des autres pays).
- Les trois catégories de produits rapportent à peu près le même chiffre d'affaires ; la catégorie « office supplies » est la plus rentable.
- Le segment « corporate » génère le plus de ventes et de profit.

## Limites

- Le jeu de données ne compte que 11 clients, et leurs dernières commandes datent toutes des 9 et 10 février 2025 : la récence ne permet pas de les distinguer. La segmentation RFM est donc un exercice de méthode, pas une conclusion business.
- Une grande partie du profit est attribuée à un produit « Generic Product » qui regroupe des articles non détaillés.
- Les valeurs manquantes (environ 5 % à 10 % selon les colonnes) sont remplacées par la médiane ou le mode, ce qui peut atténuer les écarts.

## Lancer le projet

1. Installer les dépendances : `pip install -r requirements.txt`
2. Placer dans le même dossier le fichier `sales_dataset.csv` fourni en cours (non inclus dans ce dépôt).
3. Ouvrir `analyse_ventes_rfm.ipynb` avec Jupyter et exécuter les cellules dans l'ordre.

## Outils

Python, Pandas, NumPy, Matplotlib, Seaborn, SciPy, Jupyter.
