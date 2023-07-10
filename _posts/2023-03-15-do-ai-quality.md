---
layout: post
title:  "Do-AIQ: A DoE Approach to AI Quality Assurance"
date:   2023-03-15 10:45:00 +0200
permalink: do-ai-quality
tags: [Data Science]
categories: [data-science]
excerpt: "A DoE Approach to AI Quality Assurance"

---
{% include katex.html %}

# Introduction

Great advancement has been made by machine learning algorithms on various scientific and engineering areas. However, the safety and quality assurance of these algorithms are still a significant concern. For example, a small malicious perturbation on data can deceive AI algorithms and result in catastrophe when applying them to real-life practices (Chen et al., 2020). Therefore, systematically evaluating the quality of AI algorithms is of great importance for the assurance of using the algorithms in practice. In this work, we present a principled Do-AIQ framework of using a Design-of- experiment approach to systematically evaluate the AI Quality. The proposed framework can set an exemplar for AI algorithm practitioners to enhance the AI assurance of robustness, reproducibility, and transparency.

# Motivation
We focus on investigating the quality of the AI mislabel detection (MLD) algorithm against data poisoning. In classification tasks, mislabeling the responses can disturb model training and undermine the performance of algorithms by simply assigning wrong labels to training data. Various MLD algorithms have been developed in the literature. For example, Pulastya et al. (2021) proposed a structure including a variational Auto-Encoder and a simple classifier to construct the so-called mislabeling score to distinguish the mislabeled data from normal data. It is known that the performance of MLD algorithms can be affected by two major groups of factors, hyperparameters in the algorithm and data quality factors, including the number of mislabeled observations in training data, class imbalance, and data types. However, no comprehensive evaluation exists to assess the assurance (such as robustness, reproducibility, and transparency) of these methods. Besides, the validity of the evaluation metrics and processes is not verified. The proposed Do-AIQ approach will fill these gaps and shed a light on the assessment of MLD AI algorithms and on understanding their limitations.

# Methods
First, we propose a principled frame- work of using a design-of-experimental approach to systematically evaluate the quality of AI algorithms against data poisoning. The developed framework is not restricted to the MLD algorithm, but can be used for evaluating other AI algorithms, especially when the data quality and algorithm structure (i.e., hyper-parameters) are intertwined. Second, to systematically investigate how the data quality affects the quality of AI algorithm when the internal structure of AI algorithms varies, we propose an effective design criterion with an efficient construction algorithm to obtain a space-filling design in a high-dimensional constraint space to investigate the quality of MLD algorithms in terms of detection accuracy and prediction accuracy. Specifically, we consider the design space consisting of three continuous factors without constraint, ten continuous factors of class proportions with linear constraint, and one binary factor for “data type”. The construction algorithm is efficient by leveraging the simplicity of coordinate descent in discrete optimization and constraint continuous optimization. Third, due to the complexity of design criterion and design space, an initial design is crucial to enable the design construction algorithm. Our method of initial design based on algebraic construction is very fast in computation with flexible run sizes. Fourth, we adopt an additive Gaussian process model as a surrogate model to emulate the quality of AI algorithms as a function of data quality factors and AI algorithm’s hyper-parameters. The use of an additive Gaussian process can accommodate both continuous and categorical factors of interest, providing accurate prediction and uncertainty quantification of the quality of the algorithm.


# Summary

we establish a Do-AIQ framework to comprehensively investigate how data quality factors (e.g., data type, percentage of mislabeled data, class imbalance in training data) and hyperparameters of algorithms affect the quality assurance of the AI algorithms. 

There could be several limitations of the current work. First, we choose a mislabeled data detection algorithm to describe the proposed framework. However, the Do-AIQ is not limited to this particular MLD algorithm. 
It can be extended to other AI algorithms whose quality assurance is affected by various data quality factors and their internal structure. Second, the number of classes in this study is around ten, not as large as hundreds in some
benchmark data. For data with large classes such as the CIFAR100 dataset with 100 classes, the proposed design construct algorithm may encounter certain computational difficulties.
