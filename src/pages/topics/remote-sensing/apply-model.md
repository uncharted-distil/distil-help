---
title: "Remote sensing - Apply model"
sidebar: getting-started
permalink: remote-sensing-apply-model.html
previous: remote-sensing-create-models
next:
---

Once you are satisfied with the accuracy of your model, you can save it and then apply it to the full dataset you started with.

## Apply a model to input data ##

To save and apply your candidate model:

1. Click <span class="fa fa-save"></span> **Save Model**.
   {% include image.html file="remote-sensing/save-model.png" alt="Save your model so you can apply it to the full dataset" %}
2. Enter a unique **Model Name** and click **OK**.
3. Click **Apply Model**.
4. Use the **Import dataset** dropdown to specify that you want to *Select Existing Dataset*.
5. Choose the original dataset (*sentinel-sample*) from the **Choose an existing dataset** dropdown.
   {% include image.html file="remote-sensing/apply-model.png" alt="Apply your saved model back to the full dataset" %}
6. Click **Apply Model to Input Data**.

The results of the model are displayed in the same format you saw when you created the model, but this time with only the positive/negative predictions and associated confidence scores and no ground truth data with which to compare them.

{% include image.html file="remote-sensing/model-predictions.jpg" alt="Review the predictions made by your model" %}

## Save the model predictions ##

If you are satisfied with the results, you can either create a new dataset with the predicted labels as a new feature or export the predictions for use in other applications.

To create a new dataset:

1. Click **Create Dataset**.
2. Enter a unique **Dataset Name**.
3. To save any features that weren't included in the training of your model, click **Include data not used in model**.
4. Click **OK**.

   {% include tip.html content="At this point, you have a new version of your original dataset with a snow label (positive/negative) applied to every satellite image tile. You can use this version of the dataset to create models with snow tiles filtered out so you can build a more classifier for urban development imagery." %}

To export predictions:

1. Click **Export Predictions**.
2. Enter a unique **Filename**.
3. Choose how to save the data: as a **csv** or a **geojson** file that can be used in GIS applications.
4. Click **OK**.