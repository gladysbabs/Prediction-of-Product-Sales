# Prediction-of-Product-Sales
## This project is about a sales prediction for food items sold at various stores

**Author**: Gladys Nacuka Babirye Bagandanswa

### Business problem:
The stakeholders need a predictive model to determine and improve future Item_Outlet_Sales (y variable) basing on the provided data about the various features (X variables).

### Data
The Data provided includes a csv file with the statistical data:
and a descriptive data dictionary of all the features and the target variable.

## Methods
 - Data Cleaning: There had to be data cleaning performed on this provided data which steps included: Looking for and addressing Missing values, checking for and addressing inconsistencies in the data, as well as addressing any duplicates within the given data.
 - Exploratory Data Analysis: I analyzed the data so as to obtain the various patterns and relationships of mainly how the features relate with the target variable. Afew of the data visualization methods I used are highlighted below:
   
 ### The pairplot 
This visualization showcased a negative correlation between Item_Outlet_Sales and Item_Visibility (one of the features in the data). This contradicted with the assumption that increased visibility should lead to more Item_outlet_sales. However, further investigation and stakeholder engagement is needed to understand this relationship.
![Pairplot](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/ade1900a-210e-41f8-919c-774c213d0c4e)

### The lmplot
The lmplot visualization additionally potrayed that small outlets predominantly drive most of the Item_Outlet_Sales.
![lmplot](https://github.com/gladysbabs/Prediction-of-Product-Sales/assets/162020572/c132f8b0-dcc0-43d3-8d58-ca60171a96bc)

### Summary
Further investigation and engagement with stakeholders is essential inorder to understand the negative correlation between Item_Visibility and Item_Outlet_Sales. Gathering additional information on promotional activities, shelf placement strategies, market trends, and customer preferences is crucial for developing accurate sales predictions. This comprehensive analysis will help stakeholders make informed decisions to optimize sales strategies and maximize revenue.

## PREDICTIVE MODELS
I tried to predict the Item_Outlet_Sales based on various predictive models which included a linear regression model and a Random Forest model. 

### The Linear Regression Model
The linear regression model performed poorly on the test data with a low r2_score of 0.56 which was similar to the r2_score of the training data.This clearly showed that the model is performing consistently and is not overfitting or underfitting but has however generalized well to unseen data. Even with this observation, the r2_score is not too high and therefore we need to improve the predictive performance of the linear regression model.

### The Random Forest Model
I also went ahead and tested the predictive performance of the Item_Outlet_Sales using the Random forest model, which accounted for about 57% variation in the y_test using the features in X_test. However,the tuned Random Forest model achieved a 0.6 r2_score showing a 60% variability in the true y values(y_test) using the features in the X_test dataset. 

### Comparison results
When I performed a comparison of the Mean_Absolute_Error for both the linear regression model and the tuned Random Forest model,a lower MAE:744.28 is observed for the tuned Random forest model, suggesting a better predictive performance than the linear regression model with an MAE:829.13. This lower MAE for the tuned Random forest model suggests that this model's predictions are closer to the actual Item_Outlet_Sales values on average.

### Conclusion
Based on the metrics provided for evaluating the linear regression model and the random forest model, the Random Forest model with a lower MAE and a high r2_score indicates that it makes more accurate predictions on average.

## FINAL RECOMMENDATIONS

- The linear regression and the random forest models have not performed satisfactorily on their own. Therefore, it’s worth considering using other ensemble methods that combine multiple models, so as to improve predictive performance.

- Even if we go for the Random Forest Model, we still need to continuously evaluate its performance over time so that the model remains effective as data distribution and patterns evolve.
