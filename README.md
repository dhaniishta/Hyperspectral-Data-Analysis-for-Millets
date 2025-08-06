# Hyperspectral Millet Carbohydrate Prediction

This project applies multiple **regression models** to predict **carbohydrate content** in millets using **hyperspectral reflectance data**. The dataset includes 168 spectral bands as features for each sample.

---

## Objective

- Predict `Carbohydrate` content using 168-band hyperspectral data
- Compare the performance of different regression models:
  - Linear Regression
  - Ridge Regression
  - Lasso Regression
  - Elastic Net Regression
  - Partial Least Squares Regression (PLSR)
  - Support Vector Regression (SVR)

---

## Dataset

- **File**: `Hyperspectral_data_millets_carbohydrate.csv`
- **Samples**: Rows representing millet samples
- **Features**: 168 spectral bands (wavelengths)
- **Target**: `Carbohydrate` (quantitative)

---

## Models & Methods

### 🔹 1. **Linear Regression**
- Simple baseline model.
- No regularization.
- Output: MSE & R²

### 🔹 2. **Ridge Regression**
- L2 regularization.
- `alpha` tuned via cross-validation.
- Scaled input features.

### 🔹 3. **Lasso Regression**
- L1 regularization for sparse feature selection.
- `alpha` tuned via CV.

### 🔹 4. **Elastic Net Regression**
- Combination of L1 and L2 penalties.
- Hyperparameters: `alpha` and `l1_ratio`

### 🔹 5. **Partial Least Squares Regression (PLSR)**
- Dimensionality reduction + regression.
- `n_components` (PCA) tuned.

### 🔹 6. **Support Vector Regression (SVR)**
- RBF kernel.
- Tuned `C` and `epsilon`.

---

## Visualizations

### 🔸 Spectral Signature Example

A sample reflectance curve from the dataset:

<p align="center">
  <img src="assets/spectra_plot.png" alt="Spectra Plot" width="500"/>
</p>

### 🔸 Model Comparison – Regression Performance

<p align="center">
  <img src="assets/regression_performance_carbohydrate.png" alt="Model Comparison" width="600"/>
</p>

- **X-axis**: Mean Squared Error (MSE)
- **Y-axis**: R² score
- Each point = model performance with a specific hyperparameter setting

---

## Libraries Used

- `pandas`, `numpy`
- `matplotlib`, `seaborn`
- `scikit-learn`
- `PCA`, `PLSR`, `SVR`
- `StandardScaler`, `KFold`, `cross_val_predict`

---
