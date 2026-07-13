<<<<<<< HEAD
# 🌿 PlantGuard — Plant Disease Prediction from Environmental Data

> A machine learning project that predicts whether a crop is Healthy or Diseased using temperature, humidity, rainfall, and soil pH — comparing Logistic Regression and Random Forest.

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=for-the-badge&logo=plotly&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)

---

## 🧠 Tech Stack

| Layer            | Technology                                                                 |
|------------------|------------------------------------------------------------------------------|
| Data Processing  | ![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat&logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat&logo=numpy&logoColor=white) |
| ML Models        | ![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat&logo=scikitlearn&logoColor=white) (Logistic Regression, Random Forest) |
| Visualization    | ![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat&logo=plotly&logoColor=white) ![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=flat) |
| Environment      | ![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat&logo=jupyter&logoColor=white) |
| Dashboarding     | ![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=flat&logo=powerbi&logoColor=black) |

---

## 📁 Folder Structure

```
plant-disease-prediction/
├── CA2project_improved.ipynb        ← Main notebook (cleaned + corrected analysis)
├── CA2project_1.ipynb               ← Original/earlier version of the notebook
├── plant_disease_dataset.csv        ← Raw input dataset (10,000 records)
├── plant_disease_powerbi_export.csv ← Cleaned + feature-engineered data with predictions, for Power BI
├── images/                          ← Saved plots (EDA, feature importance, confusion matrices, etc.)
├── requirements.txt                 ← Python dependencies
├── .gitignore                       ← Ignores checkpoints, venv, cache, etc.
└── README.md
```

---

## ⚙️ How It Works

1. Load the raw environmental dataset (`temperature`, `humidity`, `rainfall`, `soil_pH`, `disease_present`).
2. Detect and fix anomalies (e.g. humidity readings above 100%) and cap outliers using the IQR method.
3. Run exploratory data analysis — distributions, correlation heatmap, feature-vs-disease boxplots.
4. Engineer new features (`temp_humidity_index`, `rainfall_level`, `soil_pH_deviation`) to expose non-linear/combined effects.
5. Split the data (80/20, stratified) and scale features — fitting the scaler **only on the training set** to avoid leakage.
6. Train and evaluate **Logistic Regression** and **Random Forest**, comparing Accuracy, Precision, Recall, and F1.
7. Export the final cleaned dataset with both models' predictions to CSV for Power BI dashboarding.
8. Save every plot generated along the way into `images/` so they can be viewed directly on GitHub.

---

## 📊 Results

| Model | Accuracy | Precision | Recall | F1 Score |
|---|---|---|---|---|
| Logistic Regression | 0.781 | 0.608 | 0.251 | 0.355 |
| **Random Forest** | **0.864** | **0.779** | **0.608** | **0.683** |

**Random Forest wins** — it's substantially better at catching actual disease cases (recall), suggesting disease risk is threshold-driven (e.g. spikes past a rainfall/humidity point) rather than linear, a pattern tree-based splits capture but Logistic Regression cannot.

![Model Comparison](images/model_comparison.png)
![Feature Importance](images/feature_importance.png)

---

## 🧬 ML Concepts Used

- **Data Cleaning & Anomaly Detection** — physically impossible values, IQR-based outlier capping
- **Feature Engineering** — interaction terms, bucketed thresholds, deviation-from-neutral features
- **Train/Test Split with Stratification** — preserves the ~76/24 class imbalance across splits
- **Feature Scaling without Leakage** — `StandardScaler` fit on training data only
- **Feature Importance** — Random Forest importances computed post-split
- **Classification Models** — Logistic Regression (linear baseline) vs Random Forest (non-linear)
- **Evaluation Metrics** — Accuracy, Precision, Recall, F1, Confusion Matrix
- **BI Export** — predictions exported to CSV for Power BI visualization

---

## 🛠️ Setup & Run

### 1. Clone the repo
```bash
git clone https://github.com/your-username/plant-disease-prediction.git
cd plant-disease-prediction
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the notebook
```bash
jupyter notebook CA2project_improved.ipynb
```
Run all cells top to bottom. Make sure `plant_disease_dataset.csv` is in the same folder as the notebook.

### 4. Outputs
- All plots are saved automatically to the `images/` folder.
- The final predictions dataset is saved as `plant_disease_powerbi_export.csv`, ready to load into Power BI.

---

## ✨ Features

- 🧹 Automated anomaly detection and outlier capping (IQR method)
- 🧪 Engineered features to capture combined/threshold effects (temp × humidity, rainfall buckets, pH deviation)
- ⚖️ Leak-free, stratified train/test split
- 🌲 Two models compared side-by-side (Logistic Regression vs Random Forest)
- 🖼️ Every chart auto-saved to `images/` for easy GitHub/README embedding
- 📊 Ready-to-import CSV export for Power BI dashboards

---

## 📦 Requirements

```
pandas
numpy
matplotlib
seaborn
scikit-learn
jupyter
```

Install all with:
```bash
pip install -r requirements.txt
```

---

## 👨‍💻 Author

**[Your Name]**
CA2 Project — Data Analytics / Machine Learning

---

## 📄 License

This project is for educational purposes only.
=======
# Plant-Disease-Classification
>>>>>>> 5311306c4a5585ec2ca6d162dd58128fa0c1af4e
