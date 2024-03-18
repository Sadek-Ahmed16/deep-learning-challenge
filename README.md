# deep-learning-challenge
## Module 21 - Deep Learning Challenge

### Challenge Content

This repository includes the following files needed to to predict whether applicants will be successful if funded by Alphabet Soup:

- 'AlphabetSoupCharity.ipynb'
- 'AlphabetSoupCharity_Optimization.ipynb'
- 'AlphabetSoupCharity_Optimization2.ipynb'


## Overview

This analysis was based on a taget and preprocessed features in the provided dataset, a Neural Network model were utilised to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The model was optimized to achieve a target predictive accuracy higher than 75%.


## Results

### Data Preprocessing

- The target variable for the model is the the 'IS_SUCCESSFUL' colums of the apllications dataset to see if an application is to be successful.
- The chosen features for the model are 'APPLICATION_TYPE', 'AFFILIATION', 'CLASSIFICATION', 'USE_CASE', 'ORGANIZATION', 'STATUS', 'INCOME_AMT', 'SPECIAL_CONSIDERATIONS', 'ASK_AMT' which are the the determining factors to predict the success of a application.
- The variables which have been removed from the input data are 'EIN', 'NAME' because they are neither targets nor features, as they are only used to identify each application.

### Compiling, Training, and Evaluating the Model

For each of the models used, The RelU activation was using for each hidden layer and the Sigmoid function was used for the outpul layer

 - Initial Model: 2 hidden layers were used with 60 and 30 neurons
   
   268/268 - 1s - loss: 0.5581 - accuracy: 0.7254 - 700ms/epoch - 3ms/step
   Loss: 0.5581448078155518, Accuracy: 0.7253644466400146

 - Optimized: 3 hidden layers were used with 27, 20 and 14 neurons
   
   268/268 - 0s - loss: 0.5574 - accuracy: 0.7257 - 455ms/epoch - 2ms/step
   Loss: 0.5573567748069763, Accuracy: 0.7257142663002014

 - Optimized 1: 3 hidden layers were used with 27, 18 and 12 neurons
   
   268/268 - 1s - loss: 0.5607 - accuracy: 0.7261 - 1s/epoch - 4ms/step
   Loss: 0.5607113242149353, Accuracy: 0.726064145565033

As you can see from the results, the target model performance of 75% was not achieved, however thorugh optimization there were slight improvements the the accuracy percentage in the models.

To try and increase the model performance, the cut off points for variables with more than 10 unique values were increased, having more input features for the model. Then decreasing the cut off point in the third model reducing the input features. In the optimized models, an extra layer was also added whilst decreasing the number of neurons in the hidden layers. Finally, the epochs were increased from 100 to 150 to see if the model would reach its optimum accuracy if it passed through the training dataset more.


## Summary

Looking at the results, we were not able to achieve the desired accuracy of 75%, only achieving 73.5-72.6%. So, we can say that that the model will be able to predict the success of an application only 72.6% of the time.

One way in which we could increase the models performance is to try different architectures for the neural network, such as increasing the number of hidden layers, adjusting the number of neurons in each layer, or using different activation functions e.g., tanh (considering the nature of the features in the dataset). We can also explore additional features or transformations of existing features that might capture more information relevant to the prediction task, so that only the more relavent features are using to determine and applications success without sacricing too much data. In addition to this, we can consider using different machine learning algorithms such as decision trees, support vector machines (SVM), or logistic regression, which might be suitable for the binary classification task and could achieve the desired accuracy, which again can help identify the approriate features needed in the model by preprossessing its features more accurately.





