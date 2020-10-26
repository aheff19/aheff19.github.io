---
layout: post
title:      "Predicting Cardiovascular Disease"
date:       2020-10-26 07:31:05 +0000
permalink:  predicting_cardiovascular_disease
---


##Cardiovascular-Disease

Testing several models to see which accurately predicts factors that cause cardiovascular disease.
For my capstone project I analyzed a data set on cardiovascular disease, or heart disease. Heart disease is preventable yet affects people around the world. In the United States,  according to the Centers for Disease Control:

Heart disease is the leading cause of death for men, women, and people of most racial and ethnic groups in the United States.1
One person dies every 36 seconds in the United States from cardiovascular disease.
About 655,000 Americans die from heart disease each year—that’s 1 in every 4 deaths.
Heart disease costs the United States about $219 billion each year from 2014 to 2015.3 This includes the cost of healthcare services, medicines, and lost productivity due to death. (https://www.cdc.gov/heartdisease/facts.htm)

This project examines which variables are most likely to cause it. The dataset used here is from Kaggle and contains 70,000 instances and 12 features: (https://www.kaggle.com/sulianova/cardiovascular-disease-dataset)

* Age | Objective Feature | age | int (days)
* Height | Objective Feature | height | int (cm) |
* Weight | Objective Feature | weight | float (kg) |
* Gender | Objective Feature | gender | categorical code |
* Systolic blood pressure | Examination Feature | ap_hi | int |
* Diastolic blood pressure | Examination Feature | ap_lo | int |
* Cholesterol | Examination Feature | cholesterol | 1: normal, 2: above normal, 3: well above normal |
* Glucose | Examination Feature | gluc | 1: normal, 2: above normal, 3: well above normal
* Smoking | Subjective Feature | smoke | binary |
* Alcohol intake | Subjective Feature | alco | binary |
* Physical activity | Subjective Feature | active | binary |
* Presence or absence of cardiovascular disease | Target Variable | cardio | binary |

## Cleaning and Preprocessing

After importing the necessary libraries and the data set, the next step is to clean and prepare it. This involves inspecting the datas, looking for and removing duplicates, outliers, and null values, in addition to feature engineering. 

Weight has a lot of outliers



Visual Exploratory Data Analysis (EDA):


The distribution of age ranges from mid-30’s to the mid-60’s

![Imgur](https://imgur.com/0YM2rpr.png) 

The weight ranges from 120 pounds to about 250 pounds. 

![Imgur](https://imgur.com/7FgvVyw.png)

The highest correlation with cardiovascular disease is shown with systolic blood pressure (the upper number).

![Imgur](https://imgur.com/U64lxwxl.png)

Modeling:

## The following were used:
 * Logistic Regression
 * KNeighbors
 * Naive Bayes
 * Decision Tree
 * SVM (linear)
 * Random Forest
 * Xtra Trees Classifier
 * Ada Boost
 * The best performing models with AUC-ROC scores at .72 - .73 were: 
 * Logistic Regression
 * Decision Trees
 * SVM
 * Random Forest
 
## The worst performing models were:
 * Naive Bayes (AUC-ROC at .71)
 * Ada Boost (AUC-ROC at .63)

Below is the confusion matrix for Random Forest. The highest percentages show true negatives and true positives.

![Imgur](https://imgur.com/l67T2mq.png)

Neural Networks
This is one of the items I would like to do for future work. Perhaps the model is underfitting or it is the data. When I viewed the loss train (history.history), From viewing this, the numbers are similar, in each category or loss and accuracy. This explains the graph and also may indicate that more than just a few epochs need to be run.  

![Imgur](https://imgur.com/pX7pnXF.png)

