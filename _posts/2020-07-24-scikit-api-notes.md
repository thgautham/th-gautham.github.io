---
title: "Scikit-Learn's Design"
date: 2020-07-24
tags: [sci-kit learn, machine learning, api]
toc: true
toc_sticky: true
header:
  image: "/images/mountain-image-3.jpg"
  caption: "Photo credit: [**Unsplash.com**](https://unsplash.com)"
excerpt: "Sci-kit Learn's API and it's main design principles."
---
My notes on the Sci-kit Learn's API. FYI.

Consistency:
    - All objects share a consistent and a simple interface.

   Estimators:
    Any object that can estimate some paramters based on a dataset is called an estimator.
    (e.g., an imputer is an estimator). The estimation itself is peformed by the fit() method, and
    it takes only a datset as a paramter. Any other paramter needed to guide the estimation process is considered
    a hyperparamter and it must be set as an instance variable.

   Transformers:
    Some estimators can also transfor a dataset; these are called transformers. The transformation is performed
    by the transform() method with the dataset to transform as a parameter. It returns the transformed dataset.
    This transformation generally relies on the learned parameters, as is the case for an imputer. All transformers
    also have a convenience method called fit_transform() that is equivalent to calling fit() and then transform().

   Predictors:
    Some estimators, given a dataset, are capable of making predictions; they are called predictors.
    For example, the LinearRegression model is a predictor. A predictor has a predict() method that
    takes a dataset of new instances and returns a dataset of corresponding predictions. It also
    has a score() method that measures the quality fo the predictions, given a test set.

Inspection:
    All the estimators hyperparamaters are accessible via public instance variables (e.g., imputer.strategy), and
    all the estimator's learned paramters are accessible via public instance variables with an underscore suffic.

Nonproliferation of classes:
    Datasets are represented as NumPy arrays or SciPy sparse matrices, instead of homemade classes.

Composition:
    Existing building blocks are reused as much as possible. For example, it is easy to craete a Piepline estimator
    from an arbitrary sequence of transformers followed by a final estimator.

Sensible defaults:
    Scikit-Learn provides reasonable default values for most parameters, making it easy to quickly create a
    baseline working system.


