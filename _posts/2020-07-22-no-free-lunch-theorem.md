---
title: "No Free Lunch Theorem"
date: 2020-07-01
tags: [model, no free lunch, basic]
header: 
    image: "/images/mountain-image-3"
    caption: "Photo credits: *Unsplash.com*"[https://unsplash.com/]
excerpt: Quick read to help frame the machine learning modelling problem.
---
## No Free Lunch Theorem

A model is a simplified version of theobservations. The simplifications are meant to discard the superfluous details that are unlikely to generalize to new instances. To decide what data to discard and what data to keep, we must make assumptions. For example, a linear model makes the assumption that the data is fundamentally linear and that the distance between the instances and straight line is just noise, which can safely be ignored.

There are numerous papers which demonstrate that if we make absolutely no assumption about the data, then there is no reason to perefer one model over any other. This is called the *No Free Lunch (NFL)* therorem.For some datasets the best model is a linear model, while for other datasets it is a neural network. There is no model that is guaranteed to work better (hence the name of the theorem). 

The only way to know for sure which model is best to evaluate them all. Since, this is not possible, in practice you make some reasonable assumptions about the data and evaluate only a few reasonable models. For example, for simple tasks we may evauate linear models with various levels of regularization, and for a complex problem we may evaluate various neural networks.
