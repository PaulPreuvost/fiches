# 2 - Module AI-900T00A : Introduction au Machine Learning
---
### 1. Qu’est-ce que le Machine Learning ?
#### Définition :

Le Machine Learning permet de créer des modèles prédictifs en identifiant des relations dans les données :

- On collecte des échantillons (ex. : fleurs avec caractéristiques + étiquette d'espèce)
- Un algorithme apprend la relation entre caractéristiques et étiquettes
- Le résultat est un modèle capable de prédire l’étiquette d’un nouvel échantillon à partir de ses caractéristiques
---
### 2. Types de Machine Learning

- Apprentissage supervisé : Les données d'entraînement incluent des étiquettes connues

- Apprentissage non supervisé : Les données n’ont pas d’étiquettes

\
Sous-types :

- Régression : Prédiction de valeurs numériques (ex. : nombre de locations de vélos selon la météo)

- Classification : Prédiction de catégories (ex. : risque de diabète selon des mesures cliniques)

- Clustering : Regroupement d’éléments similaires (ex. : classification de véhicules par performance)
---
### 3. Entraînement & Validation des Modèles

- Séparer les données en ensemble d’entraînement et de validation

- Entraîner un modèle avec les données d'entraînement

- Prédire sur les données de validation



- Évaluer les performances :
    
    - En comparant les étiquettes réelles vs. prédites (supervisé)
    
    - En mesurant la qualité des regroupements (non supervisé)
    
    - Répéter jusqu’à obtenir un bon modèle

---
### 4. Machine Learning avec Microsoft Azure
#### Azure Machine Learning

Plateforme cloud pour le Machine Learning, incluant :

Automated ML :

- L’utilisateur fournit les données + le type de problème

- Azure cherche automatiquement le meilleur modèle


#### Azure Machine Learning Designer :

- Outil visuel pour créer des pipelines ML

- Pipeline d’entraînement : entraîner et évaluer un modèle

- Pipeline d’inférence : prédire de nouvelles étiquettes

- Possibilité de déployer le pipeline d’inférence comme un service


---
### 5. Cas Pratiques & Ateliers
Lab – Azure Automated Machine Learning :

    Exploration de l’automatisation de l’entraînement d’un modèle ML

    Réalisable via Azure avec un abonnement fourni

    Lien : https://aka.ms/ai900-automl-lab

---
### 6. Quiz de Révision

    Regrouper des données sans étiquettes → Clustering

    Prédire le prix d’une voiture d’occasion selon ses caractéristiques → Régression

    Catégoriser des demandes de prêts en faible/haut risque → Classification

---
### 7. Références & Ressources

    Outils visuels pour le ML : https://aka.ms/intro-visual-ml