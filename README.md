# Customer Churn Prediction — Responsible ML

## Project Overview

This project explores customer churn prediction using a small training dataset and a Decision Tree Classifier. It was developed as part of an AI/ML internship task to practise ML problem framing, responsible data documentation, baseline evaluation, and risk identification.

## Objectives

- Define the customer churn prediction problem.
- Document dataset provenance, quality, privacy, and fairness considerations.
- Build and evaluate a baseline machine learning model.
- Compare the Decision Tree with a simple baseline classifier.
- Identify potential risks and safeguards.

## Dataset

- **File:** `customer-churn-training.csv`
- **Records:** 12
- **Columns:** 7
- **Target:** `churned` (0 = not churned, 1 = churned)
- **Missing values:** None detected during the initial check.

The original data source, collection method, and consent status are not documented in the available dataset.

## Features Used

The initial model uses these four numerical features:

- `tenure_months`
- `support_tickets`
- `monthly_spend_inr`
- `last_login_days`

The `customer_id` identifier and `churned` target are excluded from the model inputs. `plan_type` was excluded from this initial experiment because categorical encoding was not included.

## Model and Evaluation

A Decision Tree Classifier with `max_depth=2` was evaluated using a holdout test set.

| Metric | Decision Tree | Dummy Baseline |
|---|---:|---:|
| Accuracy | 66.67% | 66.67% |

Additional Decision Tree metrics for the churn class:

- Precision: 50%
- Recall: 100%

The test set contains only three records. Therefore, these results are preliminary and cannot establish reliable performance on unseen customers.

## Responsible ML Considerations

- Dataset provenance and usage permissions need verification.
- The small sample may not represent the wider customer population.
- Privacy and fairness have not been fully assessed.
- False-positive and false-negative predictions may affect customers.
- The model must not be used alone to make consequential customer decisions.

## Project Deliverables

1. ML Problem-Framing Memo
2. Responsible Data Card
3. Baseline Jupyter Notebook
4. Risk Register

## Limitations and Future Improvements

- Obtain a larger, representative, and well-documented dataset.
- Check duplicate records and outliers.
- Improve validation and perform more detailed error analysis.
- Assess calibration and fairness when sufficient suitable data is available.
- Verify data permissions and privacy requirements before any real-world use.

## Conclusion

This project is an educational ML experiment. The Decision Tree did not outperform the Dummy Baseline in accuracy on the small holdout test set. Further validation is required before considering any real-world application.
