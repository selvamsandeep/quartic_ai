### Data Scientist Challenge by Quartic.ai
1. #### **Approach**
     *  Exploratory data analysis: Analyzed the train and test data sets (EDA jupyter notebook)
     *  Imbalanced data set, In train dafa target label has Majority class(0) 96.4%  Minority class 3.6% 
     *  Since data set is got anonymized, scope of future engineering limited
     *  To balance train data, down sampled the majority class (final train set 596K(rows) -> 51K(rows))
     *  Done one hot encoding on the categorical variables having categories upto 4 
     *  To balance the data tried to upsample the minority class with SMOTE (no improvement in result) 
     *  Tried with random forest, logistic regression, lightgbm and xgboot
     
     
 2. #### **Model Details**
     *  Xgboost with 5 fold cross validation and 4 bagging rounds(**xgb_model_cv jupyter notebook**)
     *  Final prediction is mean of 4 predictions 
     *  Since data is highly imbalanced,  so accuracy can not be used to evaluate the model
     *  AUC is used as evaluation metric in xgboost training (approx 64%)
     *  F1 score is used to evaluate the model performance (41.8%)
     *  Total run time 256 seconds in Intel I7 with GLX 1050Ti(HP OMAN)
     *  Submission csv file is in submission folder
     
  3. #### **Work to be done for further improvement**  
     *  Visualize the data with PCA to check both classes Linear separability
     *  Stacking uncorrelated models from different algorithms 
     *  Would have tried with polynominal features from some important features
     
     
     
     
     
   
