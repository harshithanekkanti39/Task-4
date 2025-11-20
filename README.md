# Logistic Regression

## 1. Introduction

Logistic Regression is a **supervised machine learning algorithm** used for **binary classification**. It predicts the probability of an outcome belonging to a class using the **sigmoid function**.

It is widely used in:

* Fraud detection
* Medical diagnosis
* Customer churn prediction
* Survival prediction (Titanic dataset)

---

## 2. Key Concepts

### **2.1 Sigmoid Function**

Logistic Regression uses the sigmoid function:

[
\sigma(z) = \frac{1}{1 + e^{-z}}
]

This maps values between **0 and 1**, interpreted as probabilities.

### **2.2 Decision Boundary**

Default threshold: **0.5**

* If P > 0.5 → Class 1
* If P ≤ 0.5 → Class 0

Threshold can be tuned based on recall/precision needs.

---

## 3. Dataset Used — Titanic Dataset

The Titanic dataset contains passenger details with the target variable:

* **Survived** (1 = Yes, 0 = No)

Input features typically used:

* Pclass
* Sex
* Age
* Fare
* SibSp
* Parch

---

## 4. Data Preprocessing Steps

### **4.1 Handling Missing Values**

* Drop rows with missing values **or** fill them appropriately.

### **4.2 Encode Categorical Variables**

* Convert "Sex" to numeric values.

### **4.3 Train–Test Split**

* Typical: 80% training, 20% testing.

### **4.4 Feature Standardization**

Standardization improves model convergence:
[
x' = \frac{x - \mu}{\sigma}
]

---

## 5. Model Building (Using Scikit-learn)

A pipeline is created with:

* StandardScaler
* LogisticRegression

### **Training Steps:**

1. Create pipeline
2. Fit model
3. Predict probabilities & classes

---

## 6. Model Evaluation Metrics

### **6.1 Confusion Matrix**

Shows TP, FP, FN, TN.

### **6.2 Precision & Recall**

* Precision: How many predicted positives are correct
* Recall: How many actual positives are detected

### **6.3 ROC Curve & AUC**

* AUC evaluates separability of classes
* Higher AUC → Better model

---

## 7. Threshold Tuning

Model probabilities can be converted to classes using custom thresholds:

* Lower threshold → More recall
* Higher threshold → More precision

Used for:

* Medical models
* Fraud detection

---

## 8. Industry Best Practices

* Use Pipelines to avoid data leakage
* Perform cross-validation for stability
* Analyze class imbalance before training
* Keep feature preprocessing consistent
* Document all transformations

---

## 9. Applications

* Survival prediction (Titanic)
* Customer churn
* Credit risk scoring
* HR attrition analysis

---

## 10. Summary

Logistic Regression is simple yet powerful. With proper preprocessing, threshold tuning, and evaluation, it serves as a strong baseline model for many real-world classification problems.
