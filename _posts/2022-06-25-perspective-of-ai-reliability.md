---
layout: post
title:  "Statistical Perspectives on AI Reliability"
date:   2022-06-25 14:10:33 +0200
permalink: robustness_of_ai_algorithm
excerpt: Statistical Perspectives on AI Reliability

---


## Introduction

Artificial intelligence (AI) systems have become common in many areas, from research to
practice, and even in everyday life. However, AI technologies are still in their developing
stages and there are many issues that need to be addressed. Those issues include robustness,
trustworthiness, safety, and reliability. In this paper, we focus on AI reliability, which is an
important dimension, because the reliability of AI systems needs to be shown so that AI
systems can be used with confidence. Different from other considerations, the reliability of
AI systems focuses on the time dimension. That is, the system can perform its designed
functionality for the intended period of time.

The main goal of this post is to provide statistical perspectives on the reliability of
AI systems. In particular, we introduce a so-called “SMART” statistical framework for AI
reliability research, including Structure of the system, Metrics of reliability, Analysis of failure
causes, Reliability assessment, and Test planning. We briefly review the traditional methods
in reliability data analysis and software reliability, and discuss how those existing methods
can be transformed for reliability modeling and assessment of AI systems. We also review
recent developments in modeling and analysis of AI reliability, and outline statistical research
challenges in the area, especially for statisticians.

We explore some research opportunities in AI reliability, including out-of-distribution de-
tection, the effect of the training set, adversarial attacks, model accuracy, and uncertainty
quantification, and discuss how those topics can be related to AI reliability. We provide some
examples to illustrate those research opportunities. As data are essential for reliability assess-
ment, we also discuss data collection and test planning for AI reliability assessment and how
to improve system designs for higher AI reliability.

## The Importance of AI Reliability

For any system, reliability is often of interest because failure events can lead to safety concerns.
Failures of AI systems can lead to economic loss and even, in some extreme cases, lead to loss
of life. For example, a failure in the autopilot system of an autonomous car can lead to an
accident with loss of life. Thus, reliability is critical, especially for autonomous systems.

We introduce the “SMART” framework for AI reliability study, which contains five components. Here, the acronym “SMART” comes from the first letter of the five
components below.

• Structure of the system: Understanding the system structure is a fundamental step in the AI reliability study.

• Metrics of reliability: Appropriate metrics need to be defined for AI reliability so that data can be collected over those metrics.

• Analysis of failure causes: Conducting failure analysis to understand how the system fails (i.e., failure modes) and what factors affect the reliability.

• Reliability assessments: Reliability assessments of AI systems include reliability modeling, estimation, and prediction.

• Test planning: Test planning methods are needed for efficient reliability data collection.

The ultimate goal of statistical reliability analysis is to improve designs for reliable AI systems.

## Summary

In this post, e provide statistical perspectives on the reliability analysis of AI systems.
The objective of the paper is to provide some general discussion with illustrations on several
concrete problems, while we are not trying to be exhaustive in literature review because the
AI literature is vast and involves many areas.

One challenge is the limited public availability in reliability data from AI systems, which
is common for all systems and products because reliability data are usually proprietary and
sensitive. Also, the collection of field test data is usually costly and time consuming. The
publicly available California DMV database for AV test is one exception. For the reliability
data of AI algorithms, as mentioned in Section 5.1, one can collect using in-house computing
power. However, it is useful to build data repository for AI reliability datasets. As for modeling
methods, Bayesian methods have been widely used in reliability (e.g., Hamada et al. 2008).
Although we did not discuss Bayesian reliability in this paper, Bayesian methods can be an
area that worth exploring for AI reliability modeling.
