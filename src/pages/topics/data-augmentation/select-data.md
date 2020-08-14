---
title: "Step 1 - Select data"
sidebar: getting-started
permalink: select-data.html
previous: workflow-overview
next: select-target
---

To begin, you need to find a dataset relevant to your problem. You can search for datasets from the Select Data view.

## Search for a dataset ##

<h5 class="procedure">To find datasets related to Middle East attributes:</h5>

1. Enter *Middle East* in the **Search** field on the Select Model or Dataset view. As you type, Distil returns each dataset that contains the keyword in its list of features or full description.
2. Review the **acled** result to determine its relevancy.
   - The **Top Features**, which indicate the most <a href="#" data-toggle="tooltip" data-original-title="Importance is based on how features influence other columns.">important</a> features (columns), list country (**iso**) and several other quantitative features such as **event_date**.
     {% include note.html content="Features are listed in order of importance, a measure of how much influence a feature has on other features in the dataset." %}
   -  The **Topics**, inferred from <a href="#" data-toggle="tooltip" data-original-title="From column headers and text values in columns.">text</a> in the dataset, indicates that the dataset is about military conflict.
3. Click **More Details** to see a complete summary.
   {% include image.html file="data-augmentation/select-data/more-details.png" alt="Expand to view more dataset details" class="screenshot" %}
4. Click **Dataset Name: acled** to choose the ACLED dataset for further inspection.
   {% include image.html file="data-augmentation/select-data/select-dataset.png" alt="Choose a dataset to begin selecting which features to include in your model" class="screenshot" %}

## Next steps ##

Choose a feature in the dataset that you want to predict with your model.