## Project 2 Overview

## Presentation Link & Google Colab Link

https://docs.google.com/presentation/d/1x6WQz60sm8E2nrq6oml_08uXx1_6KKVmHU9o3wt5lWs/edit?usp=sharing




## Scope and Purpose of Project

For Project 2, the project team will be working off the findings in Project 1 (github link here: https://github.com/NatashaPredov/Project-1-.git) to further understand how the learnings from the last few Module's can work to benefit those applying them in real life situations. 

To summarize the scope from Project 1: 
- Wanted to investigate and determine a predictive model for the long term behaviour of relatively stable ETFs.
- Wanted understand how this model would react and change due to the unforseen impacts the COVID-19 pandemic had on the Canadian Banks. 
- The timeframe of the model data that the team will be analyzing covers 4 years: August 2016 through July 2020. While the validation data will cover: August 2019 through July 2020 - 6 months before and after the February 2020 COVID-19 crash. Due to this being unforseen and very out of the ordinary, the team will be ignoring the data up until Feb 2020 then picking our analysis back up 6 months post crash.

Now to extend from Project 1, Project 2's scope entails that the project team wanted to try to trade BNS in a way that would beat a buy and hold strategy relative to the other correlated bank stocks. The y variable, which is the target variable is the Bank of Nova Scotia stock otherwise represented henseforth as BNS. 

The baseline, that will represent the buy and hold strategy will come from the Monte Carlo simulation from BNS with its CI closer to the top end of CI. 

To ensure we meet the technical requirements of project 2, we will be using google colab (link: https://colab.research.google.com/drive/1oMDA37RPqLsV02G0zDd6kaWDExMvUDVi) to work in an Agile framework methedology to prepare a training and testing dataset. 

For this project we will be creating three machine learning models to fit and apply the data to, to determine which model returns the best trading performance. 

The timeline for this project covers: Aug 2017 - Aug 2022 per reccomendation for a 5 year period to ensure accurancy and industry standard. 

The three models are as follows:
Model 1: Machine Learning model using PyeCarrot

Model 2: Neural Network

Model 3: 

## Analysis, Conclusions and Implications

30 day rolling correlation plots for each of the banking stocks 

### Model 1: Machine Learning model using PyeCarrot
Supervised machine learning classification algorythm that predicts if a security is increasing or decreasing over a time period.
 * Modeling Data Availability: Consider when data is availible   
    ![Modeling Data Availibility](images/Modeling_Data_Availability.png)
 *  Modeling Objective: Simple Model with Shift 
    1. Green: Data is availble to create models and predictions.
    2. Shift 6 days: Pridict up to 6 days in the future
    3. Yellow/Red: Data is not availble for modeling or predicting
    ![Modeling Objective](images/Intro_Modeling_Objective.png)
 * Model Training Timeline: Complex Model with variable Shift and Interval
    1. Target (y variable) interval is 7 days
    2. Features (x variables) are sifted 14 to 58 days
    3. Features (x variables) intervals vary 4 to 16 Days
    4. Model is build from the past (Jan 1, 2014) to Present. Note: The ealiest possible target interval date is yesterday. 
    ![Model Training Timeline](images/Model_Timeline_Training.png)
 * Model Predicting Timeline: Complex Model with variable Shift and Interval
    1. First Prediction is for Day 0
    2. Minimum Feature(x) Shift (CM.TO = 15) is the maximum day of future predictions (days 0 to 14). 
    ![Model Predicting Timeline](images/Model_Timeline_Predicting.png)
 * Trading Plan
    1. Predict a sequence of increases or decreases.
    2. Enter Trade: At the begining of the squence.  
        a. Long (buy) up-trends  
        b. Short (sell) down-trends  
    3. Exit Trade: With a trailing stop loss.  
        a. 1 Standard deviation of daily percent change in the opposit direction  
        b. Emperical Rule: 84% of the daily changes will be in the correct direction.  



### Model 2: Neural Network

Rational for:
- activiation: normal linear
- epochs: 100 

Overfitting and accuracy for train test and val 

Model 3: 


## Connection to Course Content

## Areas of challenge

## Usage and Installation instructions

To view this project, follow the main branch found in this Github repo to the final code that encompasses all of the contributions made by the team members.

The code which is submitted is commented with concise, relevant notes that other developers can understand so future extensions on the work submitted can be explored if needed.


## Technical Requirements
The technical requirements for Project 2 are as follows:
- (DONE) Create a Jupyter Notebook, Google Colab Notebook, or Amazon SageMaker Notebook to prepare a training and testing dataset.
- Optionally, apply a dimensionality reduction technique to reduce the input features, or perform feature engineering to generate new features to train the model.
- Create one or more machine learning models.
- Fit the model(s) to the training data.
- Evaluate the trained model(s) using testing data. Include any calculations, metrics, or visualizations needed to evaluate the performance.
- Show the predictions using a sample of new data. Compare the predictions if more than one model is used.
- Save PNG images of your visualizations to distribute to the class and instructional team and for inclusion in your presentation and your repo's README.md file.
- Use one new machine learning library, machine learning model, or evaluation metric that hasn't been covered in class.


 Create a README.md in your repo with a write-up summarizing your project. Be sure to include any usage instructions to set up and use the model.
