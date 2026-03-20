# Phase_3_Project-

Project Overview
 The project overview is solving a classification problem using the SyriaTel Customer Churn dataset to develope a classification model that can accurately identify customers at high risk of churning, allowing the company to implement targeted retention strategies
 
 ## BUSINESS UNDERSTANDING

## Business Problem Definition and Data

**Problem Statement:** Predicting whether a customer will churn (cancel their service) based on their demographic and service usage data.

## Project Objective

** The project objective is developing a classification model that can accurately identify customers at high risk of churning, allowing the company to implement targeted retention strategies. This is a binary classification problem, where the outcome is either 'Churn' or 'No Churn'.

**Data:** The Data set being used is from SyriaTel Customer Churn a a telecommunications company.
          That's the data set i decided to work with for solving the defined business broblem and objectives above
          
## The Stakeholder.

     The Stakeholder is Syriatel

## Modeling, Evaluation, and Conclusion

### Modeling Approach

The project began with the development of a **Logistic Regression** model as a baseline for customer churn prediction. This model served to establish initial performance metrics and highlight areas for improvement. Recognizing the class imbalance inherent in churn datasets (typically far fewer churners than non-churners), a more robust algorithm, the **RandomForestClassifier**, was subsequently introduced. To optimize its performance and ensure it effectively addressed the primary business objective of identifying churners, **hyperparameter tuning** was performed using `GridSearchCV`. The tuning process specifically optimized for the **F1-score**, a metric well-suited for imbalanced classification problems as it balances both precision and recall for the positive class (churners).

### Evaluation Summary

The evaluation of the models focused on their performance on an unseen test set. The key findings were:

1.  **Logistic Regression Baseline:** Achieved an overall accuracy of approximately **86.06%**. However, its ability to identify actual churning customers (recall for class 1) was low at **0.26**, resulting in 72 false negatives (missed churners). Its precision for churners was **0.54**.
2.  **Tuned RandomForestClassifier:** Demonstrated significantly superior performance. Its overall accuracy improved to approximately **91.45%**. Crucially, the recall for the churn class (class 1) drastically increased to **0.66**, meaning it identified 66% of actual churners. This led to a substantial reduction in false negatives, decreasing from 72 to **33**. The precision for churners also improved to **0.73**, indicating fewer false alarms. The F1-score for the churn class saw a significant rise from 0.35 to **0.69**.

### Conclusion

The **tuned RandomForestClassifier** is the recommended model for this customer churn prediction task. Its enhanced performance, particularly its significantly higher recall and reduced false negatives for the churn class, makes it far more valuable for business applications. The model's ability to accurately identify two-thirds of customers at risk of churning provides a strong foundation for implementing targeted retention strategies. Furthermore, the analysis of feature importance revealed that `customer service calls`, `total day charge`, `total day minutes`, and `international plan_yes` are the most influential factors driving churn. These insights are directly actionable, guiding the Syriatel team to focus on improving customer service, optimizing daily usage pricing, and reassessing international plan offerings to proactively mitigate churn and improve customer retention.
