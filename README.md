# BRI Hackathon People Analytics Tim Hmm
- khalidmuhammad1100@gmail.com
- adityasetyabudi1@gmail.com
- bayu.kunto1997@gmail.com

## Submission #1: 21-Feb-2021
- Model used: random forest
- Null rows in training set is removed (only 1 row)
- Model used for submission is trained on whole training data

### 1. Feature transformations
- `gender`: stringified
- `year_graduated` = 2021 - `year_graduated`
- `age` = 2021 - `age`
- `gpa`: if gpa > 4 `->` gpa = 0
- `job_level`: transformed to ordinal
- `person_level`: transformed to ordinal
- `Education_level`: transformed to ordinal
- all remaining categorical are transformed to dummy variables

### 2. Evaluation
Using sklearn's train_test_split with `test_size` = 0.25 and `random_state` = 42
- Accuracy on train set: 1.0
- Accuracy on validation set: 0.8529411764705882
- ROC AUC score on train set: 1.0
- ROC AUC score on test set: 0.5674184550707022

