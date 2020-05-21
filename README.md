# A Hotel Booking Recommender System 

Revenue Management with Hotel Booking Cancellation Predictions using a Machine Learning Classification Model 

Chloe Ling (MSc.), Phillip Cohen (MD/phD.) 

## Overview 

Managing revenue in hospitality is important for hotels to maximize profit. A challenge in hospitality is maximizing hotel 
occupancy as hotel bookings are performed in advance and customers may cancel a booking. Cancellations thus represent a 
revenue loss, that has previously been difficult to predict and therefore remedy. It is clear that booking cancellations 
negatively contribute to hotel revenue and accurate forecasting. We define revenue management as “the application of information
systems and pricing strategies to allocate the right room for the right guest and the right price at the right time via the right 
distribution channel” (Mehrotra and Ruttley, 2006). 

Using data on features of a hotel booking, this study investigates the potential machine learning approaches to predicting a cancellation of a hotel booking with the goal of maximizing hotel profit. 
Implementing several modeling methods includingrandom forest, k-nearest neighbors, logistic regression and xgboost, we present a model 
to predict cancellations with precision exceed 80%.

## Dataset 

This dataset is originally from the article Hotel Booking Demand Datasets, written by Nuno Antonio, Ana Almeida, 
and Luis Nunes for Data in Brief, Volume 22, February 2019. The data was acquired from hotels’ Property Management 
System (PMS) SQL databases. The data contains 32 different features each with a total of 119,390 values. 


## Data Preprocessing 

All categorical features were transformed into quantitative features by one-hot encoding method, where dummy variables are created for 
each potential value of a categorical feature. Features were then z-scaled before modeling using python 3 sci-kit learn StandardScaler 
function.

<img width="572" alt="Screen Shot 2020-05-21 at 11 32 01 AM" src="https://user-images.githubusercontent.com/31297724/82575819-f352bd00-9b56-11ea-8d39-1a1c64133fe8.png">


## Model Architecture 

Models that seem appropriate for the specific problem and will be evaluated are:

• Logistic Regression 
• Support Vector Machine 
• K-nearest neighbor 
• Random Forest 
• XG Boost 
• Ensemble (majority voting) 

** These models were trained on a sample of global, city hotel, and resort training datasets and tested on the respective test datasets. 


## Exploratory Data Analysis 

Distribution of cancellations by hotel type 

<img width="586" alt="Screen Shot 2020-05-21 at 11 36 57 AM" src="https://user-images.githubusercontent.com/31297724/82576143-71af5f00-9b57-11ea-9b4d-d044bdb18383.png">

## Hyperparameter Tuning 

As described above five models were generated. Hyperparameters for each model were determined using methods for each model listed.

<img width="653" alt="Screen Shot 2020-05-21 at 11 37 41 AM" src="https://user-images.githubusercontent.com/31297724/82576213-8d1a6a00-9b57-11ea-8785-1ad53464385d.png"> 



## Feature Importance by Model 

Feature importance was measured using the permutation importance method. Notably deposit type and lead time were among the top three most important features in four of five models, and thus these features are very relevant and critical to predicting hotel cancellation. Interestingly the most important features for kNN
are generally different from the other methods. This is likely because of the different nature of kNN as a lazy learning method than the other models.

<img width="886" alt="Screen Shot 2020-05-21 at 11 41 44 AM" src="https://user-images.githubusercontent.com/31297724/82576823-26e21700-9b58-11ea-9b01-1010f29c972a.png">

<img width="915" alt="Screen Shot 2020-05-21 at 11 41 51 AM" src="https://user-images.githubusercontent.com/31297724/82576839-2f3a5200-9b58-11ea-8a4e-44764ec53b33.png">

## Model Performance and Evaluation 

Accuracy Metrics for Global, City, and Resort Models

<img width="1136" alt="Screen Shot 2020-05-21 at 11 43 19 AM" src="https://user-images.githubusercontent.com/31297724/82577010-614bb400-9b58-11ea-8445-2ec4d460ca29.png">

<img width="1129" alt="Screen Shot 2020-05-21 at 11 43 27 AM" src="https://user-images.githubusercontent.com/31297724/82577024-66a8fe80-9b58-11ea-9bfe-197c131fd12f.png">

<img width="1157" alt="Screen Shot 2020-05-21 at 11 43 38 AM" src="https://user-images.githubusercontent.com/31297724/82577040-6b6db280-9b58-11ea-81d8-3ba70a65d8c3.png">



