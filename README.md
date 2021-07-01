# Neural_Network_Charity_Analysis

## Overview 

Using knowlegde of machine learning and neural networks, we will use the features in the provided dataset to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup. The provieded dataset is a CSV containing more than 34,000 organizations that have received funding over the years.  Within this dataset are several columns that capture metadata about each organization. Using this data, we will preprocess the data for a neural network model, complie, train, and evaluate the model, then optimize the model. 

## Results

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
    - The IS_SUCCESSFUL column is considered the target of the model. 

- What variable(s) are the features for your model?
    - We will be dropping a few columns, but the ones we keep are considered the features of the model.

- What variable(s) are neither targets nor features, and should be removed from the input data?
    - Since we will be dropping the EIN and NAME columns, they are neither targets nor features within the model.

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - Attempt 1:
        First, I tried adding more neurons, and third hidden layer. Knowing that adding more neurons increases overfitting, I also added an additional hidden layer. Adding more hidden layers allows neurons to train on activated input values, instead of looking at new training data. Therefore, a neural network with multiple layers can identify nonlinear characteristics of the input data without requiring more input data. 

        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_1.png)

    - Attempt 2: 
        I removed the third hidden layer and ran the training model using the checkpoints method. Using this method, we can restore model weights, and reduce computation time. I also reduced the number of neurons to see what the effect would have on the model. 

        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_2.png)

    - Attempt 3: 
        I kept the same approach from the second attempt using checkpoint, but I increased the number of neurons to see the affect.

        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_3.png)

    - Attempt 4:
        Sticking with checkpoint approach, I decreased the number of neurons and added a third hidden layer with the sigmoid activation function.

        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_4.png)

- Were you able to achieve the target model performance?
    The target accuracy was 75%.  Below are the results for each attempt:

    - Attempt 1
        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_1_results.png)

    - Attempt 2
        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_2_results.png)

    - Attempt 3
        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_3_results.png)

    - Attempt 4
        ![image](https://github.com/snkty8/Neural_Network_Charity_Analysis/blob/main/images/attempt_4_results.png)

    As shown from the images, I did reach the target goal for accuracy. Although, I was able to gradually raise the level of accuracy, it seemed to level out at 72.9%.

- What steps did you take to try and increase model performance?
    - As shown above in a previous section, I tried increasing and decreasing the number of neurons, adding an additional hidden layer with a different activation function, and using the checkpoint method. 

## Summary 

The goal was to reach an accuracy level of at least 75%.  Although I was able to gradually raise the level of accuracy from 46.7% to 72.9%, I was not able to reach the goal.  We could use a different to train the data.  Support Vector Machine Learning would not be best because the data not linear.  We could use Random Forest Machine Learning since it is close to neural network, but training time would be much longer than that of neural network training.  Another point is that the model would more than likely yeild the same accuracy level. If we stick with the current model, we could try decreasing the number of epochs and removing noisy data. 

