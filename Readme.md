## Introduction

Ce projet présente une solution d'analyse et de classification pour détecter les faux billets. En combinant plusieurs techniques d'apprentissage automatique, ce projet vise à identifier les billets contrefaits à partir de caractéristiques physiques (dimensions, marges, diagonales). Il est conçu pour illustrer des compétences en manipulation de données, analyse statistique, et modélisation.

## Objectifs

- **Analyser les caractéristiques** des billets pour détecter les schémas qui les distinguent.
- **Réduire la dimensionnalité** des données à l'aide de l'Analyse en Composantes Principales (ACP).
- **Classer les billets** avec des méthodes non supervisées comme KMeans.
- **Modéliser un algorithme de classification supervisée** avec la régression logistique.

## Structure du projet

### 1. Importation des librairies et des données
Les librairies nécessaires sont importées, suivies par le chargement des données de billets, avec des étapes de nettoyage de base (vérification des valeurs manquantes et des types de données).

**Principales librairies utilisées** :
- `pandas`, `numpy` : Manipulation de données.
- `matplotlib`, `seaborn` : Visualisation.
- `scikit-learn` : Analyse statistique et machine learning.

### 2. Analyse exploratoire des données

Les analyses univariées et bivariées permettent de comprendre la distribution des variables comme :
- La longueur du billet,
- La hauteur du billet (mesurée des côtés gauche et droit),
- La diagonale du billet,
- Les marges (supérieure et inférieure).

Des graphiques comme les boxplots et les scatter plots sont utilisés pour visualiser ces relations.

### 3. Analyse en Composantes Principales (ACP)

L'ACP est utilisée pour réduire la dimensionnalité des données tout en conservant les informations pertinentes. Cela permet de mieux visualiser les groupes dans un espace à 2 ou 3 dimensions, facilitant la détection de patterns entre les vrais et faux billets.

- **Standardisation** : Les données sont standardisées avant l'application de l'ACP.
- **Interprétation** : Les deux premières composantes principales capturent une grande partie de la variance totale.

### 4. Classification non supervisée avec KMeans

L'algorithme KMeans est utilisé pour tenter de séparer les billets en deux clusters :
- **Objectif** : Séparer les billets en groupes représentant les vrais et faux billets sans utiliser d'étiquettes.
- **Résultats** : Les performances de KMeans sont évaluées visuellement, via des clusters dans l'espace des composantes principales.

### 5. Modélisation supervisée avec Régression Logistique

Une régression logistique est utilisée pour prédire si un billet est authentique ou non, en se basant sur les caractéristiques physiques.

- **Division des données** : Le jeu de données est séparé en ensembles d'entraînement et de test.
- **Évaluation du modèle** : Le modèle est évalué à l'aide de la précision (accuracy) et des courbes ROC/AUC.
- **Résultats** : Les métriques de performance montrent la capacité du modèle à bien prédire les faux billets.

## Conclusion

Ce projet démontre l'utilisation de techniques d'apprentissage automatique pour résoudre un problème de classification binaire. Les méthodes exploratoires comme l'ACP et les modèles de machine learning comme KMeans et la régression logistique permettent une analyse robuste des données.

## Prérequis

- Python 3.x
- Bibliothèques nécessaires : `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## Instructions d'installation

1. Clonez ce dépôt :
   ```bash
   git clone https://github.com/Classification-faux-billets.git
   ```

2. Installez les dépendances :
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn
   ```

3. Exécutez le notebook Jupyter pour suivre l'analyse pas à pas :
   ```bash
   jupyter notebook Detection_faux_billets_code.ipynb
   ```