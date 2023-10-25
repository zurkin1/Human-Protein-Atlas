# Human-Protein-Atlas

![HPA](HPA.jpg)
![HPA3](HPA3.jpg)
https://www.kaggle.com/c/hpa-single-cell-image-classification

## Why is This Challenge Hard?
* My first image processing challenge.
* Rules specific to this challenge.
* Scoring metric is hard to develop.
* Submission file format.
* Notebook only challenge (all libraries have to uploaded. No internet access.)
* No logs.
* Public and private leaderboards. Not sure about the test set coverage.
* No available baseline.
* Large effort by Kaggle ‘grand masters’. “Is this only me, or does the ratio of grandmasters on the leaderboard to total number of teams seem extraordinary high in this competition?” (Darek K. 6’th place).
* Based on previous single cell classification challenge. https://www.kaggle.com/c/human-protein-atlas-image-classification.

## Challenge Overview
* Data: High resolution microscopy images of cells.
* Labels: Protein locations together for all cells in the image.
* Objective: Find protein localizations within a population of cells.
* Rational: Current machine learning models for give a summary of the entire population of cells only.
* Train: 87000 files of four channel images (150 GB).
* Test: 2236 files of four channel images.
* Labels: 
   + Image ID: 5c27f04c-bb99-11e8-b2b9-ac1f6b6435d0, labels: 8|5|0
   + Iamge ID: 5fb643ee-bb99-11e8-b2b9-ac1f6b6435d0, labels: 14|0

![labels](HPA2.jpg)

## Evaluation Metric
* mAP: Mean (over classes) of Average Precision for object detection
* Average Precision (AP): the area under the precision-recall curve
  + The confidence values are critical for this metric
* For the PASCAL VOC challenge, a prediction is positive if IoU ≥ 0.5

## First Attempt
* Use Mmdetection framework
* Very large model zoo
* Fifth place solution
* Black box approach using pipelines
* MaskRCNN

![HPA4](HPA4.jpg)
