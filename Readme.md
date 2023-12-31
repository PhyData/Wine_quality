# Predicting the wine quality 
- Ridge and Ridge cross-validation model
- Lasso and Lasso cross-validation model
- Elastic Net model
## Description

In this project I create a Ridge and a RidgeCV model to predict the quality of wines.
The correlation between the features and the target (quality) are not so large which can bring poor performance when using a RidgeCV model.
Another characteristic that reduces the perfomance of the model is the presence of outliers in the dataframe.  Correlations bellow  0.1 (of a maximum of 0.47) are neglected together with outlier in the resultant features. After applying these observations the model reduces the mean squered error from 0.43 to 0.31. Fruthermore along the whole analysis I compare the cases with raw data and scaled one using the well known StandardScaler. The performance between these two cases, the performance improves only by 0.01 in the mean squared error.

In general, the trends of testing data and predicted one is fairly similar, but it have to be carefully looked since the model seems predict with lower values when the test data is abruptly change. 

When Lasso model is applied the errors are similarly applied the MSE is around 0.42, but the model improve up to 0.31 its performance after cleaning the data. Finally, I apply an Elastic Net model where this model combine both Ridge and Lasso formalisms. This model shows that a mse up to 0.31 without cleaning data and even after cleaning the creation performance is equal to that value. I notice that adding the hyper-parameter l1_ratio to ELASTIC-NETCV improves the mse from 0.43 to 0.31.

I consider that for this project the wine quality can be dencently well predicted by the last model tested in this repository.


----
### Author
Dr. Raúl Guerrero
