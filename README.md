# Bank Marketing Term Deposit Subscription Prediction

## Summary
This project explores the prediction of a client's likelihood to subscribe to a term deposit following a bank's telemarketing campaign. We used multiple machine learning models (Logistic Regression, K-Nearest Neighbors, Decision Tree, and Support Vector Machine) to identify key client characteristics affecting subscription success. Grid search and cross-validation were employed to optimize models. Our findings can help the organization to target likely subscribers more efficiently, reducing costs and increasing marketing success rates.

- **Final Jupyter Notebook**: [BankingDataAnalysisFinal.ipynb](./BankingDataAnalysisFinal.ipynb)

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

### Top Features Impacting Logistic Regression Predictions (Simplified Explanation)

The most important features influencing the Logistic Regression model predictions are:

- **Employment Variation Rate (`emp.var.rate`)**  
  A higher (more positive) employment variation rate means better economic conditions. When employment conditions improve, people might feel financially secure and less motivated to lock their money into long-term deposits — leading to a lower likelihood of subscribing.

- **Contact Month - March (`month_mar`)**  
  If the client was contacted in March, they were more likely to subscribe. This could be because March is early in the year, when people are planning their finances, paying taxes, or considering savings options.

- **Consumer Price Index (`cons.price.idx`)**  
  A higher consumer price index means that the cost of goods is rising (inflation). Rising prices may push clients to seek better returns on their money, making a term deposit seem like a safer or smarter choice.

- **Contact Method - Telephone (`contact_telephone`)**  
  Clients who were contacted through a traditional telephone (landline) were less likely to subscribe. This may reflect that landline calls feel less personal or are associated with outdated marketing techniques, making clients less responsive.

- **Success in Previous Campaign (`poutcome_success`)**  
  If the client had a successful outcome in a previous campaign (e.g., said "yes" before), they are much more likely to say "yes" again. Past positive engagement builds trust and makes future subscriptions more likely.



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
