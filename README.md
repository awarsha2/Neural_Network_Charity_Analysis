# Neural_Network_Charity_Analysis

## Overview of Analysis:
The purpose of this analysis is to see if neural network models can be used to predict the successful use of donations and funding for the use of the charity organization Alphabet Soup.

## Results:
Data Preprocessing:
- Target Variable:
	- IS_SUCCESSFUL - evaluation of if the money was used effectively
- Feature Variables:
	- APPLICATION_TYPE - Alphabet Soup application type
	- AFFILIATION - affiliated sector of industry
	- CLASSIFICATION - organization classification by government
	- USE_CASE - use case for funding
	- ORGANIZATION - organization type
	- INCOME_AMT - income classification
	- SPECIAL_CONSIDERATIONS - special consideration for application
	- ASK_AMT - funding amount requested
- Neither (removable data)
	- EIN and NAME - Identification
	- STATUS - current active status

## Compiling, Training, and Evaluating the Model:
- Compilation of Model:
	- Original, 2 hidden layers:
		- 1st Hidden - Leaky Relu
			- 80 neurons
		- 2nd Hidden - tanh
			- 30 neurons
	- Optimized, 3 hidden layers:
		- 1st Hidden - sigmoid
			- 100 neurons
		- 2nd Hidden - leaky relu
			- 40 neurons
		- 3rd Hidden - tanh
			- 15 neurons
- Performance:
	- The original model was unable to achieve the targeted performance of 75%, only reaching 72.6% accuracy. 
	- The optimized model was not much better, only reaching 72.7% accuracy, a small improvement of 0.1%.
- Optimization:
	- Removed the status variable, which seemed unnecessary and overlapped with the target variable. 
	- Added 20 additional neurons to the first hidden layer and 10 additional neurons to the second hidden layer.
	- Added third hidden layer.
	- Altered activation functions of hidden layers. 

## Summary:
- The final 72.7% accuracy rating of the machine learning model was close to the target so I would call it a partial success. Perhaps with more time for data preprocessing and experimentation with the model's structure this could hit and exceed the target accuracy. 
- A Random Forest Model could also be used as an alternative. All the data is tabular and easily convertable to something a Random Forest could utilize. This model would also likely be faster than the neural network. 