# Neural_Network_Charity_Analysis

## Overview

### Purpose

The purpose of this analysis is to help AlphabetSoup determine the success of charities.
We will be using deep learning models to determine if ALphabetSoup should invest in particular charity or not based on historical data.


## Results :

### Data Preprocessing :

Are target and feature varaible are as follows:

* Target Variable - "IS_SUCCESSFUL"
* Feature Variable -  "APPLICATION_TYPE", "AFFILIATION", "CLASSIFICATION", "USE_CASE", "ORGANIZATION", "INCOME_AMT", "SPECIAL_CONSIDERATIONS", "ASK_AMT","STATUS"
* Dropped Columns - Initially only "EIN" and "NAME" columns were dropped, but in order improve the accuracy of the model STATUS columns was also dropped as a part of optimizing the model

### Compiling Training and Evaluating the model :

The initial neural network was created with 1 input layer, 2 hidden layers and an output layer.
The hidden layers used relu activation feature while the output layer used a sigmoid activation function.
Sigmoid and Relu activation fucntion were used as they mostly deal with positive values


![image](https://user-images.githubusercontent.com/99941484/179379556-be82726a-72fe-4dac-bba5-a499750c3402.png)


We achived an initial accuracy of 72.81%.

![image](https://user-images.githubusercontent.com/99941484/179379985-87ba6204-2c1b-40a1-a9a5-8e5eff1f76fe.png)

Accuracy Graph :

![image](https://user-images.githubusercontent.com/99941484/179380018-6b48dc5d-3ca7-4608-bf86-b8b0dbad0263.png)


But the objective is to achieve an accuracy of 75 percent or higher. So below changes were made to optimize the model in order to achieve an accuracy of 75 percent:

* Dropped the status columsn and performed binning and bucketing on ASK_AMT column

![image](https://user-images.githubusercontent.com/99941484/179379684-fb09a9bd-f0db-4eed-8a93-cb6298cc4d22.png)

* Increasing the number of neurons and Hiddenlayers :

* Changing the activation function, first 2 hidden layers using a RELU fucntion while the 3rd Hidden layer and output layer using a Sigmoid fuction we also increased the number of epochs from 10 to 15 :

![image](https://user-images.githubusercontent.com/99941484/179379738-e2005402-7bb2-4c19-b358-d346fb7a1bf0.png)

![image](https://user-images.githubusercontent.com/99941484/179380055-cbb9bd30-161e-4d7e-9dbc-976bfab8bc68.png)


Accuracy achieved - 72.78 Percent

![image](https://user-images.githubusercontent.com/99941484/179380044-f41530f7-61c0-4881-a066-9cc4a6450196.png)


We were still not able to achieve an accuracy of 75 percent.

Accuracy Graph(Optimizations) :

![image](https://user-images.githubusercontent.com/99941484/179380078-f144131d-86b2-4289-b6ee-447b2d2ba80c.png)

## Summary 

Initially when the model was created we achieved an accuracy of 72.8 percent. SInce we wanted to achieve an acuuracy of 75 percent cahnges were made to the model in order to optimize it.
Still we could not achieve a desired frequency of 75 percent which maybe due to insufficient data because of which the model cannot reach the necessary accuracy.
Based on the dataset provided it would be better used Supervise ML model like Random Forrest Classifier to handle large itliers in the data. 


