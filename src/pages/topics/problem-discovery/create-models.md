---
title: "Step 2 - Select Model Features"
sidebar: getting-started
permalink: problem-discovery-create-models.html
previous: problem-discovery-select-target
next:
---

Finally, you must choose features that you think will inform the predictions.

## Select the features to model ##

<h5 class="procedure">To choose the features that you think will predict the target feature:</h5>

1. Click **Add** under the **Horsepower** and **Cylinders** features.

   {% include image.html file="problem-discovery/create-models/available-features-add.png" alt="Add cylinders to features to model" %}

   In this example, Distil adds the selected features to the list of Features to Model. You can filter or change the **Type&nbsp;<sup class="fa fa-sort-desc" aria-hidden="true" style="display: inline;"></sup>** of any of the features to model.

   {% include image.html file="problem-discovery/create-models/features-to-model.png" alt="Cylinders and horsepower added as features that inform the prediction made by the model" %}

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

7. To remove these records, click each row and then click <span class="fa fa-minus-circle pr-1 exclude-highlight"></span> **Exclude**.

   {% include image.html file="problem-discovery/create-models/features-to-model-range.png" alt="Omit records with 0 horsepower" %}

9. Click **Excluded Samples** to review the records you removed. There is a collection of three and five cylinder vehicles, as well as some four cylinder vehicles with no horsepower.

   {% include image.html file="problem-discovery/create-models/excluded-samples.png" alt="Samples removed from consideration" %}

Your model definition is now complete and you can use your selections to create models.