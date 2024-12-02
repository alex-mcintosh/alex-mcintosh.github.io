---
layout: page
title: Applying supervised learning to predict student dropout rate
description: 
img: assets/img/student1.jpg
importance: 1
category: work
related_publications: false
---

<div class="row justify-content-sm-center">
  <div class="col-sm-8 mt-3 mt-md-0">
     {% include figure.liquid loading="eager" path="assets/img/student1.jpg" title="example image" class="img-fluid rounded z-depth-1" %}
    <figcaption style="font-size: 10px;" class="custom-caption mt-2">Unsplash</figcaption>
  </div>      
</div>

## Introduction
The Study Group provides online courses, tutoring, and consulting services, collaborating with universities to support and prepare international students. A key challenge is high dropout rates, which can harm revenue, reputation, and student satisfaction. This project aimed to predict student dropouts using supervised learning models such as XGBoost and neural networks.


<div align="center">
  <a href="https://github.com/alex-mcintosh/Supervised-Learning-for-Student-  Dropout/blob/main/Applying_supervised_learning_to_predict_student_dropout_rate.ipynb">
    <img alt="Static Badge" src="https://img.shields.io/badge/GitHub%20Notebook-black?style=plastic&logo=github" height="35">
  </a>
</div>


## Data Overview
The dataset included 36 features across 25,059 records and was divided into two subsets: minimal and extended datasets.

*	**Minimal Dataset**: Focused on core features like student demographics, course details, and unauthorised absences.
*	**Extended Dataset**: Additional features such as contact hours and attendance percentage were included.
  
The target variable, _CompletedCourse_, was highly imbalanced, with more students completing courses than dropping out. Missing data primarily affected the dropout class, especially in the _CreditWeightedAverage_ feature. To address this, missing values were imputed using the median of the dropout class instead of removing affected records, preserving the class balance.
Other preprocessing steps included converting Date of Birth to Age, one-hot encoding categorical features, and reducing feature dimensions for some variables. The exploratory analysis highlighted significant patterns in features like _CreditWeightedAverage_, _AttendancePercentage_, and _UnauthorisedAbsenceCount_, which were strongly associated with dropout behaviour.

## XGBoost Model for Predicting Student Dropouts
Initial modelling used the minimal dataset and an XGBoost model with default settings, followed by hyperparameter tuning. Performance was evaluated using the F1 score and AUC to address class imbalance.
* 	**Default Model**: Delivered modest results.
* 	**Post-Tuning**: Results were mixed, with AUC improving but declines in accuracy and F1 score.
  
Adding features from the extended dataset significantly improved the model, as they provided critical predictive information. Feature importance analysis showed _CreditWeightedAverage_ as the most influential variable, followed by categorical features like _CentreName_, which suggested some collinearity with _ProgressionUniversity_.

## Neural Network Models
Neural networks were tested with similar datasets and optimization strategies.

*	Performance was slightly lower overall compared to XGBoost.
*	Neural networks achieved better recall, which is critical for identifying potential dropouts early.
  
Using the extended dataset improved neural network performance, particularly due to features like _AttendancePercentage_ and _ContactHours_.

## Key Findings and Model Comparisons
###	XGBoost vs. Neural Networks:
*	XGBoost consistently outperformed neural networks, especially in precision and F1 score.
*	Neural networks excelled in recall, which is valuable for early dropout detection.
*	Tuning showed mixed results, with marginal AUC improvements but trade-offs in recall and precision.
*	XGBoost’s efficiency and interpretability make it the preferred choice.
  
###	Feature Importance:
*	_CreditWeightedAverage_ was the most impactful predictor.
*	Relationships between features like _CentreName_ and _ProgressionUniversity_ merit further exploration to reduce model complexity.

## Recommendations and Next Steps
1.	**Investigate Missing Data**: Explore the relationship between missing _CreditWeightedAverage_ values and dropout behaviour for deeper insights.
2.	**Expand Feature Usage**: Assess the full dataset of 35 features for increased predictive potential.
3.	**Feature Engineering**: Refine features and explore overlaps (e.g., _CentreName_ and _ProgressionUniversity_) to improve efficiency and accuracy.
4.	**Regularisation**: Introduce regularisation techniques to reduce overfitting and enhance model generalisability.

## Conclusion
XGBoost proved the most effective for predicting student dropouts, offering a balance between performance and usability. The best model allowed an AUC of 0.995, F1 score of 0.93 and a recall of 0.91. However, further feature engineering and modelling refinements could enhance prediction accuracy and model robustness.

