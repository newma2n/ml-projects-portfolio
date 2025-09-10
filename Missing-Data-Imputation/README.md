# Gestion Optimale des Données Manquantes

## 🎯 Objectif
Étudier et comparer différentes stratégies pour gérer les données manquantes dans un dataset médical (UCI Heart Disease).

## 🔎 Méthodologie
- Analyse des mécanismes de données manquantes (MCAR, MAR, MNAR).
- Implémentation de plusieurs méthodes d’imputation :
  - Moyenne / Médiane
  - KNN Imputer
  - Random Forest Imputer
- Évaluation des performances avec des modèles de classification.

## 📊 Résultats
- Les méthodes simples (moyenne/médiane) sont rapides mais biaisées.
- KNN et Random Forest offrent de meilleures performances.
- Métriques utilisées : Accuracy, F1-score, AUC.

## 🛠️ Stack
Python · Pandas · NumPy · Scikit-learn · Matplotlib · Seaborn