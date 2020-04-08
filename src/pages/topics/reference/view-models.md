---
title: "View models"
sidebar: getting-started
permalink: reference-view-models.html
previous: reference-join-datasets
next:
---

Compare the accuracy of models generated from your feature selections.

## Classification models ##

Classification model results report whether the predicted values matched the actual values.

{% include diagram.html file="view-models-classification.png" name="view-models-regression-view" alt="Classification results" caption="Click to enlarge" %}

## Regression models ##

Regression models allow you to configure the acceptable error (distance from the actual value) in predictions. Distil then lists the correctly and incorrectly predicted values based on your selection.

{% include diagram.html file="view-models-regression.png" name="view-models-regression-view" alt="Regression results" caption="Click to enlarge" %}

## Forecast models ##

Forecast model results predict the future values of a timeseries.

{% include diagram.html file="view-models-forecasting.png" name="view-models-forecasting-view" alt="Forecasting results" caption="Click to enlarge" %}