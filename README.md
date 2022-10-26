# Neural Network Charity Analysis

## Overview of the Analysis
This analysis creates a model using features of provided dataset to create binary classifier that predicts whether applicants will be successful if funded by Alphabet Soup using __Tensorflow__ to implement machine learning__ and __neural network__ .  With the help of _Pandas__ and __Scikit-Learn the dataset is preprocessed in order to compile, train and evaluate the neural network model. 

## Results

* Data Preprocessing

    1.	The target variable for this model is “__IS_SUCCESSFUL__”.
    2.	The feature variables for this model are __”APPLICATION_TYPE”, “AFFILIATION”, “CLASSIFICATION”, “USE_CASE”, “ORGANIZATION”, “STATUS”, “INCOME_AMT”,                       “SPECIAL_CONSIDERATIONS”, “ASK_AMT”__ .
    3.	__“EIN”__ and __“NAME”__ are neither feature nor target variables and should be removed from the input data.
    
* Compiling, Training and Evaluating the Model

    1.	There are two layers with 80 and 30 neurons respectively using __”rule”__ and __”sigmoid”__ activation functions. 
    2.	This model did not achieve 75% accuracy. Model’s accuracy is 72%.
    
        ![model_accuracy](https://user-images.githubusercontent.com/107717882/197937154-88c9bb09-0913-434c-b7b8-0c069af16864.png)

    
    3.	To achieve desired accuracy, three layers of 90, 60 and 30 neurons has been added with “tanh” and “sigmoid” as input layer activation functions and “rule” as           output layer activation function. Also, “SPECIAL_CONSIDERATION” and “USE_CASE” columns are removed to reduce noise. The __”INCOME_AMT”__ column has been               binned. 
        The desired accuracy has not been achieved using all these optimizations. Acuracy is still 72%, if we play with activation functions, we get 46%                       accuracy.
        
        ![optimization_accuracy](https://user-images.githubusercontent.com/107717882/197937454-68617339-f218-4e89-96b5-47a069ee68b5.png)



## Summary

This model didn’t reach to desired accuracy more than 75%. After trying all optimizations, model’s performance couldn’t improve much. Accuracy is still 72%. Using different activation functions like “tanh” couldn’t improve accuracy. To achieve accuracy more than 75% , we should add more dataset , feature selection is also not helping here as none of the feature or combination of features  are not strong enough to decide target variable values.  Normalization and rescaling is there but they do not make any difference on performance. 
In this situation _Random Forest Model__ can help as its combines multiple smaller decision trees into a more robust and accurate model. This might increase accuracy.  
