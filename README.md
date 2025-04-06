# ✈️ Flight Delay Prediction using Regression Models

This project focuses on predicting flight delays using various regression models: Linear Regression, Random Forest, K-Nearest Neighbors (KNN), and Ridge Regression. The dataset is split into three subsets for evaluation: **Combined**, **Arrivals**, and **Departures**.

📂 **Dataset:**  
We use the [U.S. Department of Transportation Flight Delays Dataset](https://www.kaggle.com/datasets/usdot/flight-delays) available on Kaggle.

---

## 📊 Models Evaluated
- Linear Regression
- Random Forest
- K-Nearest Neighbors (KNN)
- Ridge Regression

---

## 📈 Evaluation Metrics

We use the following metrics to evaluate the performance:
- **MAE**: Mean Absolute Error
- **MSE**: Mean Squared Error
- **Accuracy @ t-minutes**: Proportion of predictions within t minutes of the actual delay
- **Confusion Matrix & F1 Score**: For classification accuracy based on delay thresholds

---

## 📋 Results Summary

### 🔹 Combined Dataset
| Model             | MAE    | MSE    | Accuracy@15 | Accuracy@60 | Accuracy@90 |
|------------------|--------|--------|-------------|-------------|-------------|
| Linear Regression| 14.179 | 848.469| 0.875       | 0.964       | 0.977       |
| Random Forest    | 13.412 | 777.975| 0.838       | 0.961       | 0.979       |
| KNN              | 14.050 | 900.283| 0.877       | 0.965       | 0.980       |
| Ridge Regression | 14.179 | 848.468| 0.875       | 0.964       | 0.977       |

**MAE Rankings:**
1. 🥇 Random Forest (13.412)  
2. 🥈 KNN (14.050)  
3. 🥉 Linear & Ridge Regression (14.179)  

---

### 🔹 Arrivals Dataset
| Model             | MAE    | MSE    | Accuracy@15 | Accuracy@60 | Accuracy@90 |
|------------------|--------|--------|-------------|-------------|-------------|
| Linear Regression| 9.035  | 165.747| 0.932       | 0.986       | 0.993       |
| Random Forest    | 9.445  | 180.263| 0.924       | 0.985       | 0.992       |
| KNN              | 12.256 | 298.031| 0.920       | 0.983       | 0.991       |
| Ridge Regression | 9.035  | 165.747| 0.932       | 0.986       | 0.993       |

**MAE Rankings:**
1. 🥇 Linear & Ridge Regression (9.035)  
2. 🥈 Random Forest (9.445)  
3. 🥉 KNN (12.256)  

---

### 🔹 Departures Dataset
| Model             | MAE    | MSE     | Accuracy@15 | Accuracy@60 | Accuracy@90 |
|------------------|---------|---------|-------------|-------------|-------------|
| Linear Regression| 17.098  | 1248.703| 0.815       | 0.944       | 0.967       |
| Random Forest    | 16.921  | 1341.066| 0.756       | 0.939       | 0.967       |
| KNN              | 13.938  | 1311.312| 0.851       | 0.953       | 0.972       |
| Ridge Regression | 17.098  | 1248.700| 0.815       | 0.944       | 0.967       |

**MAE Rankings:**
1. 🥇 KNN (13.938)  
2. 🥈 Random Forest (16.921)  
3. 🥉 Linear & Ridge Regression (17.098)  

---

## 🔄 Confusion Matrix & F1 Scores

Each model was also evaluated for binary classification based on delay (e.g., significant delay vs. on-time). Here's the F1 score and confusion matrix for each:

### ✅ Combined Dataset
| Model              | F1 Score | TP     | TN     | FP     | FN     |
|-------------------|----------|--------|--------|--------|--------|
| Linear Regression | 0.605    | 6770   | 13762  | 3674   | 4437   |
| Random Forest     | 0.651    | 7383   | 13941  | 3495   | 3824   |
| KNN               | 0.595    | 6376   | 14589  | 2847   | 4831   |
| Ridge Regression  | 0.605    | 6770   | 13762  | 3674   | 4437   |

### ✅ Arrivals Dataset
| Model              | F1 Score | TP     | TN     | FP     | FN     |
|-------------------|----------|--------|--------|--------|--------|
| Linear Regression | 0.799    | 2297   | 7031   | 1248   | 939    |
| Random Forest     | 0.791    | 2292   | 6940   | 1339   | 944    |
| KNN               | 0.740    | 2124   | 6693   | 1586   | 1112   |
| Ridge Regression  | 0.799    | 2297   | 7031   | 1248   | 939    |

### ✅ Departures Dataset
| Model              | F1 Score | TP     | TN     | FP     | FN     |
|-------------------|----------|--------|--------|--------|--------|
| Linear Regression | 0.341    | 4473   | 5840   | 2595   | 3977   |
| Random Forest     | 0.410    | 5056   | 5717   | 2718   | 3394   |
| KNN               | 0.380    | 4813   | 5794   | 2641   | 3637   |
| Ridge Regression  | 0.341    | 4473   | 5840   | 2595   | 3977   |

---

## 🥇 Conclusion

### 🔹 Best Overall Model:
- **🏆 Random Forest** achieved the **lowest MAE and MSE** on the **combined dataset**, making it the most accurate in terms of continuous delay prediction.
- However, **Linear and Ridge Regression** had slightly better **F1 scores**, showing stronger classification performance.

### 🔹 Best for Arrivals:
- **🏆 Linear and Ridge Regression** stood out with the **best F1 score (0.799)**, **lowest MAE (9.035)**, and **highest accuracies** at all thresholds.

### 🔹 Best for Departures:
- **🏆 Random Forest** had the **highest F1 score (0.410)**, showing better classification performance.
- **🏅 KNN** had the **lowest MAE (13.938)** and **highest regression accuracy**, making it a strong candidate for continuous prediction.

---

✅ This comparative analysis shows that **no single model is best for all scenarios**.  
**Model selection should depend on the specific subproblem** (Arrivals vs. Departures) and the **evaluation metric that matters most** for your use case (e.g., MAE for regression tasks or F1 Score for classification).

---
