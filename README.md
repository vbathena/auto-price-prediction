# Price Prediction of Used Cars Project
> This repository contains the Used Cars dataset, which provides information about vehicle information, pricing and mileage, location information and title status attributes. The objective of this analysis is to identify the key drivers of used car prices and develop predictive models to assist used car dealers in optimizing their inventory and pricing strategies.

## General Information
- Dataset analysis work completed in Jupyter Notebook. Link here ([auto-price-prediction.ipynb](https://github.com/vbathena/auto-price-prediction/blob/main/auto-price-prediction.ipynb))
- Dataset in *data* folder
- Images in *images* folder

## Summary of Findings
Based on the data provided, the following key findings have been summarized:

1. Dataset Overview:
   
   - It's a subset of 426K cars information available from original kaggle dataset [data/vehicles.csv](https://github.com/vbathena/auto-price-prediction/blob/main/data/vehicles.csv)
   - The data set contains 14 categorical and 4 numerical features.
   - There are 0 duplicate entries that should be addressed.

2. Missing Values:

   - Multiple columns have ranging from 0 to over 300,000 missing values. So these columns can't be dropped.
   - The 'size' feature is missing a significant portion of its values (71.77%).
   - The 'year' and 'odometer' features have a small number of missing values.
   - Several features have missing values:
     'year', 'manufacturer', 'model', 'condition', 'cylinders', 'fuel', 'odometer', 'title_status', 'transmission', 'VIN', 'drive', 'size', 'type', 'paint_color'.

3. Unique Values:

   - The "state" and "manufacturer" feature contains too many unique values, which may require further analysis or handling.
   
4. Correlation:

   - The correlation between the price of a car and the year it was produced is positive. This means that older cars tend to be less expensive than newer cars.
   - The correlation between the price of a car and the mileage of a car is also negative. This means that cars with lower mileage tend to be more expensive than cars with higher mileage.

5. Price Analysis:

   - The average price of a used car in the dataset is $17,000.
   - The most expensive state for used cars is Delaware, and the least expensive state is Virginia.
   - The most expensive manufacturer is Mercedes-Benz, and the least expensive manufacturer is Mercury.
   - The most expensive type of vehicle is a pickup truck, and the least expensive type of vehicle is a minivan.
   - Cars in good condition tend to be more expensive than cars in fair condition.
   - Cars with lower odometer readings tend to be more expensive than cars with higher odometer readings.


6. Model Methodology:

   - I have conducted an in-depth analysis of a dataset containing various features related to used cars and their prices. 
   - The analysis involved exploring feature importance, model selection, performance evaluation, and interpreting model coefficients.
   
7. Model Evaluation Findings:

   - Feature Importance:
        > Features such as year, odometer, and drive were identified as crucial drivers of used car prices. These features had the most significant impact on price prediction based on variable inflation factor and permutation importance.

   - Model Selection:
        > After rigorous testing, the Ridge model with a polynomial degree of 3 and an alpha value of 10 emerged as the preferred model. This model provided a balanced trade-off between prediction accuracy and model complexity.

   - Insights from Coefficients:
        > The Ridge model's coefficients shed light on the relationships between features and prices. For instance, higher year values and certain drive types were associated with increased prices. Conversely, higher odometer readings had a negative impact on prices.

   - Recommendations:
        > Refinement of Feature Selection: Further refinement of feature selection is recommended using techniques like recursive feature elimination to optimize model performance.
        > Feature Engineering: Consider generating additional features or transforming existing ones to capture non-linear relationships and enhance model performance.
        > Validation and Testing: Perform thorough cross-validation to ensure the model's reliability in generalizing to new data.
        > Interpretation: Focus on interpreting the coefficients in terms of real-world implications for used car dealers.

8. Model Performance:

    - Ridge Model (Degree 3, Alpha 10) with Top 5 Features:
        Train MSE: 100,610,406.81
        Test MSE: 103,677,988.43
        Train MAE: 6,006.52
        Test MAE: 6,023.53
        Score: 0.55

    - LASSO Model with Top 5 Features:
        Train MSE: 122,637,942.29
        Test MSE: 125,754,086.79
        Train MAE: 6,865.58
        Test MAE: 6,886.02
        Score: 0.46

    - Linear Regression Models with Top 5 Features:
        > Linear Regression Model:
            Train MSE: 96,550,126.10
            Test MSE: 100,094,895.75
            Train MAE: 5,800.98
            Test MAE: 5,820.69
            Score: 0.57
        > Linear Regression with LASSO:
            Train MSE: 137,777,789.78
            Test MSE: 107,613,731.20
            Train MAE: 6,036.44
            Test MAE: 6,038.13
            Score: 0.53
        > Linear Regression with SFS LASSO:
            Train MSE: 137,777,789.78
            Test MSE: 107,613,731.20
            Train MAE: 6,036.44
            Test MAE: 6,038.13
            Score: 0.52

9. Additional Thoughts:
   
   - Some specific questions that we could ask our clients to help improve the model:

        What other factors are important for predicting used car prices?
        Can you provide more data on the following features: year, cylinders, odometer, fuel, and drive?
        Are there any other regularization techniques that you would like to try?


## Technologies Used
- Seaborn
- Pandas
- Numpy
- Matplotlib
- Scipy Stats
- Scikit-learn

## Future Work
Future work could focus on expanding the dataset to improve the accuracy of their pricing:
    Gather more data on the factors that affect used car prices.
    Use more sophisticated machine learning models to analyze the data.
    Regularly update their pricing models to reflect changes in the market.

## Conclusion
Overall, the findings suggest that the Ridge model with a polynomial degree of 3 and an alpha value of 10 is the most suitable model for predicting used car prices. This model effectively balances prediction accuracy and model complexity. Key features like year, odometer, and drive play a crucial role in determining prices. Further model refinement, feature engineering, and thorough validation will contribute to enhancing the model's reliability and practical applicability for used car dealers.


## Contact
Created by [@vbathena](https://www.linkedin.com/in/vijayabhaskarreddybathena/) - feel free to contact me!
