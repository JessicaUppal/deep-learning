Overview 
The non-profit foundation Alphabet Soup wants to create an algorithm to predict whether or not applicants for funding will be successful. Using machine learning and neural networks, use the features in the dataset to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.
Data Pre-processing
The target variable for our model is:
* **IS_SUCCESSFUL** 

The variables that are the features for the model are:

* **APPLICATION_TYPE**—Alphabet Soup application type
* **AFFILIATION**—Affiliated sector of industry
* **CLASSIFICATION**—Government organization classification
* **USE_CASE**—Use case for funding
* **ORGANIZATION**—Organization type
* **STATUS**—Active status
* **INCOME_AMT**—Income classification
* **SPECIAL_CONSIDERATIONS**—Special consideration for application
* **ASK_AMT**—Funding amount requested

Columns that are neither targets nor features, and will be removed from the input data are:

* **EIN** and **NAME** 
Compiling, Training, and Evaluating the Model
How many neurons, layers, and activation functions did you select for your neural network model, and why?
•	Two hidden layers with relu activation
•	First hidden layer contains 10 neurons
•	Second hidden layer contains 5 neurons
•	Output layer with sigmoid activation 
The activation functions were chosen because they had been demonstrated in previous models, and the number of neurons and hidden layers were selected to allow the best performance of the model, without large computational needs that would essentially slow down the process. The second hidden layer contains half the number of neurons as the first hidden layer, as recommended here: https://stats.stackexchange.com/questions/181/how-to-choose-the-number-of-hidden-layers-and-nodes-in-a-feedforward-neural-netw
Were you able to achieve the target model performance?
The target model performance was 75%, however this was not achieved in my initial model, nor after model optimisation. My models were only able to achieve a 72% accuracy.
What steps did you take to try and increase model performance?
•	Increase hidden layers from 2 to 3
•	Adding number of epochs to the training regimen
•	Increasing neurons in hidden layers from 10 and 5 to 50 and 25
Summary
The highest accuracy was 0.7283 in optimisation model two, where number of epochs were increased from 100 to 200. This wasn’t a significant increase from the initial model accuracy of 0.7261.

Manipulating the input data by checking for outliers and missing data may help to increase accuracy, along with dropping more columns and changing the number of values in the bin. Changing the dataset however, can be limiting as important data may be dropped and further decrease accuracy. To improve accuracy, you could also use a different model, such as the Random Forest Algorithm
Which uses cross validation to increase accuracy, handling missing values whilst maintaining the dataset. Overfitting can also be avoided by using more trees.
