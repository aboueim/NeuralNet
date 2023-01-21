# Neural Network Analysis

## Overview of the analysis
 
In this project I intend to develop a model that helps Alphabet Soup, an investment company, to make its future investment decisions with more accuracy. In particular, I will use a CSV file including details such as affilitation, organization type, usecase, rtc. on the company's on which Alphbet Soup previously invested, and build up a binary classifier on a neural network model to make future predictions. In doing so, I will use different libaries including Pandas, SKlearn, and Tensorfelow, and write python codes in Jupyter Notebook to implement and run the model. Specifically, first I will read the CSV file, conduct data preprocessing (removing irrelevant columns, checking for binning options, encoding categorical features, splitting data to training and test subsets, and scaling the input features). Next, I will create and complie the neural network model by initializing an instance of the model followed by adding input, output, and hidden layers to the model, and compiling the model using a binary classifier optimizer. Then, I will evaluate and report the model accuracy (a checkpoint folder is also created and the training result is stored in a .h5 file for future references). Finally, I will complement this process by trying different optimization solutions to enhance the model accuaracy.
 
## Results


- In this model I considered the "IS_SUCCESSFUL" feature as the target variable.
- All other variables except the target variable, and those removed in the preprocessing part are used as inputs (features) in the model.
- "EIN", "NAME", and "INCOME_AMT" (due to its improper format) were removed from the model.
- As was instructed, in the initial model I entered a single input layer, two hidden layers (first layer: 80 neurons" and the second layer: 30 neurons), and one output layer.
- The initial model achieved an accuracy of 72.69% which was close to the specified 75% accuracy limit.
- I tried different changes to the input data and the model to increase the model accuracy. First, I remove the "INCOME_AMT" feature due to its improper format. Then, I increased the number of bins for categorical variables with more than 10 unique values to allow for inclusion of more nuances in the model. I also added a third hidden layer (also checked 4 and 5 hidden layers), increased the number of neurons in the hidden layers (up to 300), increased the number of epochs (up to 200), and modified activation functions. Finally, I also tested other optimizers (adamx and Nadam). Unfortunately, none of the changes made could increase model accuracy to above 75%.


## Summary

Below are a summary of the results obtained after all analyses.

1. The ReLU activation function proved to be the best for hidden layers and sigmoid the best function for the output layer.
2. The model accuracy only slightly improved when the number of neurons per hidden layer increased.
3. Adding additional hidden layer was only effective when the third layer was added.
4. Increasing the number of epoch could slightlyimprove the model accuracy.

### Recommendation

It looks that the model hardly can be improved using the available data. To enhance model performance I suggest that the company either use a larger dataset with additional features that allow the model to decipher the inherent complexity of the data or alternatively employ another modeling technique such as super vector machines or random forrest to see if the they result in higher performance (given the number of datapoints and features).
