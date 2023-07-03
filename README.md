# Udacity-Azure-ML-First-Report

## Summary of program statement
In this report, I conducted below.
1.The hyperparameter tuning by using pipeline and hypderdrive.
2.Trial of auto-ML
These are adupted to same dataset and I compared the performance of accuracy of model.

## 1st.step: The hyperparameter tuning by using pipeline and hypderdrive
In this section, base program (train.py) is prepared in advance.
In "train.py", the sample code of classification problem by using LogisticRegression of slkern is written.
This time sample data (https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) is used for this problem.
By using RandomParameterSampling of hyperdrive, "regularization strength" and "Max iterations" is swinged automaticlly.
And early stopping policy is set by BanditPolicy.(slack_factor = 0.1, evaluation_interval = 1, delay_evaluation= 5 )

## 2nd.step: Trial of auto-ML
By using same data with 1st.step, I tried auto-ML and searched best model.
The VotingEbsemnble is choosen.

## Comparison of hyperdrive and auto-ML
Best model accuracy of hyperdrive is 0.90319.
Best model accuracy of auto-ML is 0.91724.

## The identification of areas to improve the outcome
It is assumed that by using deel lerning technique, the accuracy will be improved.
