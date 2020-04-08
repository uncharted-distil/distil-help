---
title: "Step 2 - Select Target"
sidebar: getting-started
permalink: select-target.html
previous: select-data
next: create-models
---

Now that you have a relevant dataset, you must choose the target feature that you want to predict.

## Select the target feature to predict ##

<h5 class="procedure">To choose the target feature that you want to predict:</h5>

1. Review the list of available features in the Select Target view.
   {% include note.html content="Feature summaries show the values for each column/field in the dataset. Distil automatically infers the type of data stored for each feature. To change the inferred value, use the **type&nbsp;<sup class=\"fa fa-sort-desc\" aria-hidden=\"true\" style=\"display: inline;\"></sup>** drop-down on the upper right corner of the summary." %}

2. Use the **Search** field to filter on *event*.
   {% include image.html file="data-augmentation/select-target/target-feature-search.png" alt="Search available features for event" %}

2. On the **Event_Type** feature summary, click **Select Target**.

   {% include image.html file="data-augmentation/select-target/target-feature-select.png" alt="Set event type feature as target" %}

   Distil automatically sends you to the next step, adding the feature to the model definition and listing a sample of actual event type values.

   {% include image.html file="data-augmentation/select-target/target-feature-samples.png" alt="Sample of values for selected target (event type)" %}

   {% include note.html content="You can change the target at any time by returning to the Select Target view. Click <strong>Select Target</strong> in the navigation bar to go back." %}

The target you select determines the type of results the model will generate.

<table>
  <thead>
    <tr class="header">
      <th>Feature type</th>
      <th>Model type</th>
      <th>Prediction</th>
      <th>Results</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td><a href="#" data-toggle="tooltip" data-original-title="Has values that are real numbers">Continuous</a></td>
      <td>Regression</td>
      <td>Numerical value</td>
      <td>Correct and incorrect predictions based on a configurable distance from the actual target feature values</td>
    </tr>
    <tr>
      <td><a href="#" data-toggle="tooltip" data-original-title="Has a finite set of categories reused across records">Categorical</a></td>
      <td>Classification</td>
      <td>Category</td>
      <td>Correct and incorrect predictions based the actual target feature category</td>
    </tr>
  </tbody>
</table>

**Event Type** is a categorical feature that will produce classification results.

## Next steps ##

Select the features that the model should use to predict the target feature and begin the model generation.