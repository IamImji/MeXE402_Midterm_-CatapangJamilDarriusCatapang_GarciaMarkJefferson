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
5. To make interactive data insights, model performance through graphs and metrics including R-squared, Accuracy.
## Methodology

## Linear Regression - Iris Dataset

### Import Necessary Libraries
The analysis begins by importing essential libraries for data manipulation, visualization, and machine learning. This includes __Pandas__ for data manipulation, __Matplotlib__ and __Seaborn__ for visualization, and __Scikit-Learn__ for model building.

![image](https://github.com/user-attachments/assets/0ade75cd-7c4c-4977-af2d-d7888126efb0)

### Load the Dataset 
Load the Iris dataset, which contains information on 150 iris flowers from three species: Setosa, Versicolor, and Virginica. Each sample includes four features: sepal length, sepal width, petal length, and petal width.

![image](https://github.com/user-attachments/assets/eac82cec-e363-47cc-b2e5-fc67d3d87fdc)

__Sample 10 rows of the dataset:__

![image](https://github.com/user-attachments/assets/abad9de1-f3a7-44f2-aeaa-0f5249780402) 

### Labeling and Rearrangement of dataset
Labelling the dataset to easily identify the data of every columns. Also rearranging it by putting the __Dependent Variable__ in the last column.

![image](https://github.com/user-attachments/assets/440247dc-fa17-4de9-8440-d5786916ade9)

__Rearrangement Output:__

![image](https://github.com/user-attachments/assets/3f83adc7-ebb6-4de4-8cac-188fc0863d7f)


### Data Preprocessing
__Check for missing values:__ Use .isnull().sum() to verify the data integrity.

__Encoding categorical variables (if necessary):__ In this dataset, the target label (species) may need encoding.

![image](https://github.com/user-attachments/assets/016262a4-200f-4018-a3c8-62372d71720e)

### Feature Selection and Splitting Data
Select features __(independent variables)__ and target label __(dependent variable)__.

![image](https://github.com/user-attachments/assets/3eb5b18f-da6c-4fb9-b7a2-8945707a52e0)

#### Splitting data into training and testing sets __(80% train, 20% test)__

> __Training set (80%)__, where the model "learns" the correlations and adjusts its parameters to minimize errors. __The Testing set (20%)__ helps assess how well the model generalizes to new data, ensuring it hasn’t just memorized the training data but can make accurate predictions on unknown data.

![image](https://github.com/user-attachments/assets/74ff4297-777d-4d33-a621-4d3212fee6f3)

### Model Selection and Training

Making fit for __Model Selection and Training__ to ensure the model accurately captures the relationships in the data while avoiding overfitting or underfitting.

> __fit__ is a method inside LinearRegression class - they are like functions.

![image](https://github.com/user-attachments/assets/12a96d80-ccea-4af4-bd05-a20ff38c34e5)

### Model Evaluation

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


### Interpretation
Shows insights on how each feature impacts the target variable and helps validate the model’s usefulness.

#### Get the coefficients of the model
In linear regression, coefficients indicate the expected change in the target variable for a one-unit change in the feature, holding other features constant. Coefficients can be interpreted as __Positive__ and __Negative__ Coefficients.

> __Positive coefficient:__ Suggests a direct relationship between the feature and target variable.

> __Negative coefficient:__ Indicates an inverse relationship.


![image](https://github.com/user-attachments/assets/b31a5731-d666-4c41-ad2e-5efb25eaa70d)

### Visualization
Visualizing the matrix to provide insight into the model's classification performance.

##
#### Visual Representation

__Scatter Plot of Petal Length as Dependent Variable__ 

![image](https://github.com/user-attachments/assets/24b8a3c9-a176-4c57-9952-ccae83d3540b)

> The __Scatter Plot__ effectively shows the relationship between two continuous variables, __petal length__ (the dependent variable) and each feature (__sepal length, sepal width, and petal width__). This plot shows how the dependent variable changes in response to each independent variable, which helps assess patterns in the data. The plot allow us to see if the data approximately forms a straight line, confirming whether linear regression is a good fit. By overlaying a regression line on a scatter plot, we can visually assess the model's fit to the data, which helps to interpret how well each independent variable explains changes in the dependent variable.

## Logistic Regression - Mushrooms

### Importing Libraries and Dataset
The analysis began by importing the necessary libraries, with pandas being the primary library used for data manipulation. We loaded the dataset into a DataFrame using the pd.read_csv() function, which allows us to read data from a CSV file easily. This step is essential as it provides the foundation for further analysis.


![image](https://github.com/user-attachments/assets/8089acfe-6be2-4783-8cb7-45f7a0cfce6c)


### Overview of the Dataset
To understand the structure of the dataset, we used the dataset.info() method. This command provides a summary of the dataset, including the number of entries (rows), the types of data in each column, and any potential issues. This overview is vital for identifying what kind of preprocessing steps might be necessary.


![image](https://github.com/user-attachments/assets/81901a00-b126-4563-89d7-a829434526be)


### Label Encoding
Next, we needed to convert categorical variables into numerical values, as most machine learning algorithms work only with numbers. We employed LabelEncoder to transform these categorical variables into a numerical format. For example, if we had a column representing colors (like 'red', 'blue', 'green'), each color would be assigned a unique integer (0, 1, 2, etc.). This encoding is essential for enabling the model to interpret the data correctly.


![image](https://github.com/user-attachments/assets/55840ead-564d-4651-a7f4-6bc9ee35daff)

![image](https://github.com/user-attachments/assets/5fb07167-ee66-480b-b135-f920760b19a9)



###  Handling Missing Values
To ensure the integrity of our dataset, we checked for any missing values using dataset.isna().sum(). This method shows the total number of missing values for each column. If any missing values were present, we would need to decide how to handle them (e.g., by filling them in with the mean or median of the column, or removing the affected rows). In our case, we confirmed there were no missing values, which simplified our preprocessing steps.


![image](https://github.com/user-attachments/assets/9eb2a521-5313-4493-849b-32076aef8857)


### Separating Features and Target
After ensuring the data was clean, we separated the independent variables (features) from the dependent variable (target). The features, stored in X, consisted of all columns except the last one, while the target variable, stored in y, contained only the last column. This separation is crucial as it allows the model to learn from the features in order to predict the target.


![image](https://github.com/user-attachments/assets/5fcf6d98-6d30-4b52-b5af-cb492d648410)


### Train-Test Split
To evaluate the performance of our model accurately, we divided the dataset into two parts: training and testing. We used train_test_split to create these sets, with an 80-20 split, meaning 80% of the data was used for training the model, and 20% was reserved for testing it. This separation is important because it allows us to train the model on one set of data and then evaluate its performance on a different, unseen set.


![image](https://github.com/user-attachments/assets/ef7805d4-7d0c-4cb2-b451-bc4be7839b0c)



### Feature Scaling
To ensure that all features contribute equally to the model's predictions, we standardized the features using StandardScaler. This process adjusts the features so they have a mean of 0 and a standard deviation of 1. Feature scaling is particularly important for algorithms like logistic regression, as it can improve the model’s performance and convergence speed.


![image](https://github.com/user-attachments/assets/4a9d51c2-fcb2-4c8c-b481-a74e62fcff45)

##
### Building and Training the Model
After preprocessing the data, we moved on to building and training the model.

#### Logistic Regression
We chose logistic regression as our classification algorithm because it is a widely used method for binary classification problems. We initialized the logistic regression model and trained it using the training dataset. During this training process, the model learned the relationships between the features and the target variable, allowing it to make predictions based on the input data.


![image](https://github.com/user-attachments/assets/4a6aaf21-255e-4a87-b5a6-f3d4a0b83f58)



###  Making Predictions
Once the model was trained, we used it to make predictions on the test set. This step is crucial for assessing how well our model generalizes to new data. We also demonstrated how to predict the outcome for a single data point to illustrate the model's practical application.


![image](https://github.com/user-attachments/assets/6c119c8b-1d0d-4e0b-81b2-1551ef03735d)

__List of Variables use in prediction__

![image](https://github.com/user-attachments/assets/72b1636d-9bb1-43f9-8c78-80560513c539)


##
### Evaluating the Model
The final step involved evaluating the model's performance to determine its effectiveness.

### Confusion Matrix
To evaluate the predictions, we calculated and displayed a confusion matrix. This matrix provides a visual representation of the model's performance, showing the number of true positives, true negatives, false positives, and false negatives. Analyzing this matrix helps us understand how well the model is performing and where it may be making errors.


![image](https://github.com/user-attachments/assets/1df0b736-44db-4503-8323-6d2abb60d894)



### Accuracy Calculation
We computed the accuracy of the model, both manually and using the accuracy_score() function. Accuracy is a simple yet powerful metric that indicates the proportion of correct predictions made by the model. This step is crucial in determining how reliable the model is for making predictions.


![image](https://github.com/user-attachments/assets/39f93ca0-3845-43e8-9dc2-efa923eb9826)



### Visualizing the Confusion Matrix
To make the performance of the model even clearer, we visualized the confusion matrix using a heatmap. This graphical representation allows us to quickly identify areas where the model is performing well and where it might be struggling, making it easier to communicate results to others.


![image](https://github.com/user-attachments/assets/70eff950-4872-47f4-b117-7f9249eed7fc)

__Confusion Matrix Edible and Poisonous Mushroom__

![image](https://github.com/user-attachments/assets/34b5d1fb-16a1-4cdd-9a2f-22152d724587)

> Confusion Matrix shows the exact number of correctly classified instances for each class, 820 for __class 0__ (__Edible__) and 735 __class 1__ (__Poisonous__) This helps understand how well the model distinguishes between __edible__ and __poisonous__ mushrooms. It highlights the number of misclassifications, 32 for __Class 0__ misclassified as __Class 1__ and 38 for __Class 1__ misclassified as __Class 0__. This allows us to assess where the model might need improvement, which is crucial in datasets like mushrooms, where misclassifying a poisonous mushroom as edible can have serious consequences.




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
##
### __Table 1: Linear Regression Model Evaluation (Iris Dataset)__

<div align="center">
 
| __Metric__          | __Value__ |
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
  - Accuracy : The metric reflects the proportion of correctly classified mushrooms (both __edible__ and __poisonous__) out of the total. A high accuracy, 0.96, would suggest that the model is reliable in overall classification performance.

 
##
### __Table 2: Logistic Regression Model Evaluation (Mushroom Dataset)__

<div align="center">

| Metric              | Value     |
|---------------------|-----------|
| Accuracy            | 0.96      |
| Accuracy Score      | 0.96      |



</div>

__Interpretation:__ High accuracy (0.95) indicates the model is reliable in predicting poisonous mushrooms. 

##
 ___Comparative Insights and Interpretations___

__1. Linear Regression on the Iris Dataset:__

The linear regression model was applied to predict Petal Length based on various features like Sepal Width, Sepal Length, and Petal Width. The model achieved an R-squared value of 0.96, indicating that approximately 96% of the variance in Petal Length can be explained by the input features. This strong correlation suggests that the selected features are effective predictors.

Among the features, Sepal Length and Petal Width emerged as the most significant predictors. Their positive coefficients indicate a direct relationship: as either feature increases, so does the Petal Length. Conversely, Sepal Width had a negative coefficient, suggesting a lesser influence on the target variable.

The __Adjusted R-squared__ value of 0.95 confirms the model's robustness when considering the number of predictors. This metric is particularly useful for evaluating models with multiple independent variables, as it penalizes excessive use of non-informative predictors. The low Mean Squared Error (MSE) of 0.12 further signifies the model’s accuracy in making predictions, as it reflects the average squared differences between predicted and actual values.

__2. Logistic Regression on the Mushroom Classification Dataset:__

The Logistic Regression on the Mushroom dataset performed well, as evidenced by high accuracy, showing that the model effectively distinguishes between __edible__ and __poisonous__ mushrooms.
The logistic regression model was employed to classify mushrooms as either edible or poisonous based on various features, including cap shape, bruises, odor, and habitat. The model achieved an accuracy score of 95.69%, indicating that it correctly identified nearly 96% of the mushrooms in the test set. This high accuracy reflects the effectiveness of the selected features in predicting mushroom edibility.

Among the features, odor and gill color emerged as significant predictors. Specific odors and cap colors showed strong correlations with a poisonous classification, highlighting their importance in the model's decision-making process.

Accuracy score was consistent with the overall accuracy, indicating the model's stability in handling 23 categorical features. The low error rates further reinforce the model's reliability, as it effectively utilizes the data to provide trustworthy classifications.
