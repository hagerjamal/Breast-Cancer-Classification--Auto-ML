# Breast Cancer Classification using AutoML Tools

This project focuses on building classification models to detect breast cancer using different AutoML libraries. The dataset used contains features extracted from digitized images of breast mass (mean radius, texture, perimeter, etc.), and the target variable is the diagnosis (`M` = malignant, `B` = benign).

---

## 📊 Dataset
- **Source**: Breast Cancer Wisconsin (Diagnostic) dataset.
- **Target column**: `diagnosis` (Malignant or Benign).
- **Preprocessing**:
  - Dropped unnecessary columns like `id`.
  - Label encoding applied to convert diagnosis values into integers (`M` → 1, `B` → 0).
  - Checked for class imbalance and confirmed the data is relatively balanced.

---

## ⚙️ Tools Used

### 1. H2O AutoML
- Used `H2OAutoML` to automatically train and tune multiple models.
- Displayed leaderboard of models and selected the best one based on performance.
- Converted Pandas DataFrame to H2O Frame before training.

### 2. FLAML
- Used `AutoML` from the `flaml` library.
- Defined time and metric constraints.
- Achieved a fast and resource-efficient model without extensive hyperparameter tuning.

### 3. LazyClassifier
- Used `LazyClassifier` for quick model benchmarking.
- Compared multiple classification algorithms without manual model building.
- Provided a quick overview of which models perform well on the dataset.

---

## 🧪 Evaluation
- Models were evaluated using accuracy, precision, recall, and F1-score.
- Visualizations such as count plots and pair plots were used for EDA (Exploratory Data Analysis).
- TPOT and PyCaret were tested but excluded due to compatibility issues on Kaggle environment (e.g. CUDA driver errors).

---

## 📁 Project Structure

──# breast-cancer-classification-automated-ml : Main notebook with all experiments
├─# breast-cancer.csv : The Dataset
├─# README.md # Project overview and documentation
