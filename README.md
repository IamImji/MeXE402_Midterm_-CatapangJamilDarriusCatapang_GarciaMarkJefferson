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

Sample 10 rows of the dataset:

![image](https://github.com/user-attachments/assets/abad9de1-f3a7-44f2-aeaa-0f5249780402) 

### Step 3: Labeling and Rearrangement of dataset
Labelling the dataset to easily identify the data of every columns. Also rearranging it by putting the __Dependent Variable__ in the last column.

![image](https://github.com/user-attachments/assets/440247dc-fa17-4de9-8440-d5786916ade9)

Rearrangement Output

![image](https://github.com/user-attachments/assets/3f83adc7-ebb6-4de4-8cac-188fc0863d7f)


### Step 4: Data Preprocessing
__Check for missing values:__ Use .isnull().sum() to verify the data integrity.
__Data types:__ Verify data types to ensure that features are numeric and the target label is categorical.
__Encoding categorical variables (if necessary):__ In this dataset, the target label (species) may need encoding.

![image](https://github.com/user-attachments/assets/016262a4-200f-4018-a3c8-62372d71720e)

### Step 5: Feature Selection and Splitting Data
Select features __(independent variables)__ and target label __(dependent variable)__.

![image](https://github.com/user-attachments/assets/3eb5b18f-da6c-4fb9-b7a2-8945707a52e0)

Splitting data into training and testing sets __(80% train, 20% test)__

![image](https://github.com/user-attachments/assets/74ff4297-777d-4d33-a621-4d3212fee6f3)

### Step 6: Model Selection and Training

![image](https://github.com/user-attachments/assets/12a96d80-ccea-4af4-bd05-a20ff38c34e5)

### Step 7: Model Evaluation

![image](https://github.com/user-attachments/assets/ab1fc39c-ed52-47c4-aaa6-6bc258da25b7)

![image](https://github.com/user-attachments/assets/33b83b50-9e40-4938-8bfd-207d15f80160)

![image](https://github.com/user-attachments/assets/eaff7a9e-399d-4ad1-a9c7-092d197aed51)

![image](https://github.com/user-attachments/assets/c91a7bbe-9475-4583-a35e-8d804a4c8ac4)

### Step 8: Interpretation
#### Get the coefficients of the model

![image](https://github.com/user-attachments/assets/b31a5731-d666-4c41-ad2e-5efb25eaa70d)

### Step 9: Visualization
Visualizing the matrix to provide insight into the model's classification performance.

#### Pairplot to visualize relationships between features

![image](https://github.com/user-attachments/assets/4da26123-a508-4dba-9b96-24eb48905f37)

#### Visual Representation

![image](https://github.com/user-attachments/assets/5c2bc9be-bae2-45d5-b1b0-1549d7813f9f)




