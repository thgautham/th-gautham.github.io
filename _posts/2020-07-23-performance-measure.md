---
title: "Performance measure"
date: 2020-07-22
tags: [data wrangling, data science, messy data]
toc: true
toc_sticky: true
header:
  image: "/images/mountain-image-3.jpg"
  caption: "Photo credit: [**Unsplash.com**](https://unsplash.com)"
excerpt: "A parameter that gives an estimate of the error in the predictions."
---

A typical performance measure for regression problems is the Root Mean Square Error (RMSE).
There is also Mean absolute error (MAE).

Both the RMSE and MAE are ways to measure between the two vectors:
the vector of predictions and the vector of target variables. Various distance measures
or norms, are possible:
- Computing the root of a sum of squares (RMSE) corresponds the Euclidean norm.
- Computing the sum of absolute(MAE) corresponds to the Manhattan norm.

The higher the norm index, the more it focuses on large values and neglects small ones.
This is why the RMSE is more sensitive to outliers than the MAE. But when outliers are
exponentially rare, the RMSE performs very well and is generally preferred.