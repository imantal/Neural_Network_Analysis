# Neural_Network_Analysis
<div align="justify"> 
  
## Overview of the Analysis
The purpose of this project was to use neural network to create a binary classifier that was capable of predicting whether applicants would be successful if funded by the company, Alphabet Soup. The provided data was not ideal, so it needed to be processed to fit the neural network models. 

## Data overview and preparation
The original data provided in the CSV format included information for more than 34,000 organizations that had received funding from Alphabet Soup over the years. Within this dataset were a number of columns that capture metadata about each organization, such as application type, affiliated sector of industry, use case for funding, income classification and funding amount requested. The data cleaning included removing the non-beneficial columns and dropping the null rows. Once the unique values for each column were identified, density plots were used to determine the distribution of the column values and the need for binding the data. It was realized that some of the categories in the “APPLICATION_TYPE” and “CLASSIFICATION" columns were needed to bin together. Once done with binning the data, the categorial variables were identified and encoded using one-hot encoding. The processed data was split into features and target (column “IS_SUCCESSFUL”) and then into training and test arrays. Finally, the Scikit-Learn’s StandardScaler was used to standardize and scale the numerical variables.

## Compile, train and evaluate the neural network model 
TensorFlow was used to design a neural network/ deep learning model to create a binary classification model that could predict if an Alphabet Soup–funded organization would be successful based on the features in the dataset. The model included two hidden layers with 80 and 30 neurons. Relu and Sigmond activation functions were used for the hidden and output layers, respectively. The model was compiled using the binary_crossentropy as the loss function and the Adam optimizer. A callback was created to save the model's weights every 5 epochs. The model was evaluated using the test data to determine the loss and accuracy. Finally, the results were saved to an HDF5 file. The loss and accuracy were 0.5570 and 0.7254, resopectively. 

## Neural network model optimization  
The model optimization was performed in order to achieve a target predictive accuracy higher than 75%. Additional four models were created with the adjustments listed below:
  
•	Model optimized_1: the input data was adjusted to ensure that there were no variables or outliers that were causing confusion in the model. Column “STATUS” was dropped since there was only a few cells with 0 values. More bins were created for “AFFILIATION”, “USE_CASE” and “ORGANIZATION” columns.
  
•	Model optimized_2: more neurons were added to the hidden layers of the first model. 120 and 60 neurons were used for the first and second hidden layers. 
  
•	Model optimized_3: two more hidden layers were added to the first model 
  
•	Model optimized_4: Leaky_relu activation function was used for the second hidden layer of the first model.

## Results and conclusions  
A neural network was used to create a binary classifier to predict whether applicants would be successful if funded by the company, Alphabet Soup. The dataset included information for more than 34,000 organizations that had received funding from Alphabet Soup over the years. The analysis included processing the data for the neural network model, compiling, training, and evaluating the model and finally optimizing the model to achieve better performance. The loss and accuracy for each model is summarized in Table 1. Although, a slight improvement was observed by adjusting the input data as evident by model 1 accuracy, the optimized models were not able to achieve a better accuracy compared to the original model. Considering the type and size of the data, LogisticRegression, Random Forest classifiers or SVM machine learning models could provide better performance compared to the neural network models.
  
  ![image](https://user-images.githubusercontent.com/103223944/185270466-723b72ab-c4e2-415c-9ca6-5f5b54f3066e.png)
  
  
