# Tanzania Water Wells (Classification Models)

**Author:**<br />
Jawwad A. Siddiqui<br />
Data Scientist<br />
https://github.com/jsiddiqui85<br />
https://www.linkedin.com/in/jsiddiqui85/<br />


# Overview

This project uses classification to model and predict the state of water wells in the African nation of Tanzania.  The purpose for the predictive model is to assist the goverment officials at **The Tanzania Commission for Water** to find water wells that are **not functioning at all** or that are **functioning but require repair** for the agency to contract out the work that is needed to bring these water wells up to functioning level.  

I have used a curated data set found on **DrivenData.com** to run my predictive models against.  Prior to cleaning the data, this dataset contained over 60k rows along with 30+ features.  


# Business Understanding
**The Tanzania Commission for Water** is a federal agency in the African State of Tanzania primarily responsible for the cleaniness and safety of the water that is supplied to the general public and residents of Tanzania.  

Currently, Tanzania lacks the ability to provide a safe source of drinking water to over **50%** of their population.  Although, there have been many attempts to correct this issue over the years, so far all of those attempts have fallen short of their objectives - leaving **45%** of their water wells in need of major repairs.  
My goal with this project is to help **The Tanzania Commission for Water** and the director of this agency with identifying which wells need to be repaired currently, while also prediciting on which of these wells will need to be repaired in the future in order to maintain the cleanliness and safety of the water that is supplied to the Tanzania population.  


# Data
My model and recommendations come from work done on the Tanzanian Water Wells data set found on Driven Data.  From this dataset, I looked at various features that would best predict the water wells that need to be repaired.  My best model is able to predict with an 89% accuracy to identify which water wells need to be repaired and this is what I have based my final recommendations off of.


# Methods
The target variable that I am making classification models to predict on is 'status_group'.  I created a new column named 'status_class' to transform the 'status_group' column into a classification variable, specifically creating a multi-class target that includes: 'non functional: 0', 'functional needs repair: 1', and 'functional: 2'.


# Classification Models

I determined that in order to predict which water wells will need to be repaired to be deemed functional in the future, that I would need to utilize how accurately my model is performing.  Therefore, I have resorted to using the accuracy score for all of the models explained below.

I took an iterative approach to model building, trying to improve on my previous model accuracy score with each iteration.  I also leveraged pipelines to reduce data leakage with each model.

1. DummyClassifier: this model was created to compare my accuracy scores 
2. LogisticRegression: this model was created using the default parameters simply to compare results for further modeling
3. RandomForest: an ensemble this model was created next because it outputs the class that is selected by the most trees, while correcting overfitting to the training set
4. XGBoost: this model was chosen due to its relative speed and performance when compared to the other models above - due to time constraints, this model was chosen to ensure I could meet the requirements of the project while delivering another accuracy score

# Results
