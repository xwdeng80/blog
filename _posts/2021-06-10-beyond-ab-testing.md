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

There are also other online experiments such as switchback experiment and sequanetial experiments.

*Switchback Experimentation*

Due to the limitations of A/B tests and the insufficiency of pre-post comparisons, the Dispatch team recently decided to switch to a new analytic framework for much of its experimentation — ‘switchback testing.’ Fun fact: switchback testing was originally employed in an agricultural context, specifically for cow lactation experiments. 

In switchback testing, the core concept is that we switch back and forth between control and treatment algorithms in a certain region at alternating time periods. For example, in the SOS pricing example, we switch back and forth every 30 minutes between having SOS pricing and not having SOS pricing. We then compare the customer experience and marketplace efficiency between the control time bucket and treatment time bucket metrics corresponding to the decisions made by the algorithm during the two periods.

# Summary
