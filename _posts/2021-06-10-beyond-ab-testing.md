---
layout: post
title:  "Beyond A/B Testing"
date:   2021-06-10 16:45:00 +0200
permalink: online-AB-testing
tags: [Online Experimentation]
categories: [online-experiments]
excerpt: "Online Experiments Beyond A/B Testing."

---



# Introduction

Online Experimentation has been very pouplar with wide applications in various sectors. However, there is a gap between research and application needs on the design and analysis of online experiments. In this post, we would like to provide a better picture of the online experiments. 

# Perspectives

The conventional A/B testing conisdier the treatment and control (design A or design B) are randomly assign to experiment units (users). 
For example, a e-commerce company consider two promotion webpages to boost the click rates. 
In online experimentation, it is common for millions of users to arrive at the top homepage webpage, while only a small percentage of users reach the
bottom purchase webpage). Between the transition from the top page to the bottom page, users need to navigate through multiple pages where they can exit from the
shopping process.

However, there are some problems related to A/B testing. First, there is a high cost with the “bad” versions of the product since they will continue to be offered to the user until the end of the test even if their returns are not good. Second, there is also the risk of getting churned users, because those who received the “bad” version of the product during the whole test may have a poor experience with the product.

Alternatively, there are also other online experiments such as switchback experiment and sequanetial experiments.

- Switchback Experimentation

Due to the limitations of A/B tests and the insufficiency of pre-post comparisons, some researches consider to switch to a new analytic framework for much of its experimentation — ‘switchback testing.’ 
The switchback testing was originally used in an agriculture. In switchback testing, the core concept is that we switch back and forth between control and treatment algorithms in a certain region at alternating time periods. For example, in the SOS pricing example, we switch back and forth every 30 minutes between having SOS pricing and not having SOS pricing. We then compare the customer experience and marketplace efficiency between the control time bucket and treatment time bucket metrics corresponding to the decisions made by the algorithm during the two periods.

- Multi-Armed Bandits

Multi-Armed Bandits (MAB) is a simpler case of the reinforcement learning problem in which you have $k$ different options (or actions) $A_{1}, \ldots, A_{k} each associated with a real distribution 
$R_{1}, \ldots, R_{k}$ corresponding to the rewards. The $\mu_{1}, \ldots, \mu_{k}$ are the mean of these distributions, respectively. 
Therefor, the agent executes an action $A_{t}$ iteratively according to its policy and receives a numerical reward $r_{t}$ (sampled from the distribution $R_{t}$) associated with that action. 
The goal is to maximize the rewards received during the interactions, that is, find the action that has the highest expected reward. In other words, the agent needs to learn the reward distributions associated with each action in order to obtain the one with the highest expected return. 
A possible metric to assess agent learning in $T$ interactions is regret $\rho$, given by the expected difference between the sum of the reward associated with the optimal action and the sum of the collected rewards:

# Summary
We beleive that there are a lot of research opportunites in the online experiments. 

