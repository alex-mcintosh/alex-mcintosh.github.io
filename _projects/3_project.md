---
layout: distill
title: Applying NLP for topic modelling
description: 
img: assets/img/NLP.jpg
tags: distill formatting
category: work
related_publications: false
---

<div class="row">
  <div class="col-12">
     {% include figure.liquid 
        loading="eager" 
        path="assets/img/NLP.jpg" 
        title="example image" 
        class="img-fluid w-100 rounded z-depth-1"
        caption = "Photo by <a href="https://unsplash.com/@julesea?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">jules a.</a> on <a href="https://unsplash.com/photos/grayscale-photography-of-brother-typewriter-NvFkYV2ngOk?utm_content=creditCopyText&utm_medium=referral&utm_source=unsplash">Unsplash</a>"
     %}
  </div>      
</div>


## Introduction
This project showcases the application of Natural Language Processing (NLP) techniques to analyse customer reviews, uncover actionable insights, and propose data-driven solutions for improving customer experiences. The work focuses on leveraging real-world data from PureGym, a leading fitness operator, to identify key customer satisfaction and dissatisfaction drivers.



<div align="center">
  <a href="https://github.com/alex-mcintosh/Applying-NLP-for-topic-modelling/blob/main/Applying_NLP_for_topic_modelling.ipynb">
    <img alt="Static Badge" src="https://img.shields.io/badge/GitHub%20Notebook-black?style=plastic&logo=github" height="35">
  </a>
</div>



## Project Overview
The project utilised a dataset comprising 23,520 Google reviews and 16,673 Trustpilot reviews. The analysis aimed to pinpoint themes in negative feedback to guide operational improvements. The work involved extensive preprocessing, multiple topic modelling techniques, and sentiment analysis to derive actionable insights from the data.

## Key Steps Undertaken
1.	**Data Preparation:**
    *	Cleaning and preprocessing the dataset to ensure accurate and efficient analysis.
    *	Generating initial visualisations like word clouds and bar plots to highlight commonly discussed terms.
3.	**Topic Modelling:**
    *	BERTopic was employed to identify and contextualise themes in reviews rated below three stars. Recurring issues included staff interactions, cleanliness, parking, and shower facilities. Location-specific patterns were explored by isolating data from gyms with the most negative feedback.
3.	**Latent Dirichlet Allocation (LDA)** added another layer of analysis, revealing new themes like lockers and email communication. While LDA provided quantitative topic ranking, its interpretability was somewhat limited due to high-frequency and ambiguous words appearing.
4.	**Sentiment and Emotion Analysis:**
    *	Leveraging a BERT-based emotion model, reviews with strong emotional content (e.g., anger) were analysed. This refined dataset uncovered issues like cold showers, restricted opening hours, and further details about staff concerns.
5.	**Language Model Integration:**
    *	The Phi 3.5 language model analysed a subset of reviews for subtle insights such as overcrowding and inappropriate behaviour. While this added depth, scalability limitations required combining this method with other approaches.

## Results and Insights
Across all analyses, several recurring themes emerged, highlighting customer priorities:

 *	**Staff Interactions:** Concerns about staff behaviour were a dominant theme, underscoring the importance of employee training.    
 *	**Facilities and Maintenance:** Issues related to equipment quality, cleanliness, and temperature control were prominent, emphasising the need for consistent upkeep.
 *	**Parking and Accessibility:** Parking-related complaints, particularly about fines, were frequently mentioned.
 *	**Showers and Water Facilities:** Poor shower conditions and inadequate water amenities were highlighted concerns.
 *	**Scheduling and Availability:** Topics such as overcrowding and classes highlighted the need for better scheduling and resource allocation.

Although topics like membership fees and pricing surfaced, they were not as frequently emphasised as concerns focussed on the customer experience at the gyms. Further work should focus on the following areas:
 *	**Quantifying Topic Impact:** Prioritise issues based on their potential to enhance overall customer satisfaction. This should be balanced against the cost of implementation.
 *	**Identification of Location-Specific Issues:** Many issues (poor showers, insufficient parking, etc.) may relate to specific locations. This should be investigated further. Topics such as overcrowding and equipment may also relate to particular gyms. However, they could still benefit from blanket approaches such as preventative maintenance regimes and promotional campaigns to get people to use gyms off-peak.


