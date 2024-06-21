## Titanic passenger survival prediction
This repository contains the code and documentation for my project on the Titanic passenger survival prediction, a competition hosted by Kaggle ([link](https://www.kaggle.com/competitions/titanic)). The goal of this project is to apply data mining techniques to predict the survival of passengers aboard the Titanic using various machine learning models

### Dataset
The dataset used in this project is the Titanic dataset provided by Kaggle. It contains information about passengers aboard the Titanic, including their survival status, age, sex, passenger class, and more.
given below is a list of all headers in the dataset

| Header      | Description                                                                            |
|:-----------:| -------------------------------------------------------------------------------------- |
| PassengerId | unique ID assigned to each passenger                                                   |
| Survived    | survival status of the passenger - 1 if the passenger survived, else 0                 |
| Pclass      | Ticket class (1, 2, 3)                                                                 |
| Name        | name of the passenger                                                                  |
| Sex         | sex of the passenger                                                                   |
| Age         | Age of the passenger in years - Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5                                                          |
| SibSp       | number of siblings / spouses aboard the Titanic                                        |
| Parch       | number of parents / children aboard the Titanic                                        |
| Ticket      | ticket number                                                                          |
| Cabin       | Cabin number                                                                           |
| Embarked    | port of embarkation for the passenger (C = Cherbourg, Q = Queenstown, S = Southampton) |
| Fare        | Passenger fare                                                                         |

### Requirements
This project makes use of the following libraries and packages
- Python 3.7+
- Pandas
- Scikit-learn
- matplotlib
- Tensorflow
- Seaborn

this project can be run on google colab notebooks 

to run locally, install the requirements using `pip`

```
pip install -r requirements.txt
```

### installation
Clone the repository on your computer using the following commands

```
git clone https://github.com/Amm4r03/data-mining-project-411.git
```

### Model evaluation
We made use of the following models :
- logistic regression
- random forest
- naive bayes
- neural network

The models were evaluated on the basis of their accuracy and the score they recieved on the test data from kaggle (value between 0 and 1)

#### Results
From our list of models and approaches, we concluded that the neural network were able to get the the best score from kaggle standing at 0.78468

the results in detail can be accessed from the `results.md` page ([link](results.md))

### Authors
1. Ammar Ahmad Kidwai ([github](https://github.com/Amm4r03))
2. Iliya Sabat ([github](https://github.com/iliyasabat))
3. Mohd. Waize Ali Khan
