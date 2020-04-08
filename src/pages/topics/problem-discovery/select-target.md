---
title: "Step 1 - Select Target"
sidebar: getting-started
permalink: problem-discovery-select-target.html
previous: problem-discovery-overview
next: problem-discovery-create-models
---

To begin, you must choose the target feature that you want to explore.

## Select the target feature to explore ##

<h5 class="procedure">To choose the target feature that you want to explore:</h5>

1. Review the list of available features in the Select Target view.
   {% include note.html content="Feature summaries show the values for each column/field in the dataset. Distil automatically infers the type of data stored for each feature. To change the inferred value, use the **type&nbsp;<sup class=\"fa fa-sort-desc\" aria-hidden=\"true\" style=\"display: inline;\"></sup>** drop-down on the upper right corner of the summary." %}

2. Use the **Search** field to filter on *acceleration*.
3. On the **acceleration** feature summary, click **Select Target**.

   {% include image.html file="problem-discovery/select-target/target-feature-select.png" alt="Set acceleration feature as target" %}

   Distil automatically sends you to the next step, adding the feature to the model definition and listing a sample of actual acceleration values.

   {% include image.html file="problem-discovery/select-target/target-feature-samples.png" alt="Sample of values for selected target (acceleration)" %}

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

**Acceleration** is a continuous feature that will produce regression results.

## Next steps ##

Select the features that you think should predict the target feature and export the problem definition.