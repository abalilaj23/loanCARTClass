# Comparing Logit Regression with CART for Classification: Loan Decisions  

## Introduction  
This project compares **Logistic Regression (Logit)** and **Classification and Regression Trees (CART)** for predicting loan defaults. The goal is to evaluate their classification performance and optimize the decision tree to maximize profit.  

## Dataset  
The dataset consists of **9,516 loan applications**, each with the following features:  

- **Target Variable:** `default` (1 = default, 0 = no default)  
- **Predictors:**  
  - `installment` – Loan installment amount  
  - `log_income` – Log-transformed income  
  - `fico_score` – Borrower’s credit score  
  - `rev_balance` – Revolving credit balance  
  - `inquiries` – Number of recent credit inquiries  
  - `records` – Number of derogatory records  

## Methodology  

### Logistic Regression Model  
- A **Logit model** was fitted using all predictors.  
- Model performance was assessed using **pseudo R-squared** and statistical significance of coefficients.  
- **Profit calculations** were used to evaluate decision thresholds.  

### CART Model  
- A **Decision Tree Classifier** was trained on the same dataset.  
- The initial tree **overfitted**, requiring **cost-complexity pruning (CCP)** to improve generalization.  
- Profitability was analyzed for different pruning levels to find the **optimal tree**.  

## Key Findings  

### Performance Comparison  
- **Logistic Regression**:  
  - Performed well, achieving a maximum **profit of $153.42** at an optimal cutoff of **0.2**.  
- **Initial Decision Tree**:  
  - Overfitted with **35 depth levels and 2,515 nodes**, leading to poor generalization.  
  - Provided a **maximum profit of $74.26**, much lower than Logit.  
- **Optimized Decision Tree**:  
  - Pruning improved performance significantly.  
  - The **best tree (7 nodes, depth 3)** achieved a **profit of $161.82** at an optimal cutoff of **0.2**, outperforming Logit.  

## Conclusion  
- **Logit Regression provides better interpretability** and strong classification performance.  
- **CART can be highly effective if properly pruned**, leading to a more interpretable decision-making process.  
- **Optimized decision trees outperform Logit in this case**, demonstrating the importance of **hyperparameter tuning** in machine learning models.  

## Repository Contents  
📂 **data/** – Loan dataset.  
📂 **notebooks/** – Jupyter notebooks with model implementation and analysis.  

---

🚀 **Feel free to explore, contribute, or reach out with any questions!**  
