# projet_immo
# 🏠 Prédiction des Prix Immobiliers — DVF

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-2.x-EE4C2C?logo=pytorch&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-1.x-F7931E?logo=scikit-learn&logoColor=white)
![License](https://img.shields.io/badge/Licence-MIT-green)
![Status](https://img.shields.io/badge/Statut-En%20cours-yellow)

> Modèles de machine learning et deep learning pour prédire les prix de vente immobiliers à partir des données DVF (Demandes de Valeurs Foncières) publiées par la DGFiP.

---

## 📌 Description

Ce projet vise à construire et comparer plusieurs approches prédictives sur les transactions immobilières françaises, à partir des données open data **DVF**. Il s'inscrit dans une démarche de valorisation data pour des acteurs du secteur immobilier, comptable ou foncier.

Les données DVF recensent l'ensemble des transactions immobilières en France (appartements, maisons, terrains) avec leurs caractéristiques : surface, localisation, type de bien, prix de vente, etc.

**Objectif :** prédire le prix de vente d'un bien à partir de ses caractéristiques et de sa localisation.

---

## 🧠 Modèles utilisés

| Modèle | Type | Librairie |
|---|---|---|
| Linear Regression | Baseline linéaire | Scikit-learn |
| Random Forest | Ensemble / Bagging | Scikit-learn |
| XGBoost | Ensemble / Boosting | XGBoost |
| Réseau de neurones | Deep Learning | PyTorch |

---

## 📊 Résultats

> *Les métriques seront complétées au fil de l'avancement du projet.*

Modèle  MAE (€/m²)  RMSE (€/m²)  MAPE (%)  R² (log)  R² (€/m²)
           XGBoost      573.57       802.08     23.37    0.6766     0.6939
     Random Forest      597.93       835.26     23.76    0.6606     0.6680
Réseau de neurones      659.96       881.29     29.14    0.5882     0.6304
             Ridge      699.31       951.78     30.87    0.5550     0.5690
---

## 📁 Structure du projet

```
projet_immo/
│
├── data/
│   ├── raw/               # Données DVF brutes téléchargées
│   └── processed/         # Données nettoyées et feature-engineered
│
├── notebooks/
│   ├── 01_exploration.ipynb       # EDA & visualisations
│   ├── 02_preprocessing.ipynb     # Nettoyage et encodage
│   ├── 03_linear_regression.ipynb
│   ├── 04_random_forest.ipynb
│   ├── 05_xgboost.ipynb
│   └── 06_pytorch_nn.ipynb
│
├── src/
│   ├── preprocessing.py   # Pipeline de nettoyage
│   ├── features.py        # Feature engineering
│   └── train.py           # Entraînement des modèles
│
├── models/                # Modèles sauvegardés (.pkl, .pt)
│
├── requirements.txt
└── README.md
```

---

## ⚙️ Installation

```bash
# Cloner le dépôt
git clone https://github.com/alexandresansonnette/projet_immo.git
cd projet_immo

# Installer les dépendances
pip install -r requirements.txt
```

---

## 📦 Dépendances principales

```
pandas
numpy
scikit-learn
xgboost
torch
matplotlib
seaborn
jupyter
```

---

## 🗂️ Source des données

Les données sont issues du portail open data du gouvernement français :  
👉 [https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/](https://www.data.gouv.fr/fr/datasets/demandes-de-valeurs-foncieres/)

---

## 👤 Auteur

**Alexandre Sansonnette**  
Data Scientist | Modèles prédictifs & analyse métier | Python · PyTorch · Scikit-learn  
📍 Occitanie, France  
🔗 [GitHub](https://github.com/alexandresansonnette)

---

## 📄 Licence

Ce projet est sous licence MIT — voir le fichier [LICENSE](LICENSE) pour plus de détails.
