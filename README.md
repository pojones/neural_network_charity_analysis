# Neural Network Analysis with Alphabet Soup
## Overview
Using machine learning and neural networks, this project extracts information from a dataset and creates a binary classifier capable of predicting whether applicants will be funded by a fictional charity “Alphabet Soup”.
<br/><br/>
The CSV file contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Within this dataset are a number of sections that capture metadata about each organization. The project will preprocess the data, compile a trainable model, then evaluate using the model. The code can then be optimized as needed. The target model performance for this analysis is 75%.
<br/>
## Results
### Data Preprocessing
The following metrics are collected on each organization:
-	EIN—ID number column
-	NAME—Name 
-	APPLICATION_TYPE—Alphabet Soup application type
-	CLASSIFICATION—Government organization classification
-	USE_CASE—Use case for funding
-	ORGANIZATION—Organization type
-	STATUS—Active status
-	INCOME_AMT—Income classification
-	SPECIAL_CONSIDERATIONS—Special consideration for application
-	ASK_AMT—Funding amount requested
-	IS_SUCCESSFUL—Was the money used effectively
The columns “EIN” and “NAME” were removed because they did not offer any relevant data. The target variable is the “IS_SUCCESSFUL” column. This column contains either “0” or “1” depending on the efficacy of the organization. The remaining columns are used as features for the model.
### Compiling, Training, and Evaluating the Model
The first attempt at compiling the neural network consisted of eighty neurons in the first layer and thirty neurons in the second. Both layers were given relu activation functions and the output layer was given a sigmoid activation function:

![](https://github.com/pojones/neural_network_charity_analysis/blob/9d7be5c5db8cd5e3de3912f8274b65b15f8bac6c/images/firstModelAccuracy.png)

The second attempt doubled the nodes in each layer but kept the same activation function:

![](https://github.com/pojones/neural_network_charity_analysis/blob/9d7be5c5db8cd5e3de3912f8274b65b15f8bac6c/images/secondModelAccuracy.png)

The third attempt kept the same double nodes because it increased the speed of the model significantly. However, the activation function in the second layer was changed to sigmoid:

![](https://github.com/pojones/neural_network_charity_analysis/blob/9d7be5c5db8cd5e3de3912f8274b65b15f8bac6c/images/thirdModelAccuracy.png)

The fourth attempt kept the same model but adjusted the incoming data. The columns “STATUS” and “SPECIAL_CONSIDERATIONS” were both removed. This bumped the accuracy of the model over the 73% mark:

![](https://github.com/pojones/neural_network_charity_analysis/blob/9d7be5c5db8cd5e3de3912f8274b65b15f8bac6c/images/fourthModelAccuracy.png)

## Summary
These initial attempts did not create a model that performed better than 75%. Further look at the data and model parameters will be needed. Further analyses with visualization could aid in creating a more accurate model. 
