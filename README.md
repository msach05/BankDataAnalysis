# Bank Marketing Term Deposit Subscription Prediction

## Summary
This project explores the prediction of a client's likelihood to subscribe to a term deposit following a bank's telemarketing campaign. We used multiple machine learning models (Logistic Regression, K-Nearest Neighbors, Decision Tree, and Support Vector Machine) to identify key client characteristics affecting subscription success. Grid search and cross-validation were employed to optimize models. Our findings can help the organization to target likely subscribers more efficiently, reducing costs and increasing marketing success rates.

- **Final Jupyter Notebook**: [BankingDataAnalysisFinal.ipynb](./BankingDataAnalysisFinal.ipynb)
- **Dataset Source**: [Moro et al., 2014](http://dx.doi.org/10.1016/j.dss.2014.03.001)

---

## Project Organization
- The project consists of the cleaned dataset, a final Jupyter Notebook with clear headings, explanations, and visualizations.
- No unnecessary files are included.
- Appropriate directory structure and file naming conventions have been maintained.

---

## Business Understanding
Banking institutions rely on targeted marketing campaigns to promote term deposit products. Identifying customers most likely to subscribe can lead to:
- Increased campaign efficiency for more term deposits
- Reduced operational costs
- Better management of human and time resources

The objective was to create a predictive model to assist marketing teams in prioritizing high-probability customers. 

---

## Modeling Approach

**Models Used:**
- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)

**Techniques Applied:**
- **Cross-validation** to ensure model generalization.
- **Grid search** to tune hyperparameters (e.g., `C` in Logistic Regression, `k` in KNN, tree depth in Decision Tree).
- **Interpretation of coefficients and feature importances** to explain model behavior.

**Evaluation Metric:**
- **Accuracy** was used as the primary evaluation metric due to the business need for identifying correct customer classification.

---

## Key Findings

**Top Features (Logistic Regression):**
- `emp.var.rate`
- `month_mar`
- `cons.price.idx`
- `contact_telephone`
- `poutcome_success`

**Model Performance Summary:**

| Model                 | Train Time | Train Accuracy | Test Accuracy         |
|------------------------|------------|----------------|-----------------------|
| Logistic Regression    | Fast       | High (~90%)    | High (~90%)           |
| K-Nearest Neighbors    | Medium     | Slightly lower | Slightly lower        |
| Decision Tree          | Fast       | Overfit        | High (lower than LR)  |
| Support Vector Machine | Long       | Very High      | High  (lower than LR) |

**Interpretation:**
- Logistic Regression and Decision Tree models performed best when balancing interpretability and accuracy.
- SVM offered high accuracy but had high training time and complexity.
- KNN was less interpretable and sensitive to hyperparameters.

### Actionable Insights
- Target customers during favorable months like March.
- Customers with positive previous campaign outcomes are much more likely to subscribe.
- Economic indicators like employment rate and consumer confidence significantly affect customer decisions.

---
