---
layout: post
title:  "Dropout Buyers in Large-scale Online Experimentation"
date:   2022-08-28 16:45:00 +0200
permalink: onlinedesign
tags: [Online Experimentation]
categories: [online-experiments]
excerpt: "Large-scale Online Experimentation"

---
# Introduction

Online experimentation has been playing a key role in data-driven decision making in the IT
industry including Microsoft, Linkedin, Netflix, Uber, eBay, and many others. 
Generally, online controlled experimentation, also known as A/B
testing, is conducted for a pre-determined amount of time to compare the difference in metrics
between the treatment group and the control group where users are randomly assigned to.
Prior to experimentation, a set of high-quality metrics are determined to assess the effects of
new features in the treatment group. The collected metric results can provide strong evidence
to support hypotheses and hence accelerate the decision-making process. However, incomplete metrics are
frequently occurred in the online experimentation, making the available data to be much fewer than the planned A/B testing. 

# Motivation
In this post, our focus is on the analysis of metrics that have incomplete measurements at the end of data collection in experiments.
With incomplete metric measurements, the inference of the difference in metrics between the treatment and the control in experiments is at the risk of being inaccurate. To analyze experiments with
missing metric values, a naive approach is to disregard users with incomplete outcomes. This approach assumes that the missingness is completely at random and that the fully observed
users are representative of the entire population. Such an approach will reduce the total number of users in the study, leading to a decrease in the experiment power. The power
decrease is substantial especially when the proportion of missingness is high.

# Methodology
We develop a clustering-based imputation for dropout buyers in large-scale online experimentation.
That is, we propose a clustering-based imputation method using k-nearest neighbors (kNN) for the analysis of online controlled experimentation in the presence
of incomplete metrics. The key idea of the proposed method is to identify and impute incomplete metrics with users’ neighbors by incorporating the structure information of data
from online experimentation. Specifically, the proposed method consists of two steps. The first step is to partition the data set into clusters after the stratification of experiment-specific
features, including the treatment assignment and the buyers’ characteristics. In the second step, we perform the kNN-based imputation. Moreover, we divide users with missing outcomes
into two categories: visitors and dropout buyers, such that the information of dropout buyers can be better utilized. Note that our framework assumes that the treatment assignment and
user covariates are fully observed, whereas only the outcome at the bottom of the funnel has missing values. The proposed method has three key advantages. First, the proposed
method uses the informative covariates during users’ journeys in the shopping funnel to impute incomplete metrics. Specifically, our method evaluates the heterogeneous impact from
different user segments on missing rates in metrics. Second, the imputed values from our method are intuitive to understand. Lastly, our method employs stratification and clustering
to alleviate the computation issues for large-scale data in online experimentation.
 
# Discussion
Metrics provide strong evidence to support hypotheses in online experimentation and hence
reduce debates in the decision-making process. This paper introduces the concept of dropout
buyers and classifies users with incomplete metric values into two categories: visitors and
dropout buyers. For the analysis of incomplete metrics, we propose a cluster-based k-nearest
neighbors-based imputation method. The proposed imputation method considers both the
experiment-specific features and users’ activities along their shopping paths. The proposed
method incorporates uncertainty among missing values in the outcome metrics using the
k-nearest neighbors method. To facilitate efficient imputation in large-scale data sets in
online experimentation, the proposed method employs a combination of stratification and
clustering. The stratification approach divides the entire large-scale data set into small
subsets to improve computation efficiency in the clustering step. The clustering approach
identifies inherent structure patterns to improve the performance of the k-nearest neighbors
method within each cluster.
