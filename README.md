### Heart Failure Prediction Using Machine Learning



##### Project Overview



This project aims to predict the presence of heart disease using patient clinical data and multiple machine learning models. Early and accurate prediction can help healthcare professionals in timely diagnosis and treatment planning.



In addition to standard modeling, this project incorporates model interpretability (SHAP), ensemble learning (stacking and voting), and cost-sensitive threshold optimization to better align predictions with real-world clinical requirements.



##### Dataset

* Source: Heart Failure Prediction Dataset (Kaggle)
* Number of samples: 918
* Number of features: 11
* Target variable: HeartDisease (0 = No, 1 = Yes)

##### 

##### Class Distribution

No Disease: 410 (44.7%)

Disease: 508 (55.3%)



##### Data Preprocessing

Checked for missing values — none found

Encoded categorical features using Label Encoding

Feature scaling applied using StandardScaler (for SVM)

Train-test split: 80% training, 20% testing (stratified)



##### Models and Performance



The following machine learning models were implemented and evaluated:



| Model             | Accuracy  | Precision (Class 0) | Recall (Class 0) | Precision (Class 1) | Recall (Class 1) | F1-Score (Weighted) |
|------------------|-----------|---------------------|------------------|---------------------|------------------|---------------------|
| Logistic Regression | 84.23%    | 0.77                | 0.88             | 0.91                | 0.81             | 0.84                |
| SVM                | 86.41%    | 0.82                | 0.86             | 0.89                | 0.87             | 0.86                |
| Random Forest      | 89.67%    | 0.86                | 0.90             | 0.92                | 0.90             | 0.90                |
| LightGBM           | 88.04%    | 0.85                | 0.87             | 0.90                | 0.89             | 0.88                |


> \\\*All models were fine-tuned using GridSearchCV for optimal performance.\\\*



\---





##### Additional Models

* Stacking Classifier
* Base models: Logistic Regression, SVM, Random Forest, LightGBM
* Meta-learner: Logistic Regression
* Voting Classifier



##### Model Interpretability (SHAP)

* Used SHAP (SHapley Additive Explanations) for model interpretability

###### Top Important Features

* ST\_Slope
* ExerciseAngina
* ChestPainType
* Oldpeak
* Cholesterol

###### Insights

* ST\_Slope is the most influential feature
* Higher MaxHR is associated with lower disease probability
* Oldpeak significantly increases disease risk
* Feature interactions observed (e.g., Age and MaxHR)
* 

##### Cost-Sensitive Threshold Optimization



To address the higher cost of false negatives in medical diagnosis:



* Compared multiple threshold strategies:
* Default threshold (0.5)
* Youden’s J statistic
* Cost-sensitive threshold
* Recall-targeted threshold

###### Key Result

* Cost-sensitive threshold reduced false negatives from 11 to 3 (73% reduction)
* Achieved recall of 0.97 with a slight drop in accuracy



##### Evaluation and Visualizations

* Confusion Matrix for all models
* ROC Curve (AUC > 0.90 for all models)
* Precision-Recall Curve
* Feature Importance (Random Forest and LightGBM)
* SHAP visualizations for interpretability



##### Calibration Analysis

* Random Forest and Stacking models show well-calibrated probabilities
* LightGBM shows slight overconfidence
* Calibration can be improved using Platt scaling or isotonic regression



##### How to Run

1. Clone this repository
2. Install dependencies:
3. pip install -r requirements.txt
4. Open heart\_disease\_prediction\_ml\_model.ipynb in Google Colab or Jupyter Notebook
5. Run all cells to preprocess data, train models, and evaluate results



##### Future Work

* Implement XGBoost and Neural Networks
* Improve generalization using k-fold cross-validation
* Deploy the model using Streamlit
* Perform external dataset validation
* Explore fairness analysis and uncertainty estimation



##### Acknowledgements

* Dataset: Kaggle - Heart Failure Prediction Dataset
* Thanks to online communities, tutorials, and mentors for their guidance



##### License

This project is open source and available under the MIT License

.



##### Contact



For questions or collaborations: yallapragada.yashash@gmail.com

