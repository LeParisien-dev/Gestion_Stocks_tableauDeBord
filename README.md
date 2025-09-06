Gestion des Stocks – Dashboard Supply Chain - Sept 2025
(ENGLISH below)

Objectif du projet
Ce projet simule un workflow complet de gestion des stocks et de suivi des ruptures pour une chaîne logistique fictive.

Il montre la maîtrise de :

- La préparation et nettoyage des données
- L’analyse statistique et visualisation
- La création de dashboards interactifs avec Tableau Public
- La prédiction simple de ruptures à l’aide d’un modèle Logistic Regression

////////////////////////////

Structure du dépôt
/raw_data # Fichiers CSV simulés : stocks, commandes, fournisseurs, filiales
/data_cleaning # Scripts ou notebooks pour fusionner et nettoyer les données
/analysis # Notebook principal pipeline complet avec analyse et graphiques
/exports_tableau # Fichiers CSV générés prêts pour Tableau Public
/ai # Notebook de prédiction des ruptures

///////////////////////////

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

///////////////////

Instructions pour reproduire :
1. Cloner le dépôt :
git clone https://github.com/LeParisien-dev/Gestion_Stocks_tableauDeBord.git

2. Installer les dépendances (exemple via pip) :

pip install pandas numpy matplotlib seaborn scikit-learn jupyter

3. Ouvrir le notebook analysis/01_pipeline_complet.ipynb dans Jupyter Notebook ou VS Code.

4. Lancer tout en bas la cellule contenant run_pipeline() → tous les exports et graphiques seront générés automatiquement.

//////////////////

TABLEAU PUBLIC :
https://public.tableau.com/authoring/TableauDeBordSimulation/Tableaudebord1#1

/////////////////

Notes projet :
Données simulées pour démonstration
Contrôle automatique dans la prédiction pour éviter les erreurs si trop peu de ruptures
Pipeline conçu pour exécution automatisée en 1 clic, pratique pour un workflow réel

////////////////////
////////////////////


ENGLISH VERSION


Project Objective

This project simulates a complete workflow for stock management and tracking stockouts for a fictional supply chain.

It demonstrates proficiency in:

Data preparation and cleaning

Statistical analysis and visualization

Creating interactive dashboards with Tableau Public

Simple stockout prediction using a Logistic Regression model


/////////////////////

Repository Structure
/raw_data           # Simulated CSV files: stocks, orders, suppliers, branches
/data_cleaning      # Scripts or notebooks for merging and cleaning data
/analysis           # Main notebook with full pipeline, analysis, and visualizations
/exports_tableau    # Generated CSV files ready for Tableau Public
/ai                 # Notebook for stockout prediction


/////////////////////////

Automated Pipeline (run_pipeline())

The notebook analysis/01_pipeline_complet.ipynb contains the function run_pipeline(), which executes the entire workflow in one click:

Data Loading and Cleaning

Remove duplicates

Standardize IDs and names

Create new columns (Stock_After_Sale, Inventory_Value)

Statistical Analysis and Visualization

Global statistics (describe)

Pivot table: average stock by region and warehouse

Top 10 products with stockouts

Top 10 suppliers contributing to stockouts

SKU × Supplier heatmap

Jupyter Visualizations

Barplots for stockouts and stock levels by region

Heatmap to visualize critical dependencies

Scatter plot: average stock vs number of stockouts

CSV Exports for Tableau Public

stocks_region_entrepot.csv

top10_ruptures.csv

top10_fournisseurs.csv

sku_fournisseur_ruptures.csv

Stockout Prediction (Risque_Rupture)

Logistic Regression with handling of imbalanced classes

Column added to the DataFrame and used for Tableau visualization

//////////////////////////////////////

Instructions to Reproduce

1. Clone the repository:

git clone https://github.com/LeParisien-dev/Gestion_Stocks_tableauDeBord.git


2. Install dependencies (example via pip):

pip install pandas numpy matplotlib seaborn scikit-learn jupyter


3. Open the notebook analysis/01_pipeline_complet.ipynb in Jupyter Notebook or VS Code.

4. Run the cell at the bottom containing run_pipeline() → all CSV exports and visualizations will be generated automatically.

///////////////////////

Tableau Public
View Dashboard :
https://public.tableau.com/authoring/TableauDeBordSimulation/Tableaudebord1#1

//////////////////////////

Project Notes

Simulated data for demonstration purposes

Automatic control in the prediction step to prevent errors if there are too few stockouts

Pipeline designed for one-click automated execution, practical for real workflow in real time
