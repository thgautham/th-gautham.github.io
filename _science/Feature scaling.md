---
title: "Feature Scaling"

---
One of the most important transformations we need top apply to the data is feature scaling. With few exceptions,
machine learning algorithms do no perform well when the input numerical attributes have different scales.

There are two common ways to get all attributes to have the same scale:
- min-max scaling
- standardization

Min-max scaling (also called as normalization) is the simplest: values are shifted and rescaled so that they
end up randing from 0 to 1. We can do this byu subtracting the min value and dividing by the max minus the min value.
Scikit-learn provides a transformer called MinMaxScaler for this. It also has a feature_range hyperparameter that let's
you change the range if we don't want it from 0 -1.

Standardization is different: it subtracts the mean value(so standardized values always have a zero mean), and then
divides by the standard deviation so that the resulting distribution has unit variance.UNlike min-max scaling, standardization
does not bound values to a specific range, which is a problem for some algorithms (e.g., neural networks expect an input value ranging from 0 to 1).
Scikit-Learn provides a transformer called StandardScaler for standardization.