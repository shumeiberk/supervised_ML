# Supervised machine learning
Employ different techniques to train and evaluate models with unbalanced classes. Jill asks you to use imbalanced-learn and scikit-learn libraries to build and evaluate models using resampling. Your final task is to evaluate the performance of these models and make a recommendation on whether they should be used to predict credit risk.


# Resources
Data Source: LoanStas_2019Q1.csv Software: Python 3.6.1, Jupyter Notebook 6.0.1, Numpy, Sckit Learn, SciPy

# Challenge Analysis:

For both ensemble and resampling credit risk, following similar patterns of pre-processing the original loan_stats data.
- The data was loaded and split into training and testing.  Columns for loan_status was removed to create our features and target was set.
- An objects list was created so that encoding could be applied
- The target values in loan_status was balanced
- The train and test model was run
- Balanced accuracy metric was calculated
- Classifications was created using the imbalanced-learn
- Confusion matrix was displayed for analysis
- All prior results extracted and printed as a summary

Balanced Random Forest Classifier has lower balanced accuracy score of 80% but recall is 67%-90%
Ensemble AdaBoost Classifier has high accuracy in predictions (avg 99%) as well as recall (92%-94%)
AdaBoost Classfier is better than Balanced Random Forest CLassifier

Naive Random Oversampling

balanced_accuracy_score= .66 prec=.01 rec=.74
SMOTE:

balanced_accuracy_score= .65 prec=.01 rec=.62
Undersampling:

balanced_accuracy_score= .64 prec=.01 rec=.62
Combination Sampling:

balanced_accuracy_score= .63 prec=.01 rec=.70
Out of these models, Naive Random Oversampling is the one to recommend since it has the highest balanced accuracy score .66 compared to other models. It also has the highest recall rate of .74 which means that in loans of high risk very few of them would be predicted as low risk

Out of all the models ran, Ensemble AdaBoost remains the better one for precision and recall as well as balanced accuracy (in the 90s) compared to the Naive Random Oversampling and others.


