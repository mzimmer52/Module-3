# Introduction

### Having chosen to work with the Tanzania Waterpump dataset, I knew coming into the project that the majority of my work would involve data preprocessing, feature engineering, and training many models. I also knew I would need to set up some sort of process where I could automatically transform my testing data to have the same features as the data I trained my model on. 




# Models Used:
### Random Forest
### Decision Tree
### Adaboost
### XGBoost
### Gradient Boost


<img src="Pictures/Results">


### Finding the right hyperparameters was also a big struggle during the project. Using GridSearchCV, I was able to find the optimal paramaters for the majority of my models, even though some models took 4+ hours of training time in order to find the optimal parameters. 


## Random Forest Optimal Parameters:

 <img src="Pictures/Params">
 
 # Making Use of the Pipe and Align Function
 
 ### A big realization had during the middle of the project was if there was another way to transform new testing data the same way as my training data without having to do all of it manually. Using the Pipe function in Pandas, I was able to efficiently set up a multitude of functions that would help me transform test data in a single line of code. 
 
 
  
<img src="Pictures/Pipe">

## As seen in the code above, all the functions defined earlier in the data preprocessing stage were combine with "pipe" in order to achieve fast, efficient, and effortless data transformations to new data.


<img src="Pictures/Align">


## Another big realization was that I could deal with different categorical variables in either the testing or training data by using the align function in pandas, making it possible to run the same model on each dataset despite the difference in the number of columns. As seen above, both datasets have the same number of columns after the function is run.


# Confusion Matrix

<img src="Pictures/Matrix">


## The confusion Matrix for training and test data (using sklearn's train_test_split) is shown above. As we can see, the greatest source of errors for the model occur where the model predicts the pump is functional, while in reality it is not. Future models can adress/fix issues pertaining to specific errors like this.


## Interestingly enough, while not shown in this document, all the models that were trained all had the most amount of their errors where the pump was actually non-functional but labeled functional




