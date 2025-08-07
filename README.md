# Final Year Project
# Artificial Neural Networks for Breast Cancer Diagnosis: An Exploration of Performance and Explainability
## About the Project
- This project involved using Machine Learning (ML) to predict breast cancer diagnoses as well as using Explainable Artificial Intelligence (XAI) to help explain the reasoning behind the ML model's prediction.

- The project had two main aims:
  - To investigate the performance of Artificial Neural Networks (ANNs).
    - This was achieved by using performance metrics to evaluate the ANN and comparing its performance to other ML models.
  - To make an ANN model more explainable.
    - This was acheived by using XAI to improve the understanding of relarionships between features and predictions.

- Completed using Python in a Jupyter Notebook
  - Python packages: Pandas, Scikit-learn, SHAP, DiCE.

 ## Dataset and Preprocessing
- Project uses the Wisconsin Diagnostic Breast Cancer (WDBC) dataset from the UCI machine learning repository.
- Used a mapping so that a benign diagnosis is represented by a '0' and a malginant diagnosis is represented by a '1'.
- 80/20 train test split applied to dataset.
- Standardisation applied to the dataset to prevent unequal contributions of certain features due to different measurement scales.

## Machine Learning
- ML models investigated: Artificial Neural Networks (ANN), Support Vector Machine (SVM), Decision Tree (DT), Random Forest (RF), Logistic Regressions (LR).
- Evaluation metrics used: Accuracy, Precision, Recall, F1-score.
- Validation strategy: Stratified 10-fold cross validation.
- ML model hyperparameter selection:
  - Randomised search to help narrow down the optimal set of hyperparameters.
  - Followed by manual adjustment of hyperparameters to investigate effects of performance.
- Performance on the test set shows that the SVM has the best performance, followed by the ANN model.
 
 ### Training (10-fold cross validation) results
![Training results](https://github.com/ElairaP/FYP/blob/main/screenshots/ML_Cross_Validation_results.png)

 ### Test set results
![Test results](https://github.com/ElairaP/FYP/blob/main/screenshots/ML_test_results.png)

## XAI
- XAI methods are applied to the ANN model to investigate the relationships between the dataset features and model predictions. This information is used to explain why the ANN model makes certain predictions.
- Two XAI methods used:
  - Shapely Additive Explanations (SHAP) (Lunderberg and Lee).
  - Diverse Counterfactual Explanations (DiCE) (Mothilal et al.). 

### Examples of XAI Plots
- The figure below shows two SHAP plots.
- The plot on the left shows how much each feature contributes to the ANN model's diagnosis prediction. Higher contributing features are displayed higher on the graph.
- The plot on the right shows how feature values influence the ANN model's predictions.
  - E.g. The graph shows that higher values for the feature 'Radius SE' are more likely to contribute to a malignant prediction whereas lower values are more likely to contribute to a benign prediction.
![SHAP plots](https://github.com/ElairaP/FYP/blob/main/screenshots/SHAP_plots.png)






