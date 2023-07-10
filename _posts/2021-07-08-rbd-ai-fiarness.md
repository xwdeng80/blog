---
layout: post
title:  "From Robust Parameter Design to AI Fairness"
date:   2021-07-08 10:45:00 +0200
permalink: RPD-AI-Fairness
tags: [Data Science]
categories: [data-science]
excerpt: "From RPD to AI Fairness"

---
{% include katex.html %}
# Introduction

Robust Parameter design is a well-known technqiue in qulaity control. 
By exploring the control-by-noise interaction, it provide the possiblilty of adjusting the setting of control variables to make the variation of response ($y$) less senstitive to the noise factors. 
Here Control variables are variables of which the experimenter has full control. Noise variables lie on the other side of the spectrum. 
While these variables may be easily controlled in an experimental setting, outside of the experimental world they are very hard to control.
It was introduced by Genichi Taguchi as a design-of-experiment approach to exploit the interaction between control and uncontrollable noise variables by finding the settings of the control factors that minimize response variation from uncontrollable factors.

While in the AI algorithm, the key is to make the preditive model based on common varaibles to be less affected (i.e., being fair) by some sensitive variables. It often focuses on constructing an optimal AI model subject to fairness constraints (a “constrained optimization problem”).  Commonly, constraints tend to be around sensitive varaible. 

# The Connection and Beyond

One can see that 






# Connection and Beyond

# Summary
