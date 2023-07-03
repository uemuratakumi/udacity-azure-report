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

By swinging "regularization strength" we can fing the best value against the overlearning.

"Max iterations" swinging is almost for same reason.


And early stopping policy is set by BanditPolicy.(slack_factor = 0.1, evaluation_interval = 1, delay_evaluation= 5 )

By using early stopping policy, we can save cost for lerning.

## 2nd.step: Trial of auto-ML
By using same data with 1st.step, I tried auto-ML and searched best model.

The VotingEbsemnble is choosen as best model.

Since the best model is "ebsemnble", there are a lot of parameters.

So I omit the explanation abount the parameters.

Limited to models without ensemble, LightBGM model has the best accuracy.

And the parametes is set only "min_data_in_leaf":20.

Other top model is almost all LightBGM or XGBoost.

Since these models is often highly rated in competition, the performance is shown in this report too.

## Comparison of hyperdrive and auto-ML
Best model accuracy of hyperdrive is 0.9051.

Best model accuracy of auto-ML is 0.91724.

In hyperparameter tuning, only LogisticRegression is used for algorithm and improve of accuracy is conducted only tuning of hyperparameters.

On the other hand, in auto-ML, other algorithm is used and hyperparameters is tuned comprehensive.

So accuracy of auto-ML is superior compared with hyperdrive.


## The identification of areas to improve the outcome
It is assumed that by using deel lerning technique, the accuracy will be improved since the DL can has more complex structure.

And the more data will lead more acuraccy if we can.
