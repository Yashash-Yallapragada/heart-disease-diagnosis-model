# Heart Failure Prediction Using Machine Learning

## Project Overview

This project aims to predict the presence of heart disease using patient clinical data and multiple machine learning models. Early and accurate prediction can help healthcare professionals in timely diagnosis and treatment planning.

---

## Dataset

- **Source**: [Heart Failure Prediction Dataset (Kaggle)](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)  
- **Number of samples**: 918  
- **Number of features**: 11  
- **Target variable**: HeartDisease (0 = No, 1 = Yes)

---

## Data Preprocessing

- Checked for missing values — none found  
- Encoded categorical features using Label Encoding and One-Hot Encoding  
- Feature scaling applied using StandardScaler  
- Train-test split: 80% training, 20% testing

---

## Models and Performance

The following machine learning models were implemented and evaluated:

| Model               | Accuracy  | Precision (0) | Recall (0) | Precision (1) | Recall (1) | F1-Score (Weighted) |
|---------------------|-----------|----------------|-------------|----------------|-------------|----------------------|
| Logistic Regression | 84.23%    | 0.77           | 0.88        | 0.91           | 0.81        | 0.84                 |
| SVM                 | 86.41%    | 0.82           | 0.86        | 0.89           | 0.87        | 0.86                 |
| Random Forest       | 89.67%    | 0.86           | 0.90        | 0.92           | 0.90        | 0.90                 |
| LightGBM            | 88.04%    | 0.85           | 0.87        | 0.90           | 0.89        | 0.88                 |

> *All models were fine-tuned using GridSearchCV for optimal performance.*

---

## Evaluation and Visualizations

- **Confusion Matrix**: Provided for each model to show prediction results  
- **ROC Curve**: Plotted and compared for Random Forest and LightGBM models  
- **Feature Importance**: Displayed using Random Forest and LightGBM  
- **Classification Reports**: Included precision, recall, and F1-scores

---

## How to Run

1. Clone this repository  
2. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

3. Open `Heart_Failure_Prediction.ipynb` in Google Colab or Jupyter Notebook  
4. Run all cells to preprocess data, train models, and evaluate results  

---

## Future Work

- Implement XGBoost and Neural Networks  
- Improve generalization using k-fold cross-validation  
- Deploy the best-performing model using Streamlit  
- Incorporate real-world medical data (e.g., from EHR systems)

---

## Acknowledgements

- Dataset: [Kaggle - Heart Failure Prediction Dataset](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)  
- Thanks to online communities, tutorials, and mentors for their guidance.

---

## License

This project is open source and available under the [MIT License](LICENSE).

---

## Contact

For questions or collaborations: [yallapragada.yashash@gmail.com]
