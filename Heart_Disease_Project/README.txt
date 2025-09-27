# ❤️ Heart Disease Prediction & Clustering  

## 📌 Project Overview  
This project focuses on analyzing a heart disease dataset and building predictive machine learning models to classify patients based on risk.  
In addition to classification, unsupervised clustering techniques are applied to group patients and compare clusters with actual disease labels.

### Key Objectives  
- Clean and preprocess the dataset  
- Select the most important features  
- Train multiple ML models and evaluate their performance  
- Optimize model hyperparameters  
- Apply K-Means and Hierarchical clustering  
- Save the best-performing model for reproducibility  

---

## 📂 Project Structure  
Heart_Disease_Project/
│── data/
│ ├── heart_disease.csv # Original dataset
│ ├── Cleaned # Cleaned dataset after preprocessing
│
│── notebooks/
│ ├── 01_data_preprocessing.ipynb
│ ├── 02_feature_selection.ipynb
│ ├── 03_supervised_learning.ipynb
│ ├── 04_unsupervised_learning.ipynb
│ ├── 05_hyperparameter_tuning.ipynb
│
│── models/
│ ├── final_model.pkl # Saved trained model pipeline
│
│── results/
│ ├── evaluation_metrics.txt # Model performance report
│ ├── clustering_results.csv # K-Means & Hierarchical clustering comparison
│
│── main.py # Main pipeline script (training + clustering)
│── requirements.txt # Required libraries
│── README.md # Project documentation
│── .gitignore


---

## 📊 Dataset
**Source:** UCI Machine Learning Repository – Heart Disease Dataset  
**Target Variable:** `Target` (0 = No Disease, 1–4 = Different severity levels)

**Features:** Age, Sex, ChestPain, RestingBP, Cholesterol, FastingBS, RestECG, MaxHeartRate, ExerciseAngina, Oldpeak, ST_Slope, etc.

---

## ⚙️ Installation & Setup
1. Clone this repository:
```bash
git clone https://github.com/abdulrahmanawad3/Heart_Disease_Project.git
cd Heart_Disease_Project


2, Install dependencies:
pip install -r requirements.txt


💾 Model Export

The final trained pipeline (scaler + selected features + RandomForest model) is saved as:

models/final_model.pkl


You can load and use it for prediction:

import joblib
pipeline = joblib.load("\models\best_heart_disease_model.pkl")
prediction = pipeline["model"].predict(pipeline["scaler"].transform([[Input features here]]))


📦 Requirements

Key dependencies:

pandas
numpy
matplotlib
seaborn
scikit-learn
joblib

Full list available in requirements.txt

📌 Notes

-PCA was skipped because feature selection was used and it reduced data to one dimension (not useful for clustering).
-The project focuses on end-to-end ML pipeline implementation.


## Author

👤 **Abdul Rahman Awad**

- GitHub: [@YourGitHubUsername](https://github.com/abdulrahmanawad3)
