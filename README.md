# Neural_Network_Charity_Analysis

## Overview
Create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup using a CSV containing more than 34,000 organizations that have received funding from Alphabet Soup over the years. 


## Results:

### Data Preprocessing
- What variable(s) are considered the target(s) for your model? 
  - The IS_SUCCESSFUL column is the target
- What variable(s) are considered to be the features for your model?
  - APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT
- What variable(s) are neither targets nor features, and should be removed from the input data?
  - EIN, NAME, and USE_CASE was dropped during attempted optimization.

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model?
  - The initial model consisted of 2 hidden layers with 80 in the first and 30 in the second layer using a Relu activation function. For the output we used a sigmoid funcion.
- Were you able to achieve the target model performance?
  - No
- What steps did you take to try and increase model performance?
 
 1. USE_CASE feature was dropped initially with a .1% drop in accuracy. 
 
![Optimization Result 1](https://github.com/K3Rob/Neural_Network_Charity_Analysis/blob/main/Neural_Network_Charity_Analysis/Images/OptRes1.PNG)

2. Second attempt at optimization was increasing the number of neurons in the second layer from 30 to 50 which gave a .5% increase in accuracy.
 
![Optimization Result 2](https://github.com/K3Rob/Neural_Network_Charity_Analysis/blob/main/Neural_Network_Charity_Analysis/Images/OptRes2.PNG)

3. Finally a third layer was added and neurons adjusted to 80, 40, and then 20 neurons per layer giving a .1% drop in accuracy.

![Optimization Result 3](https://github.com/K3Rob/Neural_Network_Charity_Analysis/blob/main/Neural_Network_Charity_Analysis/Images/OptRes3.PNG)


## Summary:
The neural network never reached the goal of 75% accuracy in predicting success. Potential problems faced are that the data became overfitted, or that other features may not be strong predictors. A random forest model could be an alternative to this due to the large amount of data available.
