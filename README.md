# heart-disease-diagnosis-model
# Heart Failure Prediction Using Machine Learning

## Project Overview

This project aims to predict the presence of heart disease using patient clinical data and multiple machine learning models. Early and accurate prediction can help healthcare professionals in timely diagnosis and treatment planning.

---

## Dataset

- **Source**: [https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction]  
- **Number of samples**: 918  
- **Number of features**: 11 (Age, Sex, ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope)  
- **Target variable**: HeartDisease (0 = No, 1 = Yes)

---

## Data Preprocessing

- Checked for missing values — none found  
- Encoded categorical features using Label Encoding / One-Hot Encoding  
- Feature scaling applied using StandardScaler  
- Train-test split: 80% training, 20% testing

---

## Models and Performance

| Model             | Accuracy  | Precision (Class 0) | Recall (Class 0) | Precision (Class 1) | Recall (Class 1) | F1-Score (Weighted) |
|------------------|-----------|---------------------|------------------|---------------------|------------------|---------------------|
| Logistic Regression | 84.23%    | 0.77                | 0.88             | 0.91                | 0.81             | 0.84                |
| SVM                | 86.41%    | 0.82                | 0.86             | 0.89                | 0.87             | 0.86                |
| Random Forest      | 89.67%    | 0.86                | 0.90             | 0.92                | 0.90             | 0.90                |
| LightGBM           | 88.04%    | 0.85                | 0.87             | 0.90                | 0.89             | 0.88                |

> *Hyperparameter tuning was performed using GridSearchCV for SVM, Random Forest, and LightGBM to optimize performance.*

---

## ROC Curve and AUC

- Random Forest AUC: [0.94]  
- LightGBM AUC: [0.94]

ROC curves were plotted and analyzed for both Random Forest and LightGBM models to compare model discrimination capability.

---

## How to Run

1. Clone this repository  
2. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Open and run 'heart_disease_prediction_model.ipynb` in Google Colab or locally using Jupyter Notebook  
4. Review outputs for model results and visualizations  

---

## Future Work

- Try additional models like XGBoost or Neural Networks  
- Apply cross-validation for more robust generalization  
- Deploy the model as a simple web application (e.g., using Streamlit)  
- Integrate with real-world medical datasets or EHR systems  

---

## Acknowledgements

- Dataset Source: [https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction]  
 
---

## Contact

For questions or collaborations: [yallapragada.yashash@gmail.com]
