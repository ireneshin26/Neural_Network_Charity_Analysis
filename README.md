# **Neural Network Charity Analysis**

## **Overview of the analysis**
AlphabetSoup is a non-profit philanthropic foundation dedicated to helping organizations that protect the environment, improve people's well-being, and unify the world. The organization has raised $10B in the past 20 years which were used to invest in lifesaving technologies and organize reforestation groups. 

This analysis focused on the impact of each donation and vet potential recipients to ensure that each donation is impactful, specifically to predict which organizations are best to donate to and which are high risk. The analysis was done using data from a CSV file from the AlphabetSoup's business team which contained a list of 34,000 organizations that AlphabetSoup has funded over the years. 

The data included columns of metatdata of each organization:
* EIN and NAME—Identification columns
* APPLICATION_TYPE—Alphabet Soup application type
* AFFILIATION—Affiliated sector of industry
* CLASSIFICATION—Government organization classification
* USE_CASE—Use case for funding
* ORGANIZATION—Organization type
* STATUS—Active status
* INCOME_AMT—Income classification
* SPECIAL_CONSIDERATIONS—Special consideration for application
* ASK_AMT—Funding amount requested
* IS_SUCCESSFUL—Was the money used effectively


## **Results** 

### **Data Preprocessing**
* What variable(s) are considered the target(s) for your model?
  * The variable that is considered the target is the "IS_SUCCESSFUL" column since the data depicts whether the donations were used effectively. This is also the dependent variable.


* What variable(s) are considered to be the features for your model?
  * The variables that are considered as the features for the model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT. These variables are the independent variables.


* What variable(s) are neither targets nor features, and should be removed from the input data?
  * The EIN and NAME columns do not provide any useful data so was dropped in the analysis. 


### **Compiling, Training, and Evaluating the Model**
* How many neurons, layers, and activation functions did you select for your neural network model, and why? 
  * For the deep neural network model, 80 neurons were in the first hidden layer and 30 neurons were in the second hidden layer. The ReLU activation function was utilized on both hidden layers. An advantage for using the ReLU activation function is that it identifies nonlinear characteristics from the input values. If the output of the linear transformation is less than 0, the neurons will be deactivated.

* Were you able to achieve the target model performance?
  * No, the accuracy of the target model was 73.59% as shown in the screenshot below.
<img width="651" alt="Image_1" src="https://user-images.githubusercontent.com/110875578/209252799-3c6f92c0-0148-415e-bc98-edeb2e17de9d.png">

* What steps did you take to try and increase model performance?
  * To optimize model performance, a third hidden layer with 15 neurons was added and the activation functions were adjusted. The first hidden layer used the ReLU activation function, while the second and third layers used the Sigmoid activation function. In all three attempts, the accuracy of 75% was not reached as shown in the screenshots below.

  Attempt 1:
  <img width="655" alt="Optimization_1" src="https://user-images.githubusercontent.com/110875578/209253035-4dfcd3de-b442-4105-87ec-d5f5cc6f5d63.png">

  Attempt 2:
  <img width="645" alt="Optimization_2" src="https://user-images.githubusercontent.com/110875578/209253036-61bffc47-3ee4-483b-8568-6c7f669b9cce.png">

  Attempt 3: 
  <img width="648" alt="Optimization_3" src="https://user-images.githubusercontent.com/110875578/209253037-387f1605-ab70-4c53-b6db-17a8caf75cc4.png">


## **Summary**
In this analysis, we tried to optimize the model but the performance of 75% was not achieved. A recommendation would be to adjust the model by adding more neurons to the hidden layer or adding more hidden layers. 
