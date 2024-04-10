# Prediction-of-Product-Sales
## This project is about a sales prediction for food items sold at various stores

**Author**: Gladys Nacuka Babirye Bagandanswa

### Business problem:
The stakeholders need a predictive model to determine and improve future Item_Outlet_Sales (y variable) basing on the provided data about the various features (X variables).

### Data
The Data provided includes a csv file with the statistical data: https://github.com/gladysbabs/Prediction-of-Product-Sales/blob/main/sales_predictions_2023.csv

And a descriptive data dictionary of all the features and the target variable:https://github.com/gladysbabs/Prediction-of-Product-Sales/blob/main/Sales_predictions%20Data%20Dictionary.png

## Methods
 - Data Cleaning: There had to be data cleaning performed on this provided data which steps included: Looking for and addressing Missing values, checking for and addressing inconsistencies in the data, as well as addressing any duplicates within the given data.
 - Exploratory Data Analysis: I analyzed the data so as to obtain the various patterns and relationships of mainly how the features relate with the target variable. Afew of the data visualization methods I used are highlighted below:
   
 ### The pairplot 
To view the distribution of numerical and categorical features in the dataset.
This visualization showcased a negative correlation between Item_Outlet_Sales and Item_Visibility (one of the features in the data). This contradicted with the assumption that increased visibility should lead to more Item_outlet_sales. However, further investigation and stakeholder engagement is needed to understand this relationship.
![Pairplot](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/ade1900a-210e-41f8-919c-774c213d0c4e)

### The lmplot
To visualize the relationship between two variables (Outlet_Size and Item_Outlet_Sales) and assessing whether there is a linear trend or correlation between them.
The lmplot visualization indeed potrayed that small outlets predominantly drive most of the Item_Outlet_Sales.
![lmplot](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/c132f8b0-dcc0-43d3-8d58-ca60171a96bc)

### Summary
Further investigation and engagement with stakeholders is essential inorder to understand the negative correlation between Item_Visibility and Item_Outlet_Sales. Gathering additional information on promotional activities, shelf placement strategies, market trends, and customer preferences is crucial for developing accurate sales predictions. This comprehensive analysis will help stakeholders make informed decisions to optimize sales strategies and maximize revenue.

## PREDICTIVE MODELS
I tried to predict the Item_Outlet_Sales based on various predictive models which included a linear regression model and a Random Forest model. 

### The Linear Regression Model
The R2-Score of the test set(0.58) is slightly higher than that of the training set(0.56) meaning that the model is performing slightly better on unseen data than on training data. The model is not significantly overfitting or underfitting since the difference in R2-Score between the training and test sets is small.But this could easily suggest that the model is slightly overfitting.
We therefore need to improve the predictive performance of the linear regression model.

### The Default Random Forest Model
I also went ahead and tested the predictive performance of the Item_Outlet_Sales using the Random forest model, which accounted for about 57% variation in the Item_Outlet_Sales in the test set using the features in X_test, while the training set had its r2_score at 0.97 showing that the model is performing very poorly on unseen data and too well on training data. This indeed shows that the model is overfitting.

## COMPARISON RESULTS
### The Default Random Forest Model Vs. Linear Regression Model

For the test data, the Random Forest model has a lower MAE(796.14) compared to the linear regression model MAE(831.44), indicating that Random Forest Model performs better in terms of prediction accuracy. 
However, the linear regression model has a slightly higher R2-score (58%) than the R2-score of the Random Forest Model (57%). This indicates that the linear regression model performs marginally better in explaining the variance in the target variable compared to the Random Forest Model.The difference between the R2-scores of the two models is relatively small, suggesting that their performance in this aspect is comparable.

In summary, when I consider the MAE and r_2 score values, the Random Forest model appears to be a better choice.

### Random Forest Model Vs. Tuned Random Forest Model

- The tuned model's MAE is slightly lower on the test set (762.32) compared to the default model (796.14), indicating improved accuracy.
- The tuned model's MSE is also lower on the test set (1,168,953.33) compared to the default model (1,270,475.71), indicating better performance in terms of error.
- The tuned model's RMSE is lower on the test set (1,081.18) compared to the default model (1,127.15), further confirming improved accuracy.
- The tuned model's R2 score is higher (0.60) compared to the default model (0.57), indicating that the tuned model explains more variance in the target variable.

With an overview of all the metrics,the performance of the tuned Random Forest model has improved compared to the default Random Forest model,showing the effectiveness of tuning a model.

### Tuned Random Forest Model Vs. Linear Regression Model

- The tuned random forest model has its MAE slightly lower on the test set (762.32) compared to the linear model (831.44), indicating improved accuracy.
 - The tuned random forest model has its MSE also lower on the test set (1,168,953.33) compared to the linear model (1,243,333.79), indicating better performance in terms of error.
 - The tuned random forest model has its RMSE lower on the test set (1,081.18) compared to the linear model (1,115.05), further confirming improved accuracy.
 - The tuned random forest model has its R2 score higher (0.60) compared to the linear model (0.58), indicating that the tuned model explains more variance in the target variable.

See below barplot visualization comparing the R2_score of both models:
![R2_score comparison between models](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/c71bca23-a663-495a-93be-a758033f3c72)

- This barplot visualization shows that the tuned random forest model explains a slightly higher proportion of the variance in the target variable compared to the linear regression model.

Also a lineplot showing the MSE predictive performance between the two models :

![MSE comparison between models](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/c30587ed-4221-41c8-b1c2-6d4348f67538)

- The MSE of the tuned Random Forest model is lower than that of the linear regression model, showing that the tuned Random Forest model has a lower predictive error and potentially a better predictive performance.
  
With this overview and visualization,I would recommend the tuned Random Forest model.

## CONCLUSION
Based on the metrics provided for evaluating the linear regression model, the default and tuned random forest model, the tuned Random Forest model with a lower MAE  on the test set (762.32) and a high r2_score (0.60) indicates that the tuned Random forest model makes more accurate predictions on average.

## FINAL RECOMMENDATIONS

- Both the linear regression and default random forest models have demonstrated unsatisfactory performance individually. Thus, it is worth exploring additional avenues for improvement. These may include: conducting further hyperparameter tuning and exploring alternative ensemble methods that integrate multiple models. With this, we can enhance the predictive performance of the models.

- Even if we go for the tuned Random Forest Model, we still need to continuously evaluate its performance over time so that the model remains effective as data distribution and patterns evolve.
