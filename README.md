# Product Sales Classification  
Machine Learning Study on Predicting High vs Low Selling Products  

---

## Overview

This project develops a supervised machine learning model to classify clothing products as **High Selling** or **Low Selling** using structured product attributes such as price, discount percentage, rating, category, size, and season.

The objective is to evaluate whether structured product features alone are sufficient to predict sales performance and to analyze model generalization behavior.

---

## Problem Statement

Given product-level attributes, predict whether a product is:

- 1 → High Selling  
- 0 → Low Selling  

The target variable was created using the median of `sales_count` to ensure a balanced classification problem and avoid class imbalance bias.

---

## Approach

The workflow includes:

1. Exploratory Data Analysis  
2. Data Cleaning & Preprocessing  
3. Target Engineering  
4. Feature Engineering  
5. One-Hot Encoding  
6. Stratified Train-Test Split (80–20)  
7. Random Forest Classification  
8. Model Evaluation & Generalization Analysis  

---

## Model Used

**Random Forest Classifier**

Selected because:
- It handles structured tabular data effectively
- It captures non-linear relationships
- It provides feature importance for interpretability

Two models were evaluated:
- Baseline Random Forest  
- Regularized Random Forest (controlled tree depth and split criteria)

---

## Model Performance

| Model | Training Accuracy | Testing Accuracy |
|-------|-------------------|------------------|
| Baseline RF | 96.63% | 51.25% |
| Regularized RF | 70.31% | 50.00% |

### Key Observations

- The baseline model achieved very high training accuracy but significantly lower testing accuracy, indicating overfitting.
- Regularization reduced model complexity and narrowed the training–testing gap.
- Test performance remained moderate (~50%), suggesting limited predictive separability within the available feature set.

---

## Feature Insights

The most influential features include:

- Price  
- Price-to-Rating ratio  
- Rating  
- Discount-related attributes  

These features contribute to predictions but are insufficient for strong classification performance.

---

## Limitations

The structured product attributes alone may not fully explain sales performance.

Potential improvements could include:

- Marketing exposure data  
- Inventory levels  
- Time-series demand trends  
- Customer behavior metrics  

Incorporating additional business-driven variables may significantly improve predictive capability.

---

## Skills Demonstrated

- Data Cleaning & Preprocessing  
- Feature Engineering  
- Supervised Machine Learning  
- Model Evaluation  
- Bias–Variance & Overfitting Analysis  
- Feature Importance Interpretation  

---

## Repository Structure


```
product-sales-classification/
│
├── product_sales_classification.ipynb
├── dummy_erp_clothing_dataset_2000.csv
├── README.md
├── requirements.txt
└── .gitignore
```

---

## Installation & Usage
```bash
# Clone repository
git clone https://github.com/NarjeenaThanveenPK/product-sales-classification.git
cd product-sales-classification

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook

# Open and run
product_sales_classification.ipynb
```

## Author
Narjeena Thanveen P K