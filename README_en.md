## Introduction

This project presents a solution for the analysis and classification of counterfeit banknotes. By combining several machine learning techniques, this project aims to identify fake banknotes based on their physical characteristics (dimensions, margins, diagonals). It is designed to showcase skills in data manipulation, statistical analysis, and modeling.

## Objectives

- **Analyze banknote characteristics** to detect patterns distinguishing counterfeit notes.
- **Reduce data dimensionality** using Principal Component Analysis (PCA).
- **Cluster the banknotes** using unsupervised methods like KMeans.
- **Model a supervised classification algorithm** using logistic regression.

## Project Structure

### 1. Library and Data Import
The required libraries are imported, followed by the loading of banknote data, along with basic cleaning steps (checking for missing values and data types).

**Main libraries used**:
- `pandas`, `numpy`: Data manipulation.
- `matplotlib`, `seaborn`: Visualization.
- `scikit-learn`: Statistical analysis and machine learning.

### 2. Exploratory Data Analysis

Univariate and bivariate analyses are performed to understand the distribution of variables like:
- Banknote length,
- Banknote height (measured from the left and right sides),
- Banknote diagonal,
- Margins (top and bottom).

Visualizations such as box plots and scatter plots are used to explore these relationships.

### 3. Principal Component Analysis (PCA)

PCA is used to reduce the dimensionality of the data while retaining the most relevant information. This helps to visualize groups in a 2D or 3D space, making it easier to identify patterns between real and counterfeit banknotes.

- **Standardization**: Data is standardized before applying PCA.
- **Interpretation**: The first two principal components capture a significant portion of the total variance.

### 4. Unsupervised Classification with KMeans

The KMeans algorithm is used to separate banknotes into two clusters:
- **Objective**: Separate banknotes into groups representing real and counterfeit without using labels.
- **Results**: KMeans performance is evaluated visually through clusters in the PCA space.

### 5. Supervised Modeling with Logistic Regression

Logistic regression is used to predict whether a banknote is genuine or not, based on its physical characteristics.

- **Data Splitting**: The dataset is split into training and test sets.
- **Model Evaluation**: The model is evaluated using accuracy and ROC/AUC curves.
- **Results**: Performance metrics indicate the model's ability to accurately predict counterfeit notes.

## Conclusion

This project demonstrates the use of machine learning techniques to solve a binary classification problem. Exploratory methods like PCA and machine learning models such as KMeans and logistic regression provide a robust analysis of the data.

## Prerequisites

- Python 3.x
- Required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`

## Installation Instructions

1. Clone this repository:
   ```bash
   git clone https://github.com/your-repo.git
   ```

2. Install the dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Run the Jupyter notebook to follow the analysis step by step:
   ```bash
   jupyter notebook Detection_faux_billets_code.ipynb
   ```

## Authors

This project was developed by Lamarana DIALLO, a passionate data science and predictive analytics enthusiast.