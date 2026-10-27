## Baseline Model Evaluation and Conclusion

A Decision Tree Classifier with `max_depth=2` was evaluated using a holdout test set containing three records.

The Decision Tree achieved an accuracy of 66.67%, precision of 50% for the churn class, and recall of 100% for the churn class. Its confusion matrix was `[[1, 1], [0, 1]]`.

A `DummyClassifier` using the most frequent training class as its prediction achieved the same accuracy of 66.67%. Therefore, the Decision Tree did not outperform the baseline in terms of accuracy on this test set.

The dataset contains only 12 records, and the test set contains only three records. Consequently, these metrics are highly sensitive to individual predictions and cannot establish reliable performance on unseen customers.

**Conclusion:** The Decision Tree is an educational baseline experiment, not a production-ready churn prediction model. Further evaluation requires a larger, representative dataset, appropriate validation, and additional checks for data quality, privacy, and fairness.