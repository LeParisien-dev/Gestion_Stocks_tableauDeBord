Gestion des Stocks – Dashboard Supply Chain - Sept 2025
Objectif du projet
Ce projet simule un workflow complet de gestion des stocks et de suivi des ruptures pour une chaîne logistique fictive.
Il montre la maîtrise de :

La préparation et nettoyage des données
L’analyse statistique et visualisation
La création de dashboards interactifs avec Tableau Public
La prédiction simple de ruptures à l’aide d’un modèle Logistic Regression
Structure du dépôt
/raw_data # Fichiers CSV simulés : stocks, commandes, fournisseurs, filiales /data_cleaning # Scripts ou notebooks pour fusionner et nettoyer les données /analysis # Notebook principal pipeline complet avec analyse et graphiques /exports_tableau # Fichiers CSV générés prêts pour Tableau Public /ai # Notebook de prédiction des ruptures /docs # Captures d’écran et notes projet

Pipeline automatisé (run_pipeline())
Le notebook analysis/01_pipeline_complet.ipynb contient la fonction run_pipeline() qui exécute tout le workflow en 1 clic :

Chargement et nettoyage des données

Suppression des doublons
Standardisation des IDs et noms
Création de nouvelles colonnes (Stock_After_Sale, Inventory_Value)
Analyse statistique et visuelle

Stats globales (describe)
Pivot table : stock moyen par région et entrepôt
Top 10 produits en rupture
Top 10 fournisseurs contribuant aux ruptures
Heatmap SKU × Fournisseur
Graphiques Jupyter

Barplots pour les ruptures et les stocks par région
Heatmap pour visualiser les dépendances critiques
Scatter plot : stock moyen vs nombre de ruptures
Export CSV pour Tableau Public

stocks_region_entrepot.csv
top10_ruptures.csv
top10_fournisseurs.csv
sku_fournisseur_ruptures.csv
Prédiction des ruptures (Risque_Rupture)

Logistic Regression avec gestion des classes déséquilibrées
Colonne ajoutée au DataFrame et utilisée pour visualisation Tableau
Instructions pour reproduire
Cloner le dépôt :
git clone https://github.com/LeParisien-dev/Gestion_Stocks_tableauDeBord.git

Capture d'écran du tableau de bord :
https://public.tableau.com/authoring/TableauDeBordSimulation/Tableaudebord1#1
