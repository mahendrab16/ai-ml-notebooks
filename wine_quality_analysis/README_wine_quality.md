# 🍷 Red Wine Quality Analysis & Prediction

## 📌 Overview
This project explores the **Red Wine Quality dataset** and builds machine learning models to estimate wine quality scores from physicochemical properties.

The notebook covers data cleaning, exploratory data analysis (EDA), model training, evaluation, and feature-importance analysis.

> This is an educational machine-learning project. Predictions are estimates and should not be treated as professional wine assessments.

## 🎯 Objectives
- Understand the structure and quality of the dataset.
- Explore distributions and relationships between wine properties.
- Identify features associated with wine quality.
- Compare baseline and machine-learning regression models.
- Evaluate model performance using appropriate metrics.

## 📊 Dataset
- **Source:** [UCI Machine Learning Repository — Wine Quality](https://archive.ics.uci.edu/dataset/186/wine+quality)
- **File used:** `winequality-red.csv`
- **Target column:** `quality`
- **Input features:** Physicochemical measurements such as acidity, residual sugar, chlorides, density, pH, sulphates, and alcohol.
- **Format note:** The original CSV uses a semicolon (`;`) delimiter.

The notebook attempts to download the public dataset automatically if it is not available locally. If you load the CSV manually, use:

```python
import pandas as pd

df = pd.read_csv("winequality-red.csv", sep=";")
```

## 🧰 Tools & Libraries
- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Scikit-learn
- Google Colab or Jupyter Notebook

## 🔍 Workflow

1. **Load data** — find or download the CSV and read it using the correct delimiter.
2. **Inspect data** — check shape, column names, data types, descriptive statistics, missing values, and duplicates.
3. **Clean data** — standardize column names and remove duplicate rows.
4. **Perform EDA** — visualize quality-score counts, feature distributions, correlations, and selected feature relationships.
5. **Prepare data** — separate input features (`X`) from target (`y`) and create a train/test split.
6. **Train models** — compare a mean-prediction baseline, Random Forest Regressor, and MLP Neural Network Regressor.
7. **Evaluate models** — calculate MAE, RMSE, and R² on the held-out test set.
8. **Inspect results** — plot actual vs. predicted values and residuals.
9. **Explore feature importance** — review Random Forest feature importances.

## 🤖 Models & Metrics

### Models
- **Dummy Regressor:** baseline that predicts the training-set mean.
- **Random Forest Regressor:** ensemble of decision trees that can model nonlinear relationships.
- **MLP Regressor:** feed-forward neural network.

### Evaluation metrics
- **MAE:** average absolute difference between actual and predicted scores; lower is better.
- **RMSE:** gives greater penalty to larger errors; lower is better.
- **R²:** measures performance relative to a mean-prediction baseline; higher is generally better, and it can be negative on test data.

Actual results depend on running the notebook. No performance numbers are claimed here.

## 📁 Repository Contents

```text
.
├── README.md
└── wine_quality_analysis.ipynb
```

## ▶️ How to Run

### Option 1: Google Colab
1. Open `wine_quality_analysis.ipynb` in GitHub.
2. Click **Open in Colab** if available, or download the notebook and upload it to [Google Colab](https://colab.research.google.com/).
3. Run the cells from top to bottom.
4. Check the output metrics and plots, then update the conclusions section with your findings.

### Option 2: Local Jupyter Notebook
1. Install Python 3.
2. Install the required libraries:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn jupyter
```

3. Start Jupyter:

```bash
jupyter notebook
```

4. Open `wine_quality_analysis.ipynb` and run all cells.

If automatic dataset download is unavailable, download `winequality-red.csv` from the UCI dataset page and place it in the notebook's working directory.

## 📌 Key Findings
Fill in this section **after running the notebook**:
- Most common wine quality score: _add from output_
- Strongest observed correlations with quality: _add from correlation table_
- Best model by test RMSE: _add from model comparison table_
- Test MAE, RMSE, and R²: _add actual results_

## ⚠️ Limitations
- The dataset contains a limited set of red-wine samples and physicochemical features.
- Correlation does not establish causation.
- Feature importance is model-specific and does not prove a feature causes quality.
- The evaluation uses a single train/test split; cross-validation and hyperparameter tuning could provide a more robust comparison.
- Predicted scores are estimates and may not match subjective human assessments.

## 🚀 Future Improvements
- Use cross-validation and tune model hyperparameters.
- Compare regression with ordinal or multiclass classification.
- Add permutation importance or SHAP explanations.
- Build a small web interface for entering feature values and viewing predictions.
- Track experiments and make results reproducible with fixed random seeds.

## 📚 Reference
Cortez, P., Cerdeira, A., Almeida, F., Matos, T., & Reis, J. (2009). *Modeling wine preferences by data mining from physicochemical properties.* Decision Support Systems, 47(4), 547–553.

Dataset: [UCI Wine Quality](https://archive.ics.uci.edu/dataset/186/wine+quality)

## 📄 License
Add a license if you want to specify reuse permissions. Before redistributing the dataset or third-party code, check their respective license and usage terms.
