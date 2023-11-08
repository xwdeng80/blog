---
layout: post
title:  "Data Distillation from An Experimental Design Perspective"
date:   2023-11-08 10:55:00 +0200
permalink: DD-stat-DoE
tags: [Data Science]
categories: [data-science]
excerpt: "Data Distillation and DoE"

---
{% include katex.html %}

## What is Data Distillation.

Dataset distillation is a process of selecting a subset of data samples containing most important and representative characteristics of the original dataset. 

A key objective of data distillation is to construct a more compact and manageable version of the dataset that contain key characteristics for training machine learning models.


## The Value of Data Distillation

Save computation, maintain performance: the computational cost for training machine learning models can be reduced while maintaining or even improving performance.
It is valuable in resource-constrained environments for handling large-scale datasets or when faster iterations are needed.


## Key Steps in Data Distillation

 -- Sample Selection: Select a subset of samples that represent the original dataset. Techniques include instance selection, prototype selection, or representative sample selection. These techniques aim to choose samples that capture the diversity, representativeness, and relevance of the original data.


 -- Selection Criteria: The selection of samples for the distilled dataset is guided by specific criteria. The diversity criteria aim to ensure that the selected samples cover different regions of the data space. Representativeness criteria ensure that the selected samples reflect the distribution of the original dataset. 
Relevance criteria focus on selecting samples that are relevant to the problem at hand.

 
## Connection with Experimental Design


## Summary

