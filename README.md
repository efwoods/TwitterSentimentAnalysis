# TwitterSentimentAnalysis
Sentiment Analysis of tweets using the sentiment 140 dataset. Compares &amp; contrasts the efficacy of various modeling techniques. Detects depression in tweets.

## [Dataset](https://www.kaggle.com/datasets/kazanova/sentiment140)

## [Summary]

Baseline Performance
The Bernoulli Naive Bayes, Linear Support Vector Classification, and Logistic Regression models showed baseline performant f1-scores for negative and positive sentiments with values of 82%/83%, 90%/90%, & 87%/87% respectively. These are the goal performance f1-scores and the maximum performance possible to obtain from the test data.

Model Performance Against Test Data
The Bernoulli Naive Bayes, Linear Support Vector Classification, and Logistic Regression models showed f1-scores for negative and positive sentiments when evaluated against test data with values of 80%/80%, 82%/82%, & 83%/83% respectively. This is the performance of the models when used in real-world scenarios against data which is novel to the model.

Tuning
The Linear Support Vector Classification model had the greatest potential performance with f1-scores of 90%, and the Logistic Regression model had the greatest performance against test data. The Logistic Regression model was tuned to maximize the potential of the highest performant model against test data. The potential performant difference of 90% and 87% was chosen to be miniscule, and focus was placed on tuning the model with the highest real-world performance.

Results
After defining a threshold and tuning the Logistic Regression model, f1-score performance remained at the highest of all 3 models. There was a trade-off between recall and precision for negative sentiment with an increase in recall with respect to negative sentiment of 0.03% and a decrease of 0.01% with respect to the precision of negative sentiment. There was a trade-off between recall and precision for negative sentiment with an increase in precision with respect to positive sentiment of 0.02% and a decrease of 0.03% with respect to the recall of positive sentiment. In summary, the tuning did not decrease overall f1-score performance, and increased the ability of the model to precisely detect positive sentiment while increasing the recall of negative sentiment without much cost in precision, recall, or performance.

## Future Work
    - [ ] Serve the custom tuned models with an api
    - [ ] Integrate detection of depression into an application that returns hugs/kindness/love to depressed tweets
    - [ ] Evaluate model implementations of K-Nearest Neighbor, Decision Tree, and Random Forest
    - [ ] Discover insights & tune hyperparameters of the created models with shap, GridCVSearch, & optuna
    - [ ] Develop a utility class for re-use of methods in further research & works
