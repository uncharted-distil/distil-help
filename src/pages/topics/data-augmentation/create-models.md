---
title: "Step 3 - Create Models"
sidebar: getting-started
permalink: create-models.html
previous: select-target
next: join-datasets
---

You must choose features that you think will inform the predictions. Distil will use the chosen features to automatically generate models that predict the target.

## Select the features to model ##

<h5 class="procedure">To choose the features that your model should use in its predictions:</h5>

1. Click **Add** under the features you think may influence the target:
   - **Main_Actor**
   - **Other_Main_Actor**
   - **Actor_Associated_To_Main_Actor**
   - **Actor_Associated_To_Other_Main_Actor**
   - **Main_Actor_Type**
   - **Other_Main_Actor_Type**
   - **Country**
   - **Latitude**
   - **Longitude**
   - **Event_Interaction_Type**
   - **Fatalities**

   {% include image.html file="data-augmentation/create-models/available-features-add.png" alt="Add actors to features to model" %}

   In this example, Distil adds the selected features to the list of Features to Model. You can filter or change the **type&nbsp;<sup class="fa fa-sort-desc" aria-hidden="true" style="display: inline;"></sup>** of any of the features to model.

   {% include image.html file="data-augmentation/create-models/features-to-model.png" alt="Main Actor and Other Main Actor added as features that inform the prediction made by the model" %}

   <div class="panel-group" id="accordion">
    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title"><a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseOne"><span class="fa fa-plus" aria-hidden="true"></span> To remove a feature from the features to model</a></h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse noCrossRef">
        <div class="panel-body">
          Click <strong>Remove</strong> under the feature name in the Features to Model pane or click <strong>Remove All</strong> above the list of features.
          {% include image.html file="data-augmentation/create-models/features-to-model-remove.png" alt="Remove feature from the features to model" %}
        </div>
      </div>
    </div>
   </div>

2. Click **show more** on the **Main_Actor** card to see more values. 
3. Click *Protestors (Iran)* to view samples that match the value in the Samples to Model From table.
4. To exclude these samples from the model, click <span class="fa fa-minus-circle pr-1 exclude-highlight"></span> **Exclude**.
   {% include image.html file="data-augmentation/create-models/exclude-category.png" alt="Omit records with a specific categorical value" %}
5. Click Excluded Samples to review the records you removed.
6. Click <span class="fa fa-globe"></span> to see where those records are located.
   {% include image.html file="data-augmentation/create-models/geographic-data.png" alt="View records on a map" %}

Depending on your task, next you can:

- [Join a dataset](join-datasets.html) to find and incorporate other datasets that may contain additional features that could help improve your models.
- [Generate the models](#generate-the-models) to predict **Event_Type** using the selected features.

{% include important.html content="You must select at least one feature to model from before you can proceed." %}

## Generate the models ##

If your task is to build a predictive model, you can now begin the model generation. Based on your selections, Distil:

1. Automatically determines the number and type of models to predict your target feature.
2. Uses a subset of the actual data to train the models to predict the target using the features selected in this step.
3. Applies the trained models to the rest of the actual data to predict the target feature value in each record.

<h5 class="procedure">To begin the model generation with the current feature selections:</h5>

- Click **Create Models**.

{% include image.html file="data-augmentation/create-models/create-models.png" alt="Create models" %}

In this example, Distil will try to predict the **Event_Type** based on the selected features for a subset of the dataset.

## Next steps ##

Search for datasets to join to the ACLED data.