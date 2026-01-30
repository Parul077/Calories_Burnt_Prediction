# 🔥 Calories Burnt Prediction

## 📌 Project Overview
The objective of this project is to predict **calories burnt during physical activity** based on physiological and activity-related attributes such as age, gender, height, weight, duration, heart rate, and body temperature.

Beyond prediction, this project focuses on:
- Understanding relationships between physical activity metrics and calorie expenditure
- Comparing multiple regression models
- Selecting models based on **generalization and real-world reliability**

This project is designed as an **end-to-end, decision-driven machine learning pipeline**.

---

## 🎯 Problem Statement
Accurately estimating calories burnt during exercise is crucial for:
- Fitness tracking applications
- Health monitoring systems
- Personalized workout planning

The goal is to build a regression model that predicts calorie consumption accurately while evaluating how different machine learning models behave on physiological data.

---

## 🧠 Problem Type
- **Machine Learning Task:** Regression  
- **Target Variable:** `Calories`  
- **Dataset Type:** Structured physiological and activity data
- **Dataset Size:** 15000 records

---

## 🧩 Dataset Description
The dataset includes:
- **Personal attributes:** Age, Gender, Height, Weight  
- **Activity attributes:** Exercise Duration  
- **Physiological signals:** Heart Rate, Body Temperature  

Each row represents one exercise session and the corresponding calories burnt.

---

## ⚙️ Project Workflow
1. Problem understanding  
2. Data exploration and visualization  
3. Feature preprocessing & encoding  
4. Train–test split  
5. Baseline model training  
6. Advanced model training  
7. Model comparison  
8. Bias–variance analysis  
9. Final model selection  

---

## 🔍 Exploratory Data Analysis
EDA revealed strong correlations between:
- Exercise duration and calories burnt
- Heart rate and calorie expenditure

These insights suggested that **non-linear models may capture complex physiological interactions more effectively**.

---

## 🛠 Feature Engineering & Preprocessing
Applied steps include:
- Encoding categorical variables (Gender)
- Feature scaling where required
- Consistent preprocessing to prevent data leakage

**Key Insight:**  
Physiological features carry strong predictive information, making proper preprocessing critical for stable performance.

---

## 🚦 Baseline Model
A **Linear Regression** model was used as the baseline to establish a minimum performance benchmark.

**Observation:**  
While Linear Regression provided reasonable predictions, it showed limitations in capturing complex physiological relationships.

---

## 🤖 Models Evaluated
The following models were trained and evaluated:
- Linear Regression  
- Ridge Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- XGBoost Regressor  

---
## 🔍 Insights from Model Comparison

### Linear & Ridge Regression
- Train R² and Test R² values are both approximately **0.966**, indicating **very low variance**
- However, RMSE remains higher compared to tree-based models

**Inference:**  
Linear models successfully capture the overall trend in calorie expenditure but are unable to model finer, non-linear relationships present in physiological data.

---

### Decision Tree Regressor
- Very high training performance (Train R² ≈ **0.995**)
- Slight drop in test performance (Test R² ≈ **0.991**)
- Significant reduction in RMSE compared to linear models

**Inference:**  
Decision Trees effectively learn non-linear patterns but exhibit mild overfitting due to their high flexibility and sensitivity to data splits.

---

### Random Forest Regressor
- Performance is comparable to linear regression models
- No meaningful improvement in Test R² or RMSE over baseline

**Inference:**  
For this dataset, Random Forest does not provide substantial benefits. This suggests that the underlying feature relationships are either already well captured by simpler models or that the dataset contains limited complex feature interactions.  
This observation reflects appropriate model selection reasoning rather than a model failure.

---

### XGBoost Regressor (Final Model)
- Exceptional training performance (Train R² ≈ **0.999**)
- Strong generalization (Test R² ≈ **0.998**)
- **Lowest RMSE (≈ 2.045)** with minimal train–test gap

**Inference:**  
XGBoost is the best-performing model, effectively capturing both linear and non-linear physiological relationships while maintaining excellent generalization. Its boosting mechanism enables accurate learning from subtle patterns in the data.

---



## 📊 Model Performance Comparison

| Model              | Train R² | Test R² | RMSE ↓ |
|--------------------|----------|---------|--------|
| Linear Regression  | 0.967   | 0.966   | 11.35 |
| Ridge Regression   | 0.967    | 0.966   | 11.35 |
| Decision Tree      | 0.995    | 0.991   | 5.77 |
| Random Forest      | 0.967    | 0.966   | 11.35 |
| XGBoost            | 0.999    | 0.998   | 2.045 |

📌 *Lower RMSE indicates better predictive accuracy.*



---

## 🧪 Bias–Variance Analysis
- Linear & Ridge Regression models exhibit higher bias
- Decision Tree shows strong training performance but risks overfitting
- Random Forest balances bias and variance through ensemble learning
- XGBoost offers high learning capacity but requires careful tuning

This demonstrates that **generalization performance is more important than training accuracy alone**.

---

## ✅ Final Model Selection

XGBoost Regressor was selected as the final model due to:
- Highest Test R² score (0.998)
- Lowest RMSE among all evaluated models
- Minimal train–test performance gap
- Strong ability to model complex physiological relationships

The results indicate that calorie expenditure depends on subtle, non-linear interactions between physiological signals and activity duration, which XGBoost captures effectively.


---

## 📉 Error & Limitation Analysis
Higher prediction errors were observed for:
- Extremely short or long workout sessions
- Outlier physiological measurements

These errors are attributed to limited data availability in extreme scenarios.

---

## 🧾 Results Summary
- Significant improvement over baseline regression
- Reliable calorie predictions for typical exercise sessions
- Demonstrated effectiveness of ensemble models on health data

---

## 💼 Business & Practical Impact
The model can be used in:
- Fitness tracking platforms
- Health monitoring systems
- Wearable device analytics

Accurate calorie estimation supports informed health and fitness decisions.

---

## 📚 Key Learnings
- Physiological and activity data contain strong non-linear signals
- Baseline models are essential for comparison
- Ensemble methods improve robustness
- Model evaluation must focus on generalization, not just accuracy
- Clean preprocessing is critical in health-related ML tasks

---

## 🚀 Future Improvements
- Hyperparameter tuning using cross-validation
- Inclusion of additional biometric features
- Temporal modeling across multiple workout sessions
- Model deployment as an API or app backend

---

## 🧑‍💻 Author
**Parul Singh**  
Machine Learning & Software Development Enthusiast
