# covid19-regression-projects
## Overview
"Keep your window open!", "Keep your humidifier off when you're inside!", "Don't sit where the airconditioning wind is blowing at you!"...
Moving to my college dorm during the Summer of 2020, despite of the outbreak of COVID-19 earlier that year, the text messages I would get from my parents would be limited to articles from a local newspaper with a very unusual name with titles along the lines of '10 ways to fight COVID-19 at home' or 'How college students are spreading COVID-19." From a parent who's dropping off their youngest child to college in the midst of a deadly pandemic's perspective, I totally do the same in the worries and hopefullness that I would read those articles and be a little bit more careful. 

But... what really spreads COVID-19? 

With the recent outbreak of COVID-19, researchers around the world have been trying to distinguish the environmental characteristics in which the virus is more likely to survive in. 'What causes covid-19' is a rather too theoretical of a question, a question that seems too easy but at the same time so hard to answer. 

## 1. The Effect of Releative Humidity on COVID-19 Cases in South Korea (Python)
[Relative Humidity on the Spread of COVID-19 Project](https://github.com/soneunii/relative-humidity-on-covid-19)


According to *University Hospitals*, https://tinyurl.com/9aw5jvr8 , UH pulmonologist David Rosenberg recommends
keeping the relative humidity levels in the 40 to 60 percent range to potentially reduce the possibility for
spreading the virus. The goal of this project is to see what factors of the weather contributes the most to
the relative humidity rate and whether the presented cases in South Korea follow Rosenberg’s theory.
DS4C, a Korean based data science group, structured this dataset based on the report materials of
KCDC and the local Korean government. This data can be found on
https://www.kaggle.com/kimjihoo/coronavirusdataset?select=Case.csv. There are two datasets used in
this project, one contains 13 columns describing personal information about each patient, the date when
the symptoms were shown, the date when the patient got tested positive for Covid19. The other dataset
contains 10 columns about weather information for each day, such as the temperature, wind speed, and
average relative humidity of the day from 2016/1/1 to 2020/6/28. 
  1) Using principal component analysis over the variables, visualized the cumulative explained variance ratio of both scaled and not scaled variables as more features were added into the pipelines 
  2) Visualized each variables' weights into predicting the average relative humidity, comparing both simple linear regression and regression with polynomial variables. 

## 2. GUIDE Regression Tree Analysis on Factors Affecting Probability on Dying from COVID-19 (GUIDE, R)
[GUIDE Regression Tree Analysis on COVID-19 Project](soneunii/GUIDE-regression-tree-analysis-covid19/README.md)


What kind of people are more suceptible to dying from COVID-19 when they get infected? With a dataset reported from 21 healthsystems with 145,944 subjects hospitalized with COVID-19 collected from February 1st, 2020 to January 31, 2022:
  1) Goal was to find which characteristic of someone hospitalized for COVID-19 is the most significant in affecting one's proability in dying from the disease. 
  2) Fitted a standard logistic model, GUIDE random forest, GUIDE logistic regression tree, and GUIDE tree to predict the probability of one dying from COVID-19, infer about th effects of the variables and the accuracy of the prediction models. 
  3) Found predicted values from using Rpart, Ctree, Cforest, and RandomForest to compare its performance with that of GUIDE tree, and GUIDE forest.

### GUIDE (Generalized, Unbiased, Interaction Detection and Estimation) 
GUIDE is an algorithm for constructing regression trees and forests with features such as having the ability to select unbiased varaibles either with or without missing data, handling missing values without having to require prior imputation, and being able to conduct regression trees with the options of using catagorical variables for either just splitting, fitting, or both in the models and more. 

It was interesting to compare the performances of running a regular logistic regression through R, computing a very known method of creating forests, Cforest, and comparing its performance with GUIDE's methods of predicting dependent variables. There's always a give-or-take situation with all of those regression models, hence the amount of different models and methods to predict existing in this world! At the end of the day, they are all numbers, and numbers can only do much for us, who interpret and analyze those numbers. By comparing performances through running time and plotting predicted values, I was able to see what to focus on, what I am willing to give up in return for a more significant factor that determines what a 'good' model is. 

  


