# Neural Network Charity Analysis

## Overview
AlphabetSoup is a non-profit foundation dedicated to helping organizations that protect the environment, improve people’s well-being, and unify the world. AlphabetSoup has raised and donated over $10 billion USD dollars in the past 20 years. This money has been used to invest in lifesaving technologies and has organized reforestation groups, around the world.     

The purpose of this analysis is to analyze the impact of each donation and vet potential recipients. This helps ensure the foundation’s money is being used effectively. Unfortunately, not every donation the company makes is impactful. In some cases, an organization will take the money and disappear. In trying to predict which organizations are worth donating to and which are too high of a risk, a mathematical, data driven solution is created, which can do this accurately. 

A deep learning neural network is designed and trained, using python’s tensorflow library. The model evaluates all types of input data and produces a clear decision-making result. Utilizing the features in the provided dataset, a binary classifier is created that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. The dataset contains more than 34,000 organizations that have received funding from Alphabet Soup over the years. Metadata about each organization is captured within the following columns, in the dataset: 

* **EIN** and **NAME**—Identification columns
* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested
* **IS_SUCCESSFUL**—Was the money used effectively


### Resources Utilized to Complete Analysis
* **Data Sources:** 
[charity_data.CSV](https://github.com/cmmgw/Neural_Network_Charity_Analysis/blob/main/Resources/charity_data.csv) 
* **Languages:** Python
* **Python Dependencies:** scikit-learn, pandas, tensorflow, os
* **Tools:** MS Excel, Google Collaboratory 

## Results

### Data Preprocessing
* **What variable(s) are considered the target(s) for the model?** The "IS_SUCCESSFUL" column is the target, as it contains data on whether the donations were used effectively. The target variable is the dependent variable, y.  
* **What variable(s) are considered to be the features for the model?** The following variables are considered to be the features for the model: APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. These variables are the independent variables, x.
* **What variable(s) are neither targets nor features, and should be removed from the input data?** The identification columns EIN and NAME were dropped, as they are not beneficial when completing the analysis.

### Compiling, Training, and Evaluating the Model
* **How many neurons, layers, and activation functions were selected for the neural network model, and why?** For the deep neural network model, 80 neurons were in the first hidden layer and 30 neurons were in the second hidden layer. The ReLU activation function was utilized on both hidden layers. An advantage for using the ReLU activation function is that it identifies nonlinear characteristics from the input values. If the output of the linear transformation is less than 0, the neurons will be deactivated. 
* **Was target model performance achieved?** Performance of 75% accuracy was not achieved by the target model, as it attained 73.78%. 
* **What steps were taken to try and increase model performance?** In an attempt to optimize model performance, a third hidden layer was added with 15 neurons and the activation functions were adjusted. The first hidden layer maintained the ReLU activation function, however the second and third layers utilized the Sigmoid activation function. Unfortunately, performance of 75% was not achieved by the optimized model. 


## Summary
Despite attempting to optimize the model four times, performance of 75% was not achieved. In an attempt to optimize model accuracy, it is recommended to adjust the number of hidden layers and neurons, along with the corresponding activation functions for each layer.