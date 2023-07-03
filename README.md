# Udacity-Azure-ML-First-Report

## Summary of program statement
In this report, I conducted below.
1.The hyperparameter tuning by using pipeline and hypderdrive.
2.Trial of auto-ML
These are adupted to same dataset and I compared the performance of accuracy of model.

## 1st.step: hyperparameter tuning by using pipeline and hypderdrive
In this section, base program (train.py) is prepared in advance.
In "train.py", the sample code of classification problem by using LogisticRegression of slkern is written.
This time sample data (https://automlsamplenotebookdata.blob.core.windows.net/automl-sample-notebook-data/bankmarketing_train.csv) is used for this problem.
By using RandomParameterSampling of hyperdrive, "regularization strength" and "Max iterations".
