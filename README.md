# 🔗 Understanding Elastic Net Regression

This project focuses on understanding **Elastic Net Regression** and comparing it with **Linear Regression, Ridge, Lasso, and SGDRegressor (ElasticNet penalty)**.  
Elastic Net combines both **L1 (Lasso)** and **L2 (Ridge)** penalties to balance **feature selection** and **regularization**.

---

## 🛠️ Libraries Used
- Numpy  
- Pandas  
- Matplotlib  
- Scikit-Learn (`LinearRegression`, `Ridge`, `Lasso`, `ElasticNet`, `SGDRegressor`, `train_test_split`, `r2_score`)

---

## 📌 Project Steps

### 1. Dataset
- Imported **Diabetes dataset** from `sklearn.datasets`.  
- Split into **train (80%)** and **test (20%)** using `random_state`.

---

### 2. Models & Results

#### ✅ Linear Regression
- **R² Score:** `0.4399`  

---

#### ✅ Ridge Regression
- Parameters: `alpha = 0.1`  
- **R² Score:** `0.45199`  

---

#### ✅ Lasso Regression
- Parameters: `alpha = 0.1`  
- **R² Score:** `0.44`  

---

#### ✅ Elastic Net Regression
- Parameters:  
  - `alpha = 0.005`  
  - `l1_ratio = 0.9` (favoring Ridge component more than Lasso)  
  - Note: `l1_ratio = a / (a+b)` → balance between L1 and L2.  
- **R² Score:** `0.4531`  

---

#### ✅ SGDRegressor (Elastic Net Penalty)
- Parameters:  
  - `penalty = "elasticnet"`  
  - `alpha = 0.005`  
  - `eta0 = 0.007` (learning rate)  
  - `max_iter = 1000` (epochs)  
- **R² Score:** `0.4256`  

---

## 📊 Observations
- **Linear Regression** is the baseline with moderate performance.  
- **Ridge Regression** improves results by reducing overfitting with L2 penalty.  
- **Lasso Regression** performs slightly worse here, but it helps in **feature selection**.  
- **Elastic Net** balances both Ridge and Lasso → gave the **best performance** (`0.4531`).  
- **SGDRegressor with Elastic Net penalty** performed worse due to sensitivity to learning rate and iterations.  
- Learned how **different penalties change bias-variance tradeoff**.  

---

## 🚀 Next Steps
- Apply these models on **real-world datasets** to test performance.  
- Compare convergence and loss curves of **SGD vs ElasticNet solver**.  
- Tune hyperparameters (`alpha`, `l1_ratio`, learning rate) for best results.  

---

## 📂 File Structure
