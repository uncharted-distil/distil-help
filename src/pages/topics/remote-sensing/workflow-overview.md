---
title: "Remote sensing overview"
summary: Use Distil to train a classifier than can predict land use from satellite imagery.
sidebar: getting-started
permalink: remote-sensing-overview.html
previous:
next: remote-sensing-label-creation
---

In this workflow, you'll learn how to add labels to a Sentinel-2 satellite imagery dataset and train a classifier model to predict whether images match those labels. In this case, you'll be training a model to recognize imagery containing snow so you can later remove them from a model used to detect urban development.

The workflow has two main steps:

1. [Build a set of labels](remote-sensing-label-creation.html)
2. [Create candidate models](remote-sensing-create-models.html)
3. [Apply a model to a dataset](remote-sensing-apply-model.html)

{% include video.html src="vid/distil-locust-remote-sensing-vo.mp4" %}