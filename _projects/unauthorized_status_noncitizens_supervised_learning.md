---
title: 'Predicting Unauthorized Status Among the U.S. Noncitizen Population'
subtitle: 'Using Census Data and Supervised Learning Models'
date: 2020-05-04 00:00:00
description: This page previews my project using supervised learning on U.S. Census data to predict unauthorized status among the noncitizen population.
featured_image: '/images/noncitizens/populationbystatus.png'
---
<img src="/images/noncitizens/populationbystatus.png" width="800" height="800" align="center">


## Summary

Using the best performing features from a combination of predictors from the most influential models in research estimating the size of the unauthorized immigrant population in the United States, I compared the performance of more than several supervised learning models in predicting unauthorized status among noncitizens in the 2008 Survey on Income and Program Participation (SIPP). After extensive data wrangling and feature engineering, I used Naive Bayes, Support Vector Machines, K-Nearest Neighbors, Random Forest, and Gradient Boosted Classifiers to classify the target variable. As you can see in the figure above (or below), the target variable suffered from major imablance. To mitigate that, I upsampled the minority class. Also, For each model, I tuned the algorithm's hyperparameters with *Hyperopt*. While the results were respectable, there is room for improvement. __The project's Jupyter Notebook is [here](https://github.com/slackademic/Projects/blob/master/classifying_noncitizens_sipp2008.ipynb)__.

### Why Is This Work Important?
- Some of my work in the health care policy research and advocacy space would benefit from having the ability to filter out this population from measures of eligibility for health insurance programs in the United States.
- Estimating the unauthorized immigrant population is an important step in the process of calculating how many residents in the United States fall into the so-called health insurance "coverage gap." People who fall into this category are those who make too much money to qualify for Medicaid but do not make enough to qualify for government subsidized health insurance premiums on the health insurance exchanges.
- I am currently working on a project incorporating estimates of the coverage gap and I would like to be able to measure the unauthorized population in Florida's major metropolitan areas.


### The Data
- The SIPP is a national panel survey of approximately 50,000-60,000 households over a four-year period.
- The federal government uses it to track microeconomic trends and to analyze how government programs affect American households over time.
- In each wave, respondents are asked a core set of questions measuring socioeconomic status, demographics, and receipt of and usage of public benefits.
- Each wave also includes an additional set of questions on a specific topic. The second wave's supplemental questions focused on ethnicity and immigration.
- You may find the 2008 panel survey [here]((https://www.census.gov/programs-surveys/sipp/data/datasets.2008.html)).


### Visualizing the Data
- Here are some descriptive plots of the target variable and features used in the models.
- The data are unweighted, so the figures are only meant to convey the sample data, *not the population from which the sample was drawn.*

<div class="gallery" data-columns="2">
	<img src="/images/noncitizens/household_poverty.png">
	<img src="/images/noncitizens/hh_citizen_related.png">
	<img src="/images/noncitizens/female_hispanic_age.png">
	<img src="/images/noncitizens/education_residence.png">
	<img src="/images/noncitizens/insurance_bystatus.png">
	<img src="/images/noncitizens/industry_classification_bystatus.png">
	<img src="/images/noncitizens/regionbirth_bystatus.png">
	<img src="/images/noncitizens/english_bystatus.png">
</div>


### Model Performance Comparisons


| ML Classifier | Training Accuracy (%)| Testing Accuracy (%) | False Positives (%) | False Negatives (%) | Sensitivity (%) | Specificity (%) |    
|----------------------|---------------|------------------|-------|
| Naive Bayes (untuned) | 72 | 69 | 53 | 15 | 71 | 68 |
| KNN   | 83 | 69 | 54 | 23 | 40 | 81 |
| SVC | 89 | 71 | 53 | 27 | 18 | 92 |
| Random Forest  | 86 | 72 | 48 | 20 | 52 | 80 |
| Gradient Boosting | 87 | 72 | 47 | 23 | 36 | 87 |
