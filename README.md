# Neural_Network_Charity_Analysis

## Overview 

Using knowlegde of machine learning and neural networks, we will use the features in the provided dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The provieded dataset is a CSV containing more than 34,000 organizations that have received funding over the years.  Within this dataset are a number of columns that capture metadata about each organization. Using this data we will preprocess the data for a neural network model, complie, train, and evaluate the model, then optimize the model. 

## Results

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
    - The IS_SUCCESSFUL column is considered the target of the model. 

- What variable(s) are considered to be the features for your model?
    - We will be dropping a few columns, but the ones we keep are considered the features of the model.

- What variable(s) are neither targets nor features, and should be removed from the input data?
    - Since we will be dropping the EIN and NAME columns, they are neither targets or features within the model.

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
    - 