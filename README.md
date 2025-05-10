# End-of-phase3-PROJECT

# Introduction

A pharmaceutical company wants to start manufacturing the seasonal flu vaccine as a new product line. They would like to know how they can increase vaccine uptake and optimize distribution strategies to ensure that they get to majority of the population. To get better insights the company would want to make data driven decisions.

## Objective

Launch and scale a seasonal flu vaccine product line successfully by increasing the uptake and optimizing distribution.

To get the insights we need, there are several questions we need to answer;
1. Identifying the populations that are less likely to be vaccinated.
2. Which factors drive vaccine acceptance or hesitancy.
3. Where they should prioritize distribution efforts geographically and demographically.

## Data Understanding

The data that was used is the **H1N1 vaccine and seasonal flu vaccine** which was collected during The National 2009 H1N1 Flu Survey (NHFS).The target population for the NHFS was all persons 6 months or older living in the United States at the time of the interview. Data from the NHFS was used to produce timely estimates of vaccination coverage rates for both the monovalent pH1N1 and trivalent seasonal influenza vaccines. The NHFS was conducted between October 2009 and June 2010. It was one-time survey designed specifically to monitor vaccination during the 2009-2010 flu season in response to the 2009 H1N1 pandemic.

There are 3 datasets **test_set_features.csv, training_set_features.csv and training_set_labels.csv** to work with.

## Modeling

Before embarking on the modeling, the data was prepared in the following ways:

Handling the missing values: The missing data in the numerical columns was imputed with the **mean** and categorical columns with the **most frequent value**.

Feature scaling: The numerical features are standardized using **StandardScaler** in the preprocessing pipeline, 0,1.

Data balancing: This is important to avoid bias in regression and classification. Logistic regression is configured to use **balanced class weight** so that it assigns more importance to cases from minority class during training.  

Two models were build using **Logistic Regression and Decision Tree algorithms** and thereafter hyperparameters were employed to tune the two models.

After modeling with the 2 algorithms, Logistic Regression performed best with a ROC AUC of 0.85 which identified strong predictors of the vaccine uptake.

