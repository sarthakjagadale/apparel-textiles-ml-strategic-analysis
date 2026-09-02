# Model Evaluation Metrics & Testing Strategy

## 1. Introduction

Model evaluation is an important step in Machine Learning because it determines whether a trained model performs well on unseen data.

In the Apparel & Textiles industry, different Machine Learning problems require different evaluation metrics.

For example, sales prediction is a regression problem, customer purchase prediction is a classification problem, and customer segmentation is a clustering problem.

Therefore, the evaluation metric must match the type of Machine Learning problem.

---

# 2. Evaluation Objectives

The main objectives of model evaluation are:

- Measure prediction performance
- Compare different algorithms
- Identify overfitting
- Identify underfitting
- Validate generalization
- Select the best-performing model
- Understand model errors
- Support business decision-making

---

# 3. Regression Evaluation Metrics

Regression models predict numerical values such as:

- Sales
- Revenue
- Demand
- Product price
- Inventory requirements

## 3.1 Mean Absolute Error (MAE)

MAE measures the average absolute difference between actual and predicted values.

A lower MAE indicates better performance.

### Example

If actual sales are 100 units and predicted sales are 90 units, the absolute error is 10 units.

### Advantages

- Easy to understand
- Expressed in the same unit as the target
- Less sensitive to extreme errors than MSE

### Apparel Application

MAE can measure the average error in predicted product demand.

---

## 3.2 Mean Squared Error (MSE)

MSE calculates the average squared difference between actual and predicted values.

Large errors receive greater penalties because the errors are squared.

### Advantages

- Penalizes large errors
- Useful when large prediction errors are particularly undesirable

### Disadvantage

MSE is sensitive to outliers.

---

## 3.3 Root Mean Squared Error (RMSE)

RMSE is the square root of MSE.

It measures prediction error in the same unit as the target variable.

### Apparel Application

RMSE can measure how far predicted sales or demand are from actual values.

A lower RMSE generally indicates better predictive performance.

---

## 3.4 R² Score

R² measures how much of the variation in the target variable is explained by the model.

A higher R² generally indicates better fit.

However, R² should not be used alone. It should be considered together with error-based metrics such as MAE and RMSE.

---

## 3.5 Mean Absolute Percentage Error (MAPE)

MAPE measures prediction error as a percentage.

It can be useful for understanding forecasting performance in business terms.

### Limitation

MAPE can become problematic when actual values are zero or very close to zero.

---

# 4. Classification Evaluation Metrics

Classification models predict categories or classes.

Examples include:

- Customer will purchase / will not purchase
- Product category
- Customer churn / no churn
- Product return / no return

---

## 4.1 Accuracy

Accuracy measures the proportion of correct predictions.

### Formula

Accuracy = Correct Predictions / Total Predictions

### Advantages

- Easy to understand
- Useful when classes are reasonably balanced

### Limitation

Accuracy can be misleading when the dataset is highly imbalanced.

---

# 5. Confusion Matrix

A confusion matrix summarizes classification predictions.

It contains:

- True Positive (TP)
- True Negative (TN)
- False Positive (FP)
- False Negative (FN)

| | Predicted Positive | Predicted Negative |
|---|---|---|
| Actual Positive | True Positive | False Negative |
| Actual Negative | False Positive | True Negative |

A confusion matrix helps identify the types of mistakes made by the model.

---

# 6. Precision

Precision measures how many predicted positive cases are actually positive.

### Apparel Example

If a model predicts that 100 customers will purchase a product and only 80 actually purchase it, precision is 80%.

Precision is important when false positive predictions have a significant business cost.

---

# 7. Recall

Recall measures how many actual positive cases were successfully identified.

Recall is important when missing a positive case is costly.

### Apparel Example

A model predicting customers likely to purchase a product should have good recall if the business wants to identify as many potential customers as possible.

---

# 8. F1-Score

F1-Score combines Precision and Recall into a single metric.

It is particularly useful when there is a balance between the importance of precision and recall.

F1-Score is useful for classification problems where class imbalance may exist.

---

# 9. ROC-AUC

ROC-AUC evaluates the ability of a classification model to distinguish between classes across different classification thresholds.

A higher ROC-AUC generally indicates better class discrimination.

It can be useful for:

- Purchase prediction
- Churn prediction
- Return prediction
- Customer response prediction

---

# 10. Clustering Evaluation Metrics

Clustering algorithms such as K-Means do not use predefined target labels.

Therefore, different evaluation methods are required.

---

## 10.1 Silhouette Score

The Silhouette Score evaluates how similar observations are to their own cluster compared with other clusters.

A higher score generally indicates better-separated clusters.

### Apparel Application

It can help evaluate customer segments.

---

## 10.2 Inertia

Inertia measures the sum of squared distances between observations and their assigned cluster centers.

Lower inertia generally indicates more compact clusters.

However, inertia usually decreases as the number of clusters increases, so it should not be used alone.

---

## 10.3 Davies-Bouldin Index

The Davies-Bouldin Index evaluates cluster separation and compactness.

A lower score generally indicates better clustering.

---

# 11. Train-Test Split

The dataset should normally be divided into different subsets.

A common structure is:

```text
Dataset
   |
   ├── Training Set
   |
   ├── Validation Set
   |
   └── Test Set
