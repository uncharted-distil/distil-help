---
title: "Step 4 - Join Datasets"
sidebar: getting-started
permalink: join-datasets.html
previous: create-models
next: view-models
---

Use the optional Join Datasets step to add new features that add more context. Distil's data augmentation recommendation services suggest data that can be joined to expand the model.

## Review dataset suggestions ##

<h5 class="procedure">To view datasets suggested by Distil's data augmentation recommendation services:</h5>

1. Click <span class="fa fa-table"> in the Alerts sidebar.

   {% include image.html file="data-augmentation/join-datasets/open-join-suggestions.png" alt="Access Join Suggestions" %}

2. Click the **World Bank Employment Indicators** dataset to select it, then click **Join**.

   {% include image.html file="data-augmentation/join-datasets/join-suggestion.png" alt="Select the World Bank Employment Indicators dataset" %}

3. Scroll through a sample of records to preview the join. Evaluate how the features from the join dataset have been added to your original selection.
4. Click **Commit Join** to return to the Create Models stage and add any new features to your model.

   {% include image.html file="data-augmentation/join-datasets/join-preview.png" alt="Preview the join before committing" %}

## Next steps ##

Review the generated models to determine whether they accurately predict the target feature.