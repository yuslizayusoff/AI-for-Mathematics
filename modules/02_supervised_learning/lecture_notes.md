# Module 2: Supervised Learning
## Duration: 60 minutes

### Learning Objectives
By the end of this module, students will understand:
- ✅ What supervised learning is and when to use it
- ✅ Mathematical foundations of regression
- ✅ Mathematical foundations of classification
- ✅ How to evaluate model performance
- ✅ Hands-on implementation with real datasets

---

## Part 1: Introduction to Supervised Learning (10 minutes)

### 1.1 What is Supervised Learning?

**Definition:** Learning from labeled data (input → output pairs)

**Two Main Types:**
1. **Regression**: Predict continuous values (price, temperature, age)
2. **Classification**: Predict categories (spam/not spam, cat/dog/bird)

---

## Part 2: Regression (25 minutes)

### 2.1 Linear Regression

**Problem:** Find the best-fit line through data points

```
y = mx + b
```

### 2.2 Loss Function: Mean Squared Error (MSE)

**Why we need a loss function:**
- Measures how wrong our predictions are
- Used to train the model

```
MSE = (1/n) × Σ(actual_i - predicted_i)²
```

### 2.3 Training Linear Regression

**Method 1: Gradient Descent (Iterative)**
- Start with random weights
- Calculate gradient of MSE
- Update weights
- Repeat until convergence

**Method 2: Normal Equation (Analytical)**
```
w = (X^T X)^(-1) X^T y
```

---

## Part 3: Classification (20 minutes)

### 3.1 Binary Classification Problem

**Problem:** Predict yes/no, spam/not spam, cat/dog, etc.

### 3.2 Logistic Regression

**Sigmoid Function:**
```
σ(z) = 1 / (1 + e^(-z))
```

**Logistic Regression Model:**
```
p = σ(w^T x + b)
```

**Prediction Rule:**
- If p > 0.5: predict class 1
- If p ≤ 0.5: predict class 0

### 3.3 Binary Cross-Entropy Loss

**Loss function for classification:**
```
BCELoss = -(1/n) × Σ[y_i × log(p_i) + (1-y_i) × log(1-p_i)]
```

---

## Part 4: Model Evaluation (5 minutes)

### 4.1 Regression Metrics

**Mean Absolute Error (MAE):**
```
MAE = (1/n) × Σ|actual - predicted|
```

**R² Score:**
```
R² = 1 - (SS_residual / SS_total)
```

### 4.2 Classification Metrics

**Accuracy, Precision, Recall, F1 Score**

---

## Key Takeaways

| Topic | Formula | Use Case |
|-------|---------|----------|
| **Linear Regression** | y = w^T x + b | Predicting continuous values |
| **MSE Loss** | (1/n)Σ(y - ŷ)² | Regression training |
| **Logistic Regression** | p = 1/(1+e^(-z)) | Binary classification |
| **Binary Cross-Entropy** | -Σ[y log p + (1-y)log(1-p)] | Classification training |

---

## Next Steps
- Complete notebook: `02_regression_classification.ipynb`
- Implement from scratch
- Train on real datasets
- Compare different algorithms