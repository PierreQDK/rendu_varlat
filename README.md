# Modélisation de la performance thermique des bâtiments universitaires

Projet réalisé dans le cadre du Master 1 Économétrie et Statistiques – parcours Économétrie Appliquée (IAE Nantes).  
Encadré par l'équipe pédagogique de l’UE “Modèles à variables latentes (PCR / PLS)”.

## 📌 Objectif

L’objectif de ce projet est de modéliser la **consommation énergétique totale** de bâtiments universitaires à partir de données simulées, en comparant deux méthodes économétriques :

- 📉 **PCR** (Régression sur Composantes Principales)  
- 📊 **PLS** (Partial Least Squares Regression)

Le but est d’identifier la méthode la plus performante pour la prédiction, tout en déterminant les **variables explicatives les plus influentes** via les scores **VIP**.

## 📁 Données

Les données sont issues d’un jeu simulé de **144 bâtiments** appartenant à deux universités (UPENN et GT), fourni par **Tian et al. (2015)**.  
Elles incluent des variables relatives :

- à la **géométrie des bâtiments** (surface, hauteur, orientation)  
- à leur **enveloppe thermique** (coefficients U, surfaces vitrées)  
- et aux **usages internes** (occupation, débits thermiques, équipements)

La variable cible **`EnergyLoad`** est construite comme la somme de la charge de chauffage (`HeatTotal`) et de la charge de refroidissement (`CoolTotal`).  
Une **transformation en racine carrée** a été appliquée pour stabiliser la variance : `sqrt_EnergyLoad`.

## 🛠 Méthodologie

1. **Exploration des données** (distribution, transformation, corrélation)
2. **Modélisation avec et sans transformation**
   - Régression linéaire multiple
   - Régression PCR
   - Régression PLS
3. **Évaluation des performances**
   - R² (apprentissage, validation croisée, test)
   - RMSE (erreur quadratique moyenne)
4. **Interprétation du modèle retenu via scores VIP**

📌 Les modèles sont évalués sur :
- Un jeu d’apprentissage (**UPENN**) avec validation croisée (k=10)
- Un jeu test (**GT**) pour évaluer la généralisation


## 👥 Auteurs

Pierre QUINTIN de KERCADIO
Florian CROCHET


📚 Référence

Tian W., de Wilde P., & Kalz D. (2015). Thermal simulation of university buildings in different climates. Building Simulation Conference.
