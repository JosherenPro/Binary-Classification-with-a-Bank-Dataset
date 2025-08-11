# Binary Classification with a Bank Dataset

Ce projet implémente un pipeline complet de **classification binaire** sur un dataset bancaire, incluant :

* Exploration et analyse des données
* Prétraitement (imputation, encodage, normalisation)
* Optimisation des hyperparamètres avec `RandomizedSearchCV`
* Comparaison de plusieurs modèles (XGBoost, LightGBM, Stacking)
* Génération d'une soumission pour Kaggle
* Score ROC AUC final : 0.96433

## 📂 Données

* **Lien Google Drive (train/test utilisés dans ce notebook)** :
  [📎 Accéder aux fichiers](https://drive.google.com/drive/folders/17Czz1D-gmyK5WurHmANwnXEu9pHBdh-n?usp=sharing)

* **Lien Kaggle officiel** :
  [📊 Playground Series S5E8 - Kaggle Dataset](https://www.kaggle.com/competitions/playground-series-s5e8/data)

> **Note** : Les fichiers doivent être placés dans le dossier :

```
/content/drive/MyDrive/kaggle_1/data/
```

## 🚀 Installation et exécution

1. **Cloner ce repository** :

```bash
git clone https://github.com/JosherenPro/Binary-Classification-with-a-Bank-Dataset.git
cd Binary-Classification-with-a-Bank-Dataset
```

2. **Ouvrir dans Google Colab** :

   * [📓 Notebook Colab](https://colab.research.google.com/github/JosherenPro/Binary-Classification-with-a-Bank-Dataset/blob/main/main.ipynb)

3. **Monter Google Drive** dans Colab :

```python
from google.colab import drive
drive.mount('/content/drive')
```

4. **Télécharger les données** dans le chemin :

```
/content/drive/MyDrive/Binary-Classification-with-a-Bank-Dataset/data
```

5. **Installer les dépendances** si besoin :

```bash
pip install pandas numpy matplotlib scikit-learn xgboost lightgbm
```

6. **Exécuter le notebook**.

## 🧠 Modèles utilisés

* **XGBoost** avec GPU (`tree_method="hist"`, `device="cuda"`)
* **LightGBM**
* **Stacking Classifier** avec :

  * RandomForestClassifier
  * LogisticRegression

## 📊 Résultats

* Optimisation avec `RandomizedSearchCV` (20 itérations par modèle)
* Évaluation par **ROC AUC** en cross-validation
* Score ROC AUC final : 0.96433
* Comparaison des modèles via un **boxplot** (`comparaison_modeles.png`)

## 📄 Soumission

Le notebook génère un fichier `submission.csv` dans :

```
/content/drive/MyDrive/Binary-Classification-with-a-Bank-Dataset/
```

formaté pour Kaggle avec :

```
id, y
```

---

👤 **Auteur** : JosherenPro
📅 **Projet** : Classification binaire - Kaggle Playground Series S5E8
