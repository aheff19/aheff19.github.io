---
layout: post
title:      "Types of News Stories that get Shared "
date:       2020-08-25 01:20:33 +0000
permalink:  types_of_news_stories_that_get_shared
---


The content of your blog post goes here.
Social media is part of everyday life. Daily we are inundated with news stories of all different types. This project I did for the end of Module 3 goes on to explore which topics are the most popular. 

 NewsPopularityPredictorLogisticRegression:
Logistic regression to predict which news topic will trend on social media given factors

The purpose of this project is to predict which variables will determine a news article to be popular and get shared on social media. 
EDA:



![Imgur](https://imgur.com/gYltnpM.png)

The maximum number of shared articles were in the range 1000 to 3000.

There are a lot of outliers in this dataset and were removed using IQR and the Z-Score method. 


Models used for this dataset and outcomes:

![Imgur](https://imgur.com/ZvztTPC.png)

Random Forest showed the highest accuracy with XGBoost being a close second. 

Confusion Matrix of Random Forest:

![Imgur](https://imgur.com/Eefiy9u.png)

 
True positives: 3877 
True Negative: 4040
False Positive: 2028
False Negative: 1949 
Precision=TP/ (TP+FP) =3877/ (3877+2028) =0.6566 
Recall=TP/ (TP+FN) =3877/ (3877+1949) =0.6654

 
 
 
 
 
Outcomes:
Lifestyle data channel got the maximum number of shares. While social media got the least number of shares.

![Imgur](https://imgur.com/XjGPVcG.png)

![Imgur](https://imgur.com/99ajmFf.png)

Saturday was the most popular day to share:

![Imgur](https://imgur.com/ys1e90F.png)



 
Recommendations:
 
Publish new articles during the weekend so that they become more popular


Articles are getting more number of shares when the data channel is either lifestyle or social media


Short and to the point: the articles with the most number of shares should have titles that are around 6 to 14 words.
Future Work:
Delve more into subtopics
For example: different topics under “lifestyle”



Reasons why some topics are not as popular
This would be fun to partner with a psychology expert
 



