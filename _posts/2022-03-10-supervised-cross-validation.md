---
layout: post
title:  "Self-supervised cross validation: embracing data generation structure"
date:   2022-03-10 22:10:33 +0200
permalink: self-supervised-cross-validation
tags: [Active Learning, Deep Learning]
categories: [deep-learning]
excerpt: "Self-supervised cross validationg"

---
## Introduction

Modern statistics and machine learning typically involves large amounts of data coupled with computationally inten-
sive methods such as neural networks 1 and Gaussian processes.2 For many of these models, classical inference such as
hypothesis testing, is replaced by an emphasis on understanding generalized (out of sample) performance, as measured
by prediction accuracy. Rather than fitting models to all the data, one partitions the observations into training and hold-
out sets. Models are fit (parameters are estimated) using the training data set. Many models of different types are then
considered, and their prediction accuracy is assessed on the holdout set.

The allocation of data rows to the training and holdout partitions are often implemented using random sampling,
not taking into account the structure of the data. However, data often has a complex underlying structure matching the
problem at hand. Examples of structure in data include operational restrictions and time sequencing issues resulting from
the data generation process itself. In the literature, some resampling methods consider the data structure, to some degree.
For example, using the Euclidian distance between the samples, the Kennard-Stone algorithm 3 considers splitting the
data into the training and calibration sets based on the distance to the points already selected. Hedayat et al. 4 discuss
balanced resampling methods, with the exclusion of contiguous units. Other approaches for data partitioning, such as
leverage-based sampling 5 and venetian-blinds method 6 are based on the ordering of the samples and have been developed
under different contexts. However, these methods do not explicitly incorporate the data generation structure into the
modeling and data partition.


## Motivation and Key Method

To fill this gap, we focuse on the role of data structure in the partitioning of observational data into training and
hold-out datasets for assessing the fit of predictive models. We propose embracing the data generation structure to parti-
tion the data for validating predictive model. This is essential to the success of data science projects. To meet this challenge,
the framework of befitting cross validation (BCV) is developed here in connection to the Information Quality (InfoQ) per-
spective.

Clearly, a complex data structure increases the challenge of machine learning to be sensible and accurate. In particular,
the cross-validation approach, commonly used in machine learning, encounters the challenges of how to appropriately
partition data into the training dataset and the hold-out dataset in complex data structures. Conventional cross validation
applies a random partition of the data into training and hold-out datasets. As shown in Figure 2, such a random allo-
cation cross validation approach does not necessarily account for the data structure in the whole dataset. In such cases
the training dataset and the hold-out dataset do not have the same data structure as the whole data. Consequently, the
machine learning method could result in misleading performance.

To address this challenge, we propose a befitting cross-validation (BCV) embracing the data generation structure, as
illustrated in Table 1. BCV incorporates the data generation structure of the whole data into the partition of the training
data and hold-out data with the following three principles.

-BCV Principle 1: The formation of training and hold-out datasets should reflect the goal of the study.

-BCV Principle 2: The training dataset and the hold-out dataset should have the same data generation structure as the whole dataset.

-BCV Principle 3: The construction of the hold-out dataset should reflect the data generation structure needed for the predictive model.

## Summary

In the era of Data Sceince, cross validation is widely used. 
In this post, we address issues with hold out sets and cross validation in the context of data splitting. 36 We propose the
BCV method to handle such conditions and thereby provide for enhanced information quality in predictive analytics
modeling. BCV focuses on cross validation for predictive models, whose goal is prognostic with the InfoQ utility being
prediction accuracy. The proposed BCV key concepts and principles can be extended to bootstrapping, whose goal is
diagnostic. In this case the InfoQ utility is error rate and estimates of variability.
The proposed method deals with a general methodological issue requiring an information quality assessment, so that the analytics associated with data generates information quality. 
From such an perspective, one can derive proper holdout and cross validation strategies that enable proper generalization of predictive analytic models. BCV extensions are also possible to
situations where the data generation process can be learned from the data itself.
