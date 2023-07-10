---
layout: post
title:  "From Robust Parameter Design to AI Fairness"
date:   2021-07-08 10:45:00 +0200
permalink: RPD-AI-Fairness
tags: [Data Science]
categories: [data-science]
excerpt: "From RPD to AI Fairness"

---
# Introduction

Robust Parameter design is a well-known technqiue in qulaity control. 
By exploring the control-by-noise interaction, it provide the possiblilty of adjusting the setting of control variables to make the variation of response ($y$) less senstitive to the noise factors. 
Here Control variables are variables of which the experimenter has full control. Noise variables lie on the other side of the spectrum. 
While these variables may be easily controlled in an experimental setting, outside of the experimental world they are very hard to control.
It was introduced by Genichi Taguchi as a design-of-experiment approach to exploit the interaction between control and uncontrollable noise variables by finding the settings of the control factors that minimize response variation from uncontrollable factors.

While in the AI algorithm, the key is to make the preditive model based on common varaibles to be less affected (i.e., being fair) by some sensitive variables. It often focuses on constructing an optimal AI model subject to fairness constraints (a “constrained optimization problem”).  Commonly, constraints tend to be around sensitive varaible. 

# The Connection and Beyond

One can see that the concept of control-by-noise interaction, signal-to-noise ratio, and response surface methodology can be borrowed into the study of AI fairness, where the common varaibles are used to build the AI algorihtm, while we need to make the AI algorihtm robust, stable, and reliable with respect to sensitive varaibles. 

# Summary
We believe there are great potential to borrow strength from robust parameter design to enhance AI fairness. We would like to conclude the post with several remarks:

- Remark 1: How can the RPD be used for online experimentation, where the platform factor is of great interest.
- Remark 2: How can the RPD be used for computer experiments, where Gaussian process is commonly used but the control-to-noise
interactions is not explicitly included in the model.
- Remark 3: How can the RPD be used for AI fairness, where some demographic variables playing key roles to make model being fair.
- Remark 4: The idea of RPD can be considered towards the broad sense of the decision-integrated modeling and optimization.
