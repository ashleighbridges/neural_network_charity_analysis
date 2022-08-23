# neural_network_charity_analysis

## Overview
The purpose of this project was to use deep-learning neural networks to analyze the more than 34,000 charitable donations provided by Alphabet Soup and determine their successes. We completed this analysis by:
- Preprocessing the data
- Compiling, training, and evaluating the model 
- Optimizing the model

## Results
### *Data Preprocessing*
 - What variable(s) are considered the target(s) for your model?
    - The target variable for this model is ```IS_SUCCESSFUL```
 - What variable(s) are considered to be the features for your model?
    - The feature variables for this model are ```APPLICATION_TYPE```, ```AFFILIATION```, ```CLASSIFICATION```, ```USE_CASE```, ```ORGANIZATION```, ```STATUS```, ```INCOME_AMT```, ```SPECIAL_CONSIDERATIONS```, and ```ASK_AMT```
 - What variable(s) are neither targets nor features, and should be removed from the input data?
    - The ```EIN``` and ```NAME``` variables were removed from the input data
 
### *Compiling, Training, and Evaluating the Model*
 - How many neurons, layers, and activation functions did you select for your neural network model, and why?
   - This model was created with three hidden layers with 80, 30, and 15 neurons respectively. This gave us a total of 6,911 params. In order to speed up the training process, we used the ```relu``` activation function for the hidden layers. We used the ```sigmoid``` activation function for the output layer since this was a binary classification
 - What steps did you take to try and increase model performance?
    - To attempt to increase model performance, we created 7 bins for the ```ASK_AMT``` since the .nunique() query returned 8747 unique values in this column. We also added a third hidden layer with 15 neurons as well as increased the number of epochs in training from 100 to 250
 - Were you able to achieve the target model performance?
    - Unfortunately, we were not able to achieve target model performance. Our final model accuracy score was 73%, very close to the accuracy score from the second deliverable

## Summary
Our final accuracy score after making multiple optimizations to the model was 73%, below the 75% threshold required for the model to be used by the organization. I would recommend using the Random Forest Classifier model as an alternative to the deep-learning neural network due to the binary nature of the classification. The Random Forest model is also capable of similar performace with less hidden layers, reducing the risk of user-error and unintentional overfitting.
