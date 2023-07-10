---
layout: post
title:  "Robusness of AI Algorithm"
date:   2021-05-31 14:10:33 +0200
permalink: robustness_of_ai_algorithm
excerpt: Discussion on the robustness of AI algorithms

---

<!--
![](https://raw.githubusercontent.com/jacobgil/dlib_facedetector_pytorch/master/positive_images/13_4.jpg)
-->

# Introduction

Machine learning (ML) and deep learning (DL) algorithms are widely used in many artificial
intelligence (AI) applications such as computer vision, autonomous
driving, and medical diagnostics. There is a growing in-
terest in investigating the robustness of AI algorithms, as it is highly related to the safety of AI systems (Amodei et al.,
2016). The training data can be noisy and imbalanced, resulting in performance degradation
of the AI algorithm. Moreover, some AI algorithms could be vulnerable to
data poisoning attacks, where adversarial insiders may change the data structures in certain
scenarios. Therefore, there is an emerging need to understand how the data quality affects
the quality assurance of the AI algorithms. Such a comprehensive understanding will pave
a foundation for developing solid solutions to mitigate and remedy data quality problems in
AI algorithms.

# Key Method

In this post, we focus on the robustness of AI classification algorithms in terms of how
the performance of the algorithm, such as the classification accuracy, may change when the
training and test datasets contain differences in class proportions. The robustness of AI algorithms relies heavily on how the algorithm is trained and the evaluation
of the algorithm relies heavily on the test dataset. We focus on investigating the robustness
of AI classification algorithms in terms of the classification accuracy based on the area under
the curve (AUC). The proposed framework is not restricted to using AUC for examining
the robustness, and can be extended to study the robustness for AI algorithms beyond
classification.

We use designed experiments to systematically
investigate the robustness of classification algorithms with respect to: (1) the class label
imbalance in the training data; and (2) the distribution change between training and test
data regarding the proportions of class labels. In particular, our key idea is to use the
mixture experimental design  for the proportions of class labels in the training
data, such that the robustness of the AI classification algorithms can be investigated in a
systematic manner. Here the robustness of a classification algorithm is characterized by the
mean and standard deviation of the areas under the receiver operating characteristic curves
(AUC) for each class label. 

We also study a wide range of other factors that can affect the robustness, including the distributional changes between
the training data and the test data, different classification algorithms, and datasets from
different applications. The convolutional neural network (CNN) and XGBoost
(Chen et al., 2015) are adopted as two representative AI classification algorithms. Based on
the classification performance results collected from the designed mixture experiments, we
build a statistical surrogate model for the classification accuracy (i.e., AUC) as a function
of the mixture proportions, and reveal some interesting findings on the robustness of AI
classification algorithms. The resultant model estimation, inference, and prediction provide
a set of useful tools to quantify the importance of class proportion, visualize the effect of class
imbalance, and to identify conditions under which the algorithms tend to be robust, which
can not be easily achieved by existing studies on class imbalance. Note that the proposed
framework can be extended to include more factors for investigating the robustness of the
AI algorithms, and can also be used to study other characteristics of the AI algorithms, such
as the transparency of the AI systems.

# Summary

In this post, we consider an experimental design framework to systematically investigate
how the data quality, such as imbalance among class labels, and distribution shift between
training data and test data, affects the quality assurance of the AI classification algorithms.

It is to elaborate how the experimental design thinking is used to systematically investigate
the performance characteristics of AI algorithms, which is called AI assurance in the general
media. The AI assurance is all about ensuring that the AI is going to operate in a proper
and risk-controllable manner over time, which broadly includes robustness and reliability,
privacy and security, fairness and bias, transparency, and reproducibility. 

