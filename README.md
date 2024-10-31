# MeXE402_Midterm_-CatapangJamilDarriusCatapang_GarciaMarkJefferson-

## Introduction

This paper highlights the basics of two such techniques known as **Linear Regression** and **Logistic Regression**. These are two of the most critical techniques in machine learning and data analysis.

- **Linear Regression**: This is a supervised learning algorithm that makes predictions on continuous output based on one or multiple input variables. It assumes a linear relationship between input features and target outputs.

- **Logistic Regression**: one class of algorithms where the outcomes will depict how likely it is that something might happen or not. Logistic regression does differ with linear regression since, instead of predicting a value, it predicts discrete values like 0 or 1, and it uses the sigmoid function to approximate an event's probability.

## Dataset Description

### Dataset 1: Iris Dataset
- **Type**: Continous (both classification and regression tasks are allowed)
- **Features**: Sepal length, Sepal width, Petal length, Petal width.
- **Target Variable**: The iris species are mainly classified into three types. Setosa, Versicolour, and Virginica. But in case of regression, we can predict the value for **Sepal Length** or **Petal Length** based on other attributes.
- **Description**: The Iris dataset may be used for classification tasks. However, it is very easily adapted to the linear regression where a continuous value like Sepal Length or Petal Length could be predicted. It's one of the most famous datasets in machine learning for its simplicity and flexibility.

### Dataset 2: Mushroom Classification Dataset
- **Type**: Binary classification.
- **Features**: Describes different physical characteristics of mushrooms such as its cap shape, cap color, gill measurement, and scent.
- **Target Variable**: To classify whether a mushroom is **poisonous** or **edible**.
- **Description**: This dataset is a detailed description of mushrooms along with physical features. It serves as a classic example for binary classification tasks and often comes up in testing models like logistic regression.

## Project Objectives

The goals of this project are:

1. Apply **Linear Regression** on **Iris dataset** to predict Sepal Length or Petal Length based on other attributes and assess the performance of models.
3. Employ the **Mushroom Classification dataset** to apply **Logistic Regression** towards predicting whether the mushroom is poisonous or edible, along with its model accuracy.
4. To understand the tacit assumptions of both models and compare usage in applications.
5. To make interactive data insights, model performance through graphs and metrics including R-squared, precision, recall, and ROC (Receiver-Operating Characteristic) curve.

## Methodology

## Linear Regression - Iris Dataset

### Step 1: Import Necessary Libraries
The analysis begins by importing essential libraries for data manipulation, visualization, and machine learning. This includes __Pandas__ for data manipulation, __Matplotlib__ and __Seaborn__ for visualization, and __Scikit-Learn__ for model building.

![image](https://github.com/user-attachments/assets/0ade75cd-7c4c-4977-af2d-d7888126efb0)

### Step 2: Load the Dataset 
Load the Iris dataset, which contains information on 150 iris flowers from three species: Setosa, Versicolor, and Virginica. Each sample includes four features: sepal length, sepal width, petal length, and petal width.

![image](https://github.com/user-attachments/assets/eac82cec-e363-47cc-b2e5-fc67d3d87fdc)

__Sample 10 rows of the dataset:__

![image](https://github.com/user-attachments/assets/abad9de1-f3a7-44f2-aeaa-0f5249780402) 

### Step 3: Labeling and Rearrangement of dataset
Labelling the dataset to easily identify the data of every columns. Also rearranging it by putting the __Dependent Variable__ in the last column.

![image](https://github.com/user-attachments/assets/440247dc-fa17-4de9-8440-d5786916ade9)

__Rearrangement Output:__

![image](https://github.com/user-attachments/assets/3f83adc7-ebb6-4de4-8cac-188fc0863d7f)


### Step 4: Data Preprocessing
__Check for missing values:__ Use .isnull().sum() to verify the data integrity.
__Data types:__ Verify data types to ensure that features are numeric and the target label is categorical.
__Encoding categorical variables (if necessary):__ In this dataset, the target label (species) may need encoding.

![image](https://github.com/user-attachments/assets/016262a4-200f-4018-a3c8-62372d71720e)

### Step 5: Feature Selection and Splitting Data
Select features __(independent variables)__ and target label __(dependent variable)__.

![image](https://github.com/user-attachments/assets/3eb5b18f-da6c-4fb9-b7a2-8945707a52e0)

#### Splitting data into training and testing sets __(80% train, 20% test)__

> __Training set (80%)__, where the model "learns" the correlations and adjusts its parameters to minimize errors. __The Testing set (20%)__ helps assess how well the model generalizes to new data, ensuring it hasn’t just memorized the training data but can make accurate predictions on unknown data.

![image](https://github.com/user-attachments/assets/74ff4297-777d-4d33-a621-4d3212fee6f3)

### Step 6: Model Selection and Training

Making fit for __Model Selection and Training__ to ensure the model accurately captures the relationships in the data while avoiding overfitting or underfitting.

> __fit__ is a method inside LinearRegression class - they are like functions.

![image](https://github.com/user-attachments/assets/12a96d80-ccea-4af4-bd05-a20ff38c34e5)

### Step 7: Model Evaluation

> #### __Make predictions on the test set__
> To assess how well the trained model generalizes to unseen data. Ensures the linear regression model performs well and generalizes to new data


#### Inference

To interpret the model’s parameters and make predictions on new data. Helps interpret how each feature impacts the target variable.

![image](https://github.com/user-attachments/assets/f183ace1-9dd1-44e0-a927-b108bb57b0e3)

![image](https://github.com/user-attachments/assets/9d651414-9de2-4ddf-8e2a-6dd2c24d0eb4)

##
#### Making the prediction of a single data point with SL = 5.1, SW = 3.5 , PW = 1.0

![image](https://github.com/user-attachments/assets/0667c52f-9716-465e-a807-41d45300f4cb)

> #### __Detailed Explanation__
> The __Petal Length__ output value, __2.63__, is predicted based on the input values for __sepal length__, __sepal width__, and __petal width__. This prediction reflects the linear relationships the model learned from the data, with each input feature contributing to the predicted value through its coefficient. The accuracy of this prediction depends on how well the model is generalized.

##
### Evaluation Metrics
 

> #### Calculated R-Squared (Accuracy)
> Measure of the proportion of variance in the target variable that the model explains. 

![image](https://github.com/user-attachments/assets/3209e0fc-fcbe-46d9-8118-c236f7baa699)

> #### Calculated Adjusted R-squared
> Number of predictors in the model. It helps to make a better choice when comparing models with different numbers of features. 

![image](https://github.com/user-attachments/assets/38e7e8ee-bee4-44de-8230-63c7d54333cf)

> #### Calculated Mean Squared Error
> Representation of the average squared errors between actual and predicted values

![image](https://github.com/user-attachments/assets/d07263ac-641a-4588-8d18-c9d5c693d482)


### Step 8: Interpretation
Shows insights on how each feature impacts the target variable and helps validate the model’s usefulness.

#### Get the coefficients of the model
In linear regression, coefficients indicate the expected change in the target variable for a one-unit change in the feature, holding other features constant. Coefficients can be interpreted as __Positive__ and __Negative__ Coefficients.

> __Positive coefficient:__ Suggests a direct relationship between the feature and target variable.

> __Negative coefficient:__ Indicates an inverse relationship.


![image](https://github.com/user-attachments/assets/b31a5731-d666-4c41-ad2e-5efb25eaa70d)

### Step 9: Visualization
Visualizing the matrix to provide insight into the model's classification performance.

#### Pairplot to visualize relationships between features

![image](https://github.com/user-attachments/assets/4da26123-a508-4dba-9b96-24eb48905f37)

#### Visual Representation

__Pairplot Visual Represatation__ of the Iris dataset, that shows pairwise relationships among features like sepal length, sepal width, petal length, and petal width across three species of Iris flowers.

![image](https://github.com/user-attachments/assets/5c2bc9be-bae2-45d5-b1b0-1549d7813f9f)

> Different colors and shapes indicate different Iris species ___(e.g., Iris-setosa, Iris-versicolor, Iris-virginica)___, making it easy to see clusters and patterns by species.

## Results 

### Summary of findings
##
__1. Linear Regression on the Iris Dataset__
- __Goal:__ Predict __Sepal Length__ (or __Petal Length__) based on other features in the dataset.
- __Data Preprocessing__:
  - Checked for missing values, confirmed no missing entries.
  - Verified that features are numeric, making them compatible with the model.

- __Model Performance__:
  - __R-squared score__: Demonstrates how well the model explains the variance in sepal/petal length.
  - __Adjusted R-squared__: Corrects R-squared by accounting for the number of predictors.
  - __Mean Squared Error (MSE)__: Indicates how closely the predictions match actual values.

### __Table 1: Linear Regression Model Evaluation (Iris Dataset)__

<div align="center">
 
| Metric              | Value     |
|---------------------|-----------|
| R-squared           | 0.96      |
| Adjusted R-squared  | 0.95      |
| Mean Squared Error  | 0.12      |

</div>

__Interpretation:__ A high R-squared value (0.96) suggests a strong linear relationship between the features and the target variable (Petal Length). A low MSE (0.12) indicates the model’s predictions are generally close to actual values.


##
__2. Logistic Regression on the Mushroom Dataset__
- __Goal:__ Classify mushrooms as __edible__ or __poisonous__ based on physical characteristics.
  - __Data Preprocessing__:
  - Checked for missing values and encoded categorical features.
 
- __Model Performance__:
  - __
  - 
 

### __Table 2: Logistic Regression Model Evaluation (Mushroom Dataset)__

<div align="center">

| Metric              | Value     |
|---------------------|-----------|
| Accuracy            | 0.95     |


</div>

__Interpretation:__ High accuracy (0.95) indicates the model is reliable in predicting poisonous mushrooms. 

## ___Comparative Insights and Interpretations___

__1. Linear Regression on the Iris Dataset:__

The linear regression model was applied to predict Petal Length based on various features like Sepal Width, Sepal Length, and Petal Width. The model achieved an R-squared value of 0.85, indicating that approximately 85% of the variance in Petal Length can be explained by the input features. This strong correlation suggests that the selected features are effective predictors.

Among the features, Sepal Length and Petal Width emerged as the most significant predictors. Their positive coefficients indicate a direct relationship: as either feature increases, so does the Petal Length. Conversely, Sepal Width had a negative coefficient, suggesting a lesser influence on the target variable.

The __Adjusted R-squared__ value of 0.95 confirms the model's robustness when considering the number of predictors. This metric is particularly useful for evaluating models with multiple independent variables, as it penalizes excessive use of non-informative predictors. The low Mean Squared Error (MSE) of 0.12 further signifies the model’s accuracy in making predictions, as it reflects the average squared differences between predicted and actual values.

__2. Logistic Regression on the Iris Dataset:__

The Logistic Regression on the Mushroom dataset performed well, as evidenced by high accuracy, showing that the model effectively distinguishes between __edible__ and __poisonous__ mushrooms.
