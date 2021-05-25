---
title: "Remote sensing - Create labels"
sidebar: getting-started
permalink: remote-sensing-label-creation.html
previous: remote-sensing-overview
next: remote-sensing-create-models
---

To start working with the satellite imagery tile data, search for *sentinel* in the Select Model or Dataset view and click the *sentinel-sample* dataset.

{% include image.html file="remote-sensing/select-dataset.png" alt="Search for the sentinel dataset and click it to begin annotating data" %}

## Add a label to the dataset ##

In the New Model: Select Target view, you can add a label to your dataset and identify some samples that contain positive and negatives examples of the terrain you're trying to predict (snow).

1. Click <span class="fa fa-tag"></span> **Label**.
   {% include image.html file="remote-sensing/select-target-label.png" alt="Click Label to create a new label feature for the satellite imagery" %}
2. In the Label Creation dialog, enter a name for the label you want to add (e.g. *Snow*).

   The new label appears above the list of features on the left and indicates that all samples in the dataset are currently *unlabeled*.
   {% include image.html file="remote-sensing/label-feature.png" alt="Your new label feature appears above the other features in the dataset" %}
3. Use the Samples table to identify and label examples of tiles that contain snow:
   <ul type="a">
     <li>Click samples containing tiles that depict snow to select them.</li>
     <li>
      Once you have selected a number of samples, click <span class="fa fa-plus-circle"></span> <b>Positive</b> to label them.
      <figure><img class="docimage" src="images/remote-sensing/select-positive.png" alt="Your new label feature appears above the other features in the dataset" /></figure>
    </li>
   </ul>
    <div class="panel-group" id="accordion">
    <div class="panel panel-default">
      <div class="panel-heading">
        <h4 class="panel-title"><a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseOne"><span class="fa fa-plus" aria-hidden="true"></span> To inspect the terrain of a tile...</a></h4>
      </div>
      <div id="collapseOne" class="panel-collapse collapse noCrossRef">
        <div class="panel-body">
          There are several ways you can inspect the terrain of tiles in your data:
          <ul>
            <li>Hover over a tile and click <span class="fa fa-search-plus"></span> to expand it. Here you can:
                <ul>
                    <li>View the tile at full size.</li>
                    <li>Increase or decrease the <span class="fa fa-adjust fa-rotate-180"></span> <b>Brightness</b> of the tile to bring out details that may not be visible in the normal display.</li>
                    <li><b>Upscale</b> the image to enhance the resolution.</li>
                </ul>
            </li>
            <li>Change the <span class="fa fa-clone"></span> <b>Image layer</b> to view a different satellite image band that is more sensitive to the terrain you're looking for.</li>
            <li>Adjust the Samples table layout:
              <ul>
                <li>Click <span class="fa fa-image"></span> to view just the tiles without any of the other features in your dataset.</li>
                <li>Click <span class="fa fa-globe"></span> to view where the tiles are located on a geographic map.</li>
              </ul>
            </li>
            <li>Filter the samples using the other features in the dataset.</li>
          </ul>
        </div>
      </div>
    </div>
   </div>
4. Follow the previous step to also select and label examples of tiles that *do not* contain snow. In this case, click <span class="fa fa-minus-circle"></span> **Negative** to label them.
   {% include note.html content="To proceed to the next steps, you must label at least one positive and one negative example." %}

## Refine your positive and negative examples ##

At this point, you can use the samples you've already labeled to search for more positive examples. **Search Similar** uses your labeled input to rank the remaining unlabeled samples in terms of how confident the system is that they contain target terrain type (snow).

1. Click **Search Similar**.
   {% include image.html file="remote-sensing/search-similar.png" alt="Search for tiles similar to your positive examples and sort them by confidence" %}
   Note that now, the Samples table is sorted by a new **Confidence** column on the right. Based on your previous labeled input, samples at the top of the list are ones that the system determines are most likely to contain your target terrain (snow).
2. Repeat steps 3&ndash;4 above to add more positive and negative examples.

   <div class="panel-group" id="accordion">
   <div class="panel panel-default">
     <div class="panel-heading">
       <h4 class="panel-title"><a class="noCrossRef accordion-toggle" data-toggle="collapse" data-parent="#accordion" href="#collapseTwo"><span class="fa fa-plus" aria-hidden="true"></span> To use confidence scores to find positive or negative examples...</a></h4>
     </div>
     <div id="collapseTwo" class="panel-collapse collapse noCrossRef">
       <div class="panel-body">
           Filter the <b>Confidence</b> chart on the right by clicking and dragging a selection around areas of interest. To find potential negative examples, focus on the left side of the chart (low confidence). To find potential positive examples, focus on the right side (high confidence).
           <figure><img class="docimage" src="images/remote-sensing/confidence-scores.png" alt="Filter samples by confidence scores" /></figure>
       </div>
     </div>
   </div>
   </div>
   {% include tip.html content="If a high number of the samples in the table are either positive or negative, click <b>Select All</b> and then individually deselect any samples that don't match." %}

To build a large enough set of labels, repeat the process of labeling positive and negative examples and then using **Search Similar** as necessary. Each time the system should be better at identifying positive examples, allowing you to quickly build your training data.

{% include tip.html content="For the best results, it is recommended that you label roughly the same number of positive and negative examples, including at least 100 of each." %}

## Save the dataset ##

Once you have labeled a sufficient number of positive and negative examples, you can save your dataset. Saving the dataset makes a copy of the original dataset with:

- Your new label feature consisting of your positive and negative examples
- All unlabeled samples removed
  {% include note.html content="Unlabeled samples are removed from the saved dataset so you can use it to train a model to predict your target terrain. Any unlabeled samples would not be useful for this process." %}

To save your dataset:

1. Click **Save**, enter a unique **Dataset Name** and click **OK**.
2. Click **Go Back to Select Target Page** to begin training your model.