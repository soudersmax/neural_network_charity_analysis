# Neural Networks and Deep Learning

## Purpose

The purpose of this project is to attempt to create a neural network model that predicts the outcome of loan applications with at least 75% accuracy. 



## Results

### Data Preprocessing

- Target Variable: IS_Successful

- Features: APPLICATION_TYPE, AFFILITATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMOUNT

- Removed Variables: EIN, NAME, STATUS

  

### Compiling, Training, and Evaluating the Model

- Because of the size of the data, I didn't want to increase the width or depth of the neural network by much, if any, so I kept the 2 hidden layers (80 and 30 neurons, respectively). 

- I was not able to achieve optimal performance - my accuracy was fairly static around 72-73% 

- To attempt optimization, I removed  additional variables (STATUS, SPECIAL_CONSIDERATION) and changed the activation function to SeLU. Neither of these were particularly fruitful, and SeLU actually reduced the slight accuracy increase I received from dropping the STATUS column. The SPECIAL_CONSIDERATION column didn't have much effect on the accuracy either way. I also attempted the tanh activation function, just to play around with it, but the accuracy decreased drastically at that time. 

  

## Summary

Overall, this model wasn't particularly successful in classifying the outcomes of loan applications. In fact, previous models (including the AdaBoost model we did a couple weeks ago) were  much more successful. Naturally there are pros and cons to using each different type, but based on what I was able to create in this instance, I wouldn't recommend it for this task. I think that the model could benefit from a much larger dataset, as well as some additional features. 