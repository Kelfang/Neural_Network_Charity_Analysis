# Neural Network Charity Analysis

## Project Overview

The motivation behind this project is to utilize machine learning and neural networks to create a binary classifier that can predict whether applicants will be successful if provided charitable funding from Alphabet Soup. 

A formulaic approach was taken in an effort to achieve the desired results using a .csv file with data from 34,300 charitable organizations. This process included the following steps:
1.	Preprocess the data for a Neural Network Model
2.	Compile, Train, and Evaluate the Model
3.	Optimize the Model – I performed four different variations of optimization

## Resources
* Python 
* TensorFlow – with Keras
* Scikit-learn library
* Pandas library
* Jupyter Notebook
* Data Sources: .csv and .ipynb files

## Results

Below I will expound upon the steps taken to complete this project and provide a summary of my conclusion. 

### Data preprocessing
![pre_process_data](https://github.com/Kelfang/Neural_Network_Charity_Analysis/blob/main/images/pre_process_data.png)

*	The variable “IS_SUCCESSFUL” was the target for my model.
* The variables marked in the image above indicates the features used during this project. For machine learning and specific to neural networks I did not seek to eliminate any of these during the project.	
* The variables EIN and Name were removed because they are simply identifiers that do not qualify as a measurable property and have no bearing on the outcome.

-------------------------------------------------------------
### Compiling, Training, and Evaluating the Model
![most_successful_attempt](https://github.com/Kelfang/Neural_Network_Charity_Analysis/blob/main/images/most_successful_attempt.png)


* In my most successful model with 73.07% accuracy (still below the targeted accuracy of 75%), I had my neural network model set up with the following:
  - Layers: 2
  - Neurons: First Layer = 100; Second Layer = 40
  - Activation function(s): First and Second Layer = ReLU
  - Activation function: Output Layer = Sigmoid

*	As you can see, I was not successful in reaching the target model performance after four attempts. 

* Here is a rundown of some of the steps I took to increase the accuracy metric:
  - Adjusting the number of neurons which meant adding and/or subtracting them from all layers.
  - Adding a third layer of neurons and adjusting the activation functions among the hidden layers.
  - On my final attempt, I utilized the KerasTuner and further adjusted some of the layers, neurons, and activation functions based on the model hyperparameters.


_<sub>To view all of the code used for optimizations, click [here](https://github.com/Kelfang/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.ipynb).</sub>_

-------------------------------------------------------------
## Summary

Overall, I find this dataset to be simple and straightforward. While we had data from over 34,000 organizations to work with, the features provided were not robust. I intentionally did not remove any other columns from my optimizations because I felt that the data was already lean for neural network modeling. Based on my analysis, I theorize that removing features would only further reduce the accuracy and increase the loss. 

I do believe that this dataset, in the current form, is better suited for Supervised Learning since there is a distinct goal and the data is well labeled. However, if more features were being collected and the relationships between those features were more complicated, I would recommend revisiting deep learning. 
