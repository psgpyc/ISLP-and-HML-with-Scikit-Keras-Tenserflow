# Conceptual Questions

## Question 1:

For each of parts (a) through (d), indicate whether we would generally
expect the performance of a fexible statistical learning method to be
better or worse than an infexible method. Justify your answer.


**(a) The sample size n is extremely large, and the number of predictors p is small.**

The performance of flexible statistical learning models will be **better** in this case. 

The large sample size(n) will provide abundent data to estimate the complex pattern in data more accurately(better fitting the data).  Also, the small number of predictors(p) will help reduce the problem of overfitting of data(dimentionality curse).

**(b) The number of predictors p is extremely large, and the number
of observations n is small.**

The performance of flexible statistical model will be **worse** in this case. Due to smaller number of observation(n) and extremely large predictors(p) flexible models suffer from overfitting issue.

**(c) The relationship between the predictors and response is highly
non-linear.**

In this case, we will expect flexible model to **perfrom** better as flexible models are good at modelling non-liner relationships. Also, the bias is smaller for flexible models when dealing with non-liner relationship.  If we use a stricter model, then the bias will be much higher.

**(d) The variance of the error terms, i.e. σ2 = Var("), is extremely
high.**

In this case, we expect flexible model to perfrom **worse**. The variance increases as the flexibility increases.



## Question 2:

Explain whether each scenario is a classifcation or regression problem, and indicate whether we are most interested in inference or prediction. Finally, provide n and p

**(a) We collect a set of data on the top 500 firms in the US. For each firm we record profit, number of employees, industry and the CEO Salary. We are interested in understanding which factors affect CEO Salary.** 

Here, n = 500 and p = 3.

This is a regression problem and we are most interested in inference, as the goal is to understand which factors affect CEO salary.


**(b) We are considering launching a new product and wish to know whether it will be a success or failure. We collect data on 20 similar products that were priviously launched. For each product we have recorded whether it was a success or failure, price charged for the product, marketing budget, competition price, and ten other variables.**

Here, n=20 and p=13

This is a classification problem, as we are trying to predict a binary outcome (success or failure). We are interested in making prediction.

**(c) We are interested in predicting the % change in the USD/Euro exchange rate in relation to the weekly change in the world stock markets. Hence we collect weekly data for all of 2012. For each week we record the % change in the USD/Euro, the % change in the US market, the % change in the British market, and the % change in the German market.** 

Here, n=52 and p=3

This is a regression problem, as we are trying to predict a continuous variable (% change in USD/Euro exchange rate). We are interested in making prediction.



## Question 3:

We now revisit bias-variance decomposition.

**(a) Provide a sketch of typical (squared) bias, variance, training error, test error, and Bayes (or irreducible) error curves, on a single plot, as we got for less flexible statistical learning methods towards more flexible approaches. The x-axis should represent the amount of flexiblity in the method, and the y-axis should represent the values for each curve. There should be five curves. Make sure to label each one.**


Will add the graph from Ipad Later

**(b) Explain why each  of the five curves has the shape displayed in part (a).**

**Squared bias:** Bias is introduced because our approximation(function which we assumed to explain the underlying relationship) is different than the true underlying relationship. 
For example, assuming the relationship is linear when the true underlying relationsip is not.
As the model gets flexible, the function will be more and more similar to the true underlying function                   reducing the squared bias.

**Variance:** The variance is the difference between the predicted value and the actual one. As the model gets flexibe, it fits the data more closely by capturing intricate patterns and relationship in data. Due to this, even a slight change to data point will increase variance.

**Training Error:** Trainig error is given by the average of the difference between the predicted value and actual value.                    Flexible models fit the data better than the inflexible models, hence reducing the Training error.

**Test Error:** The Expected test error is given by the formula, 

            Test Error = Variance + Bias + Irreducible Error 
            

The Test error follows a u-shaped curve. Initially, the test error decreases as the flexibility increases, but will start to rise again after a certain point. This is because, flexible models has high variance. The test error will be the lowest, if the each of the above values are less. 

**Bayes (or Irreducible) error curve:** This is a constant value and is not dependent on the predictors or the flexibility of the statistical model.


        

## Question 4:

You will now think of some real-life applications for statistical learning.


**(a) Describe three real-life applications in which *classification* might be useful. Describe the response, as well as the predictores. Is the goal of each application inference or prediction? Explain your answer.**

The three real-life applications:

1. Based on life-style choices and heridietary factors, classifying weather the person is likely to get diabeties or not.
   
   The goal is to make **prediction.**
   
   Possible predictors: age, gender, Ethnicity, BMI, Blood Pressure, Family history of diabeties, average sleep duration,     average physical activity duration, smoker, alcohol consumption.

   Response variable(binary): 1 for likely to have diabetes, 0 for otherwise

2. Predicting Customer Churn in subscription based services like Netflix
   The goal is to make **prediction**

   Possible predictors: date_joined, frequency_of_use, subscription_amount, average_watch_hours, watch_list_count

   Response Variable(binary): 1 for likely to leave, 0 for otherwise

3. Detecting fraudulent  Financial Transactions:

   The goal is to make **prediction**

   Possible predictors: Transaction Amount, Time of Transaction, Geographical Location, Transaction frequency, login_in_device_id

   Response Variable(binary): 1 for legitimate , 0 for fraudalent

   

**(b) Describe three real-life applications in which regression might be useful. Describe the response, as well as the predictors. Is the goal of each application inference or prediction? Explain your answer.**

1. Identifying factors associated with customer purchasing behaviour in ecommerce platform

   The goal is to make **Inference** 

   Possible Predictors: past_purchase_behaviour, number_of_marketing_emails_opened, time_spent_in_seconds_in_website, customer_age, number_of_time_item__is_viewed.

    Response Variable: Identifying which predictors are most likely to influence the purchasing behaviour.

2. Rental Price prediction for apartments in London

   The goal is to make **prediction** and **Inference**

   Possible Predictors: no_of_bedrooms, no_of_baths, total_area, parking_space, no_of_balcony, kitchen_type(modern, traditional), council_tax_band, enery_rating_band, has_living_space, furnished

   Response Variable: Price (if prediciton) and Identifying which predictors are most likely to influence purchasing behaviour(if inference)

3. Predicting cost of living index based on economic factors.

   The goal is to make **inference** and **prediction**

   Possible Predictors: Inflation rate, avg_housing_price, energy_prices, food_prices, unemployment_rate, average_wage_growth

   Response Variable: cost of living index(prediction) and identifying which predictors has most significant impact on the cost of living

   

**(c) Describe three real_life applications in which *cluster analysis* is useful.**

1. Recommendation system used for streaming platfroms like Netflix, Disney +, Youtube to recommend your next watch based on your browsing histroy, reviews, ratings.
2. Cluster Analysis for grouping customers into different segments based on their purchasing habit like category_of_purchase, purchasing_amount, return/refund types and frequency
3. Clustering differnt treaking routes in Nepal based on popularity amongst the treakers.



## Question 5

What are the advantages and disadvantages of a very flexible (versus a less flexible) approach for regression or classification? 

Under what circumstances might a more flexible approach be preffered to a less flexible approach? 

When might a less flexible approach be preffered?

**Advantage**

The flexible models have less bias as compared to less flexible models and makes better prediction given larger datasets.

**Disadvantages:**

But, flexible models are less interpretable than flexible ones. 

Risk of overfitting.

Computationally demanding.

**Circumstances where a more flexible approach be preffered to a less flexible approach?**

1. large sample data sets and less predictors
2. Non-linear relationship between predictor and response variable

**Circumstances where a less flexible approach be preffered to a flexible approach?**
1. When we are trying to make inference(to identify relationship between two variables)
2. smaller sample size but larger predictors
3. High variance of error terms.



## Question 6

Describe the difference between a parametric and a non-parametric statistical learning approach. What are the advantages of a parametric approach to regression or classification (as opposed to a non-parametric approach)? What are its disadvantages?

**Parametric Model** are less flexible and make strong assumptions about the function form(like linear or polynomial).

These models are simpler and interpretable.

These models are less computationally intensive.

**Parametric Models** are preferred when the sample is smaller. Also, if interpretability  is crucial.

**Non Parametric Model** are flexible and hence make fewer assumptions about the shape of the function. 

These models are complex and less interpretable.

These models are computationally intensive.


**Non Parametric Models** are preferred when we have larger sample dataset with high number of predictors.


**Parametric Model** are less flexible and make strong assumptions about the function form(like linear or polynomial).

These models are simpler and interpretable.

These models are less computationally intensive.

The major disadvantage: As it makes assumption of the functional form, the model might not be able to capture pattern in the data adequately.

**Parametric Models** are preferred when the sample is smaller. Also, if interpretability  is crucial.

**Non Parametric Model** are flexible and hence make fewer assumptions about the shape of the function. 

These models are complex and less interpretable.

These models are computationally intensive.


**Non Parametric Models** are preferred when we have larger sample dataset with high number of predictors.



## Question 7

The table below provides a training data set contains six observations, three predictors, and one qualitative response variable.

![image](https://github.com/user-attachments/assets/a2946d68-0277-4729-bfb1-c82d058d866a)


Suppose we wish to use this data set to make a prediction for Y when X<sub>1</sub> = X<sub>2</sub> = X<sub>3</sub> = 0 using k-nearest neighbour.


**(a) Compute the Euclidean distance between each observation and the test point, X<sub>1</sub> = X<sub>2</sub> = X<sub>3</sub> = 0.**


```python
import numpy as np
import pandas as pd
```


```python
df = pd.DataFrame({
    'X1': pd.Series([0,2,0,0,-1,1]),
    'X2': pd.Series([3,0,1,1,0,1]),
    'X3': pd.Series([0,0,3,2,1,1]),
    'Y': pd.Series(['Red','Red','Red','Green', 'Green', 'Red'])
})
df.index = np.arange(1,7)
```


```python
df['euc_distance'] = np.sqrt(df['X1']**2+df['X2']**2+df['X3']**2)
```

**(b) What is our prediction wuth k = 1? Why?**


```python
df.sort_values(by='euc_distance')
```
![image](https://github.com/user-attachments/assets/d75a0e53-b26e-4cf9-a837-515060f90699)

For k=1, our prediction is Green. Green is the closest neighbour.

**(c) What is our prediction with k = 3? Why?**

For k = 3, We have three neighbours (Green, Red, Red). As the mode of Red is greater than of Green, our prediction will be Red.

**(d) If the Bayes decision boundary in this problem is highly non-linear, then would we expect the best value of K to be large or small? Why?**

If the Bayes decision boundary in this problem is highly nonlinear, we would expect the best value for K in a K-Nearest Neighbors (K-NN) classifier to be small.

A highly nonlinear decision boundary indicates a complex, irregular separation between classes. K-NN with a small K value can better capture these intricate patterns.

Large K values tend to smooth out the decision boundary, making it more linear and less able to capture the nuances of a highly nonlinear Bayes decision boundary


