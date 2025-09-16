# NeurIPS 2025 Open Polymer Prediction Challenge – Hybrid Ensemble Solution

This repository contains my solution to the [NeurIPS 2025 Open Polymer Prediction Challenge](https://www.kaggle.com/competitions/neurips-open-polymer-prediction-2025/overview), where the goal was to predict various polymer properties with high accuracy.

## 🏆 Results
- **Competition Ranking:** 297 / 2250 participants
- **Weighted MAE:** 0.090 (top score = 0.075)
- **Time Spent:** ~11 days of development

## 🚀 Key Highlights
- Built a **hybrid ensemble system** combining tree-based models, neural networks, and modern tabular methods.
- Achieved competitive performance in a short time using **model stacking, feature selection, and descriptor engineering**.
- Learned advanced integration strategies for **hybrids and ensembles** that generalize across molecular datasets.

## ⚙️ Approach

### Core Models
- XGBoost (`XGBRegressor`)
- CatBoost (`CatBoostRegressor`)
- LightGBM (`LGBMRegressor`)
- Extra Trees (`ExtraTreesRegressor`)
- Random Forest (`RandomForestRegressor`)
- Neural Networks (custom `FeedforwardNet` in PyTorch)
- TabNet (`TabNetRegressor`)
- HistGradientBoosting (`HistGradientBoostingRegressor`)
- GNNs
- RNNs
- even more algorithms

### Stacking Ensembles
- Stacked predictions from XGBoost, LightGBM, CatBoost, Random Forest,... 
- Meta-learners: `ElasticNet`, `CatBoost`, `LightGBM`, `XGBoost`,... 

### Feature Engineering
- **Molecular descriptors:** RDKit, Mordred
- **Fingerprints:** Morgan, MACCS
- **Embeddings:** ChemBERTA (optional)
- **Graph-based features**
- **Aggregated importance:** SHAP, permutation importance, tree-based importance

### Neural Network Architectures
- **Low data (Rg, Tc):** smaller, high-regularization nets
- **Medium data (Tg, Density):** balanced nets
- **High data (FFV):** wide, deep architectures

### Training Strategy
- Cross-validation with stratified folds
- Model averaging across seeds
- Feature selection via Lasso/ElasticNet
- Weighted stacking for robust predictions

## 📊 Performance
The hybrid ensemble was able to consistently approach the top leaderboard scores, showing the strength of combining multiple paradigms of ML models.

## 📚 Learnings
- Gained deeper experience with **hybrid model integration**.
- Practiced balancing **bias-variance tradeoffs** in multi-model systems.
- Strengthened skills in **chemoinformatics feature engineering** and **stacked ensembling**.


---
