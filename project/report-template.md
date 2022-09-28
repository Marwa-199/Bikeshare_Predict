# Report: Predict Bike Sharing Demand with AutoGluon Solution
Marwa Ibrahim Alalfi 

## Initial Training
### What did you realize when you tried to submit your predictions? What changes were needed to the output of the predictor to submit your results?
 some values were negative and result should be >= 0.

### What was the top ranked model that performed?
 WeightedEnsemble_L3 with score : -53.085896.

## Exploratory data analysis and feature creation
### What did the exploratory analysis find and how did you add additional features?
some variables require changing datatypes to category in order Autogluon to deal with.
datetime must be changed to datetime not object.

from datetime column we extract hour , day , month, and year.

### How much better did your model preform after adding additional features and why do you think that is?
 new score : - 30.466340 it improved approximately about 25% 
 extracting new features and changing it to category let the model train acts better by classifying these integers as categories in AutoGluon 
 
## Hyper parameter tuning
### How much better did your model preform after trying different hyper parameters?
slight difference

### If you were given more time with this dataset, where do you think you would spend more time?
feature engineering & more hyperparameteter tuning 

### Create a table with the models you ran, the hyperparameters modified, and the kaggle score.

|model       |hpo1    |hpo2    |hpo3    |score|

|initial     | default| default| default|?1.78856|
|add_features| default| default| default|0.6855|
|hpo         |"GBM:'num_boost_round': 100,'num_leaves'(lower=26, upper=66, default=36)"|  "NN_TORCH (num_epochs': 10), activation('relu', 'softrelu', 'tanh')"| " 'num_trials': num_trials,    'scheduler' : 'local',    'searcher': search_strategy "|1.29520|

    "score":[ 1.78856 , 0.6855,  1.29520]


### Create a line plot showing the top model score for the three (or more) training runs during the project.
![model_train_score](https://user-images.githubusercontent.com/76065069/192902425-73e5c392-3959-4ad5-8268-32f0b58e9829.png)

 
 

### Create a line plot showing the top kaggle score for the three (or more) prediction submissions during the project.

 ![model_test_score](https://user-images.githubusercontent.com/76065069/192902438-5432e668-fe32-4109-b6b7-601a9c30f813.png)

 

## Summary
This project is about estimating the bike rental demand of bike rental company.
We implement a whole Machine Learning process inorder to achive our objective which is (Predict number of bikes' demands ) using a Bike_Share dataset downloaded from kaggle.

1- Data wrangling :
2- EDA
3- Model Training & testing
4- Result prediction
5- model tuning 
6- visualization 

