# Type 2 Diabetes - Risk Predictions

### Objective

Type 2 diabetes is usually diagnosed using the **glycated hemoglobin (A1C)** test. This blood test indicates the average blood sugar level for the past two to three months. Normal levels are below 5.7 percent, and a result between 5.7 and 6.4 percent is considered prediabetes. An A1C level of 6.5 percent or higher on two separate tests means you have diabetes.

In this project we will try to predict A1C levels: no-diabetes, pre-diabetes and diabetes. We will transform the dataset from a regression task (A1C) into a multi-class classification task (3 A1C levels).



### Challenges

We were facing two challenges with our dataset:

- relatively small number of observations
- imbalanced classes (A1C levels)

To overcome the issues with imbalanced data, we will use several techniques:

1. f1 macro averaged score for performance metric
2. cost-sensitive learning (penalize algorithms)
3. SMOTE - Synthetic Minority Over-sampling Technique

and several machine learning algorithms:

1. L_2-regularized Logistic Regression
2. $L$_2-regularized Logistic Regression
3. Support Vector Machine (SVM)
4. Random Forest
5. Gradient Boosting
6. AdaBoost

All together, we have trained 22 models.



### Findings

Our dataset was relatively small and imbalanced and we had to employ several techniques for handling imbalanced classes which  we listed earlier.

We have used six machine learning algorithms listed above, and trained 22 models.

- Plain models, without any of the above listed techniques, did pretty bad with predicting minority classes. They mostly predicted the majority class. Because of that, their accuracy score was high, but f1-macro score was low. As expected, tree ensembles models, were performed slightly better.
- All three techniques listed above, made a positive difference. Again, tree ensemble models produced better performance.

- We could not find one single health condition that could alone increase the risk of being diagnosed with type 2 diabetes. We found that several factors could impact risks for the person to be diagnosed with diabetes: age, high cholesterol ratio, high blood pressure, increased weight... It looks that they are working differently for different people.
- Due to imbalanced data, all models had problems with predicting minority classes: `pre_diabetes` and `diabetes`. They were mostly predicting the majority class, `no_diabetes`.
- At the end, we found that Random Forest algorithm with cost_sensitive learning did the best with f1 macro score of 0.56.



### Tools / Techniques Used:

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
- Numpy
- Seaborn
- Sklearn
- Imblearn



### About Data

The dataset used for this project was obtained from http://biostat.mc.vanderbilt.edu/DataSets. These data are courtesy of Dr John Schorling, Department of Medicine, University of Virginia School of Medicine.

1. ***Data/diabetes.csv*** 

- **Number of records:**      403
- **Columns** (19):
  - id
  - chol
  - stab.glu
  - hdl
  - ratio
  - glyhb
  - location
  - age
  - gender
  - height
  - weight
  - frame
  - bp.1s
  - bp.1d
  - bp.2s
  - bp.2d
  - waist
  - hip
  - time.ppn















