---
title: "Step 1 - Select Model Features"
sidebar: getting-started
permalink: model-generation-create-models.html
previous: model-generation-overview
next: model-generation-view-models
---

To begin, you must choose features that you think will inform the predictions. Distil will use the chosen features to automatically generate models that predict the target.

## Select the features to model ##

<h5 class="procedure">To choose the features that your model should use in its predictions:</h5>

1. Click **Add** under the **Horsepower** and **Cylinders** features to send them to the list of Features to Model.

   {% include image.html file="problem-discovery/create-models/available-features-add.png" alt="Add cylinders to features to model" %}

   {% include note.html content="You can filter or change the <b>type&nbsp;<sup class=\"fa fa-sort-desc\" aria-hidden=\"true\" style=\"display: inline;\"></sup></b> of any of the features to model." %}

   <div class="panel-group" id="accordion">
    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title"><a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseOne"><span class="fa fa-plus" aria-hidden="true"></span> To remove a feature from the features to model</a></h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse noCrossRef">
        <div class="panel-body">
          Click <strong>Remove</strong> under the feature name in the Features to Model pane or click <b>Remove All</b> above the list of features.
          {% include image.html file="problem-discovery/create-models/features-to-model-remove.png" alt="Remove feature from the features to model" %}
        </div>
      </div>
    </div>
   </div>

2. Note the distribution of categories for the **Cylinders** feature. Four, six and eight cylinder engines appear often, while three and five cylinder engines appear much less frequently.

   {% include image.html file="problem-discovery/create-models/cylinders.png" alt="Distribution of cylinder values in the dataset" %}

3. Click the three-cylinder category to view samples that match the value in the Samples to Model From table.
4. To exclude these samples from the model, click <span class="fa fa-minus-circle pr-1 exclude-highlight"></span> **Exclude**.
   {% include image.html file="problem-discovery/create-models/exclude-category.png" alt="Omit records with a specific categorical value" %}
5. Repeat steps 3–4 for the five-cylinder category as well.
6. Review the updated Samples to Model From table. Click the column headers to sort by feature and check for extreme values that may indicate problems with the data. Note that several rows have no value for **Horsepower**.

   {% include image.html file="problem-discovery/create-models/samples-to-model-from-error.png" alt="Record with no horsepower value" %}

8. To remove these records, click each row and then click <span class="fa fa-minus-circle pr-1 exclude-highlight"></span> **Exclude**.

   {% include image.html file="problem-discovery/create-models/features-to-model-range.png" alt="Omit records with no horsepower value" %}

9. Click **Excluded Samples** to review the records you removed. There is a collection of three and five cylinder vehicles, as well as some four cylinder vehicles with no horsepower.

   {% include image.html file="problem-discovery/create-models/excluded-samples.png" alt="Samples removed from consideration" %}

## Generate the models ##

You can now begin the model generation. Based on your selections, Distil:

1. Automatically determines the number and type of models to predict your target feature.
2. Uses a subset of the actual data to train the models to predict the target using the features selected in this step.
3. Applies the trained models to the rest of the actual data to predict the target feature value in each record.

<h5 class="procedure">To begin the model generation with the current feature selections:</h5>

- Click **Create Models**.

{% include image.html file="model-generation/create-models/create-models.png" alt="Create models" %}

{% include note.html content="Click <i class=\"fa fa-cog\" aria-hidden=\"true\" style=\"display: inline;\"></i> to limit the number of generated models, set a processing time limit or specify the quality of training models." %}

In this example, Distil will attempt to predict **Acceleration** based on the **Horsepower** and **Cylinders** features for a subset of the dataset.

## Next steps ##

Review the generated models to determine whether they accurately predict the target feature.