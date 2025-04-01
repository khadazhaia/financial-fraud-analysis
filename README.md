# Financial Fraud Analysis and Detection 

This project uses a logistic regression model to detect fraudulent transactions from a large dataset of financial transactions. The primary goal is to accurately classify whether a transaction is fraudulent or not

## Exploratory Data Analysis (EDA)

Out of 6 million transactions, less than 1% are fraudulent.

There are 5 types of transactions, with cash out being the most common.

Only cash out and transfer transactions are fraudulent, and they tend to involve higher transaction amounts.

Fraudulent transactions remain relatively steady over time, while not fraudulent transactions show high variability and a dramatic decrease after step 400.

Transfer transactions have the highest median and the widest range, indicating variability in the amounts. Payment and debit transactions generally involve smaller amounts, while cash in and cash out transactions are moderate in size but show some large outliers.

## Data Preprocessing (Clean)

Dropped step column as fraudulent transactions remained steady over time, indicating no significant trend.

Dropped nameDest and nameOrig as these features did not add any predictive value.

Dropped isFlaggedFraud because it contained only 16 instances of flagged fraud, which is too small and irrelevant compared to the entire dataset.

## Model Evaluation (Logistic Regression)

Initial Model Accuracy Score: 0.9989

Optimized Parameter Model Accuracy Score: 0.9979

Optimized Threshold Model Accuracy Score: 0.9978

Initial F1 Score: 0.64

Optimized Parameter F1 Score: 0.50

Optimized Threshold F1 Score: 0.49

## Conclusion

The initial model had the highest F1 score, indicating a better precision-recall balance.

The optimized models improved recall (identifying more fraud) at the cost of reduced precision.

The model is highly accurate, but the choice of the threshold affects the trade-off between detecting fraud and minimizing false positives.
