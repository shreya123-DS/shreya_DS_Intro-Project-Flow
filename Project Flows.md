# PROJECT FLOWS
## 1. PROJECT: Generative AI Based Content Creation
  Problem Statement:The manual creation of product descriptions for retail websites is a time-consuming and labor-intensive process. As product catalogs grow, it becomes increasingly difficult to maintain consistency and efficiency in generating high-quality descriptions.
Solution:
We developed and fine-tuned a Generative AI model (GPT) to automate the generation of personalized product descriptions. This AI-powered solution eliminates the need for manual content creation, enabling faster and more consistent product descriptions.
Objective:The objective of this project is to reduce the manual effort involved in product catalog creation, improving efficiency by 50% through automation. The model will generate domain-specific content for retail websites, saving time and ensuring accuracy.
Project Flow:
Data Collection & Preprocessing: Gather and clean product description data to train the model effectively.
Model Selection & Fine-Tuning: Fine-tune a pre-trained GPT model with domain-specific data to enhance its understanding of retail terminology.
Model Training & Evaluation: Train the model, then evaluate it using BLEU scores to ensure the quality and relevance of the generated content.
Automation: Integrate the model into the catalog management system to automate the generation of product descriptions.
Vocabulary Integration: Add industry-specific vocabulary to improve the contextual accuracy of the descriptions.
Deployment & Scaling: Deploy the model for real-time use and scale it for handling larger catalogs and additional product types.


## 2.PROJECT:Customer Churn Prediction Model
Dataset size: [240000,30] 

0-churn,1-non churn--------------------------

Churn: where customer starts stop using the services 

Description: Developed a machine learning model to predict customer churn for a retail company. The objective was to identify customers at risk of leaving the service and enable the company to implement proactive strategies or steps, such as personalized promotions or offers, to retain them and improve customer loyalty. 

Problem statement: 
           
                In a retail company the customers are frequently churning, that could be because of multiple reasons like Price and value perception, Poor customer service, Product quality issues, Inconvenient shipping experience, competitors offerings and promotions, the stores are too far from the locations and communication gaps etc. We wanted to build a customer churn model to predict if a customer is going to churn in the next quarter or not. Why ? If we identify the customers who are likely to churn, we can target them with the right strategies and the retailer will be able to give them the right offers to retain the customers. This will help in reduction of operation cost because acquiring a new customer is costlier than retaining the existing customer. So, this is how we tried to reduce the operation cost. 

                 →I had a discussion with my client on the client requirements. Once I had a discussion with the client, I started with collecting the data that is required. I went to the Oracle database. I fetch the data by using python and a package called cx_oracle. Once I fetched the information, I started creating my master dataset. But the master dataset was not in a cleaned process. So I started cleaning the dataset by using different preprocessing pipeline 

At first, I collected the last one-year data from my client (Barnes & Noble) then I imported all data into the Oracle database with the help of CX-Oracle(package).


The initial dataset had 240 columns, 3 million rows, and around 10 GB in size. So we started actually doing memory optimization.

PREPROCESSING:  
During the pre-processing stage, several steps are undertaken.

1. Memory Optimization
 2. Null value treatment
 3. Outlier detection – treatment
 4. Label encoding 
5. Feature Scaling (min max, standard scaling) 
6. Normalization/standardization 

Then I split all data into train-test-split .After this I use a SMOT technique – this is for balancing the imbalancing data.
Here we can also do EDA for finding the relation b/n columns (scatter plot, box plot, histogram).

MODEL BUILDING: 

Here I use Decision tree/ Random forest as a base model. For base model I get 70% accuracy.

MODEL VALIDATION: 
Precision: is the ratio of true positive predictions to the total predicted positives (true positives + false positives).

Recall: is the ratio of true positive predictions to the total actual positives (true positives + false negatives). 

Accuracy

 F1 score 

Hyperparametric tuning:
Random search cv/Grid search cv (75%) 

Tuning involves adjusting these hyperparameters to find the best combination for achieving the highest accuracy, precision, recall, F1-score, or other evaluation metrics. 

Parameters: N-estimators, min depth, max depth, criteria (entropy, Gini index, information gain) 

Overfitting: smote, regularization, dropout, early stopping, cross validation 

Underfitting: take more data, remove regularization, feature engineering, increase training time. Finally save all data into a pickle file

Deployment: 

Flask API

Fast API 

Django

Top 10 Features: 
1.Customer id 

Customer tenure

 Occupation type

 2.total spend

 3.churn

 4. last purchase date Payment history

 5.Gender

 6.AGE 

7.purchase categories

 8.No of Purchases

 9. store location Product usage Promotions discounts 

10.ratings 

11.Annual income

 12.No.of returns(customer experience)
