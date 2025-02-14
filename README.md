# Predictors of Vehicle Crash Injury
This is the fourth of a series of three projects completed for my Applied Econometrics course at UCLA's Master of Quantitative Economics. The objective is to be able to predict whether a vehicle crash will result in injury for any of the parties involved. To achieve this, we test various multinomial probit and logit models.

## 1. Introduction
In this project, we will analyze the `Kaggle Crash Dataset (2016-2023)`, which provides detailed records of vehicle crash incidents over 8 years. The dataset aggregates information from multiple open-source crash datasets.

*Link: https://www.kaggle.com/datasets/trsaivarun/crash-dataset-2016-2023?resource=download*

The goal is to answer the following question: **What are the significant factors that determine whether a vehicle crash leads to an injury?**

By employing qualitative dependent variable models, we will explore how various features (e.g., weather, road conditions, vehicle details, and driver behavior) contribute to crash severity.

## Dataset Overview
- Period: 2016 to 2023
- Content: Detailed records of vehicle crash incidents, including categorical and numerical attributes.
- Purpose: Designed for machine learning practice and accident pattern analysis.

## Results:
- The model consistently shows moderate-to-high **NPV**, making it useful for ruling out injuries.  
- **PPV** remains low across all scenarios, meaning positive predictions for injury are rarely reliable.  
- **Sensitivity** and **Specificity** vary widely, suggesting the model’s performance heavily depends on the scenario.  
- Despite some bright spots (like good specificity in the substance abuse scenario or decent sensitivity in the high-speed or older-vehicle conditions), the model struggles to balance both detecting injuries and avoiding false alarms.

- Possible factors that may have contributed to the model's low reliability include:
    - **Data Reduction:** Heavy filtering and feature removal likely discarded valuable predictors and crash details.  
    - **Imbalanced Target:** The rare occurrence of injuries biased the model toward predicting “no injury.”  
    - **Coarse Feature Encoding:** Binary conversions of complex categories stripped away potentially important subtleties.  
    - **Weak Predictors:** Chosen variables explained little variance; some were statistically insignificant.  
    - **Confounding Factors:** Unexpected negative relationships (i.e., substance abuse) suggest missing variables or confounders.  
    - **Limited Modeling Complexity:** Minimal feature engineering, no interaction terms, and reliance on simple linear/logistic methods.
