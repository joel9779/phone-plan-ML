# phone-plan-ML
phone plan ML
# 📌 Megaline Plan Recommendation Model

## 📖 Introduction
The purpose of this project is to analyze subscribers' behavior and recommend one of Megaline's newer plans: **Smart or Ultra**. The goal is to achieve an **accuracy above 75%** to ensure reliable recommendations.

## 📂 Dataset Overview
The dataset consists of **3,214 subscriber records** with the following features:
- `calls` - Number of calls made by the subscriber.
- `minutes` - Total minutes used.
- `messages` - Number of messages sent.
- `mb_used` - Mobile data used (MB).
- `is_ultra` - Target variable (1 = Ultra plan, 0 = Smart plan).

### ✅ Data Preprocessing:
- Checked for missing values (None found).
- Explored statistical properties of the dataset.
- Split into **Training (75%)**, **Validation (12.5%)**, and **Test (12.5%)** sets.

## 🏗️ Model Selection & Evaluation
### **1️⃣ Logistic Regression**
- **Accuracy:** 76.6% on validation data.
- **Good generalization** but lower accuracy than Random Forest.

### **2️⃣ Random Forest Classifier** (Best Performing Model)
- **Best hyperparameters** (found via GridSearchCV):
  - `max_depth=10`, `min_samples_split=2`, `n_estimators=50`
- **Validation Accuracy:** 81.0%
- **Test Accuracy:** 79.8%
- **Training Accuracy:** 89.1%
- **Sanity Check Passed:** The difference between train/test accuracy is within acceptable range (**<10%**), meaning no significant overfitting.

## 🎯 Final Model Evaluation on Test Set
| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | 76.1%    |
| Random Forest       | **79.8%** |

## 🔍 Overfitting Check
- The **difference between training and test accuracy is within 10%**, meaning the model generalizes well.
- **Random Forest performed better** than Logistic Regression, making it the best choice for deployment.

## 🚀 Conclusion
- **Random Forest** provides the highest accuracy (79.8%) and generalizes well.
- The model is **ready for deployment** to recommend **Smart vs. Ultra plans** based on user behavior.

## 📌 Future Improvements
- Experiment with **other ML models** (e.g., XGBoost, SVM).
- Collect more data for improved model generalization.
- Fine-tune hyperparameters further for **even better accuracy**.

---
📢 **Recommendation:** Use **Random Forest Classifier** for Megaline’s plan recommendation system. ✅

