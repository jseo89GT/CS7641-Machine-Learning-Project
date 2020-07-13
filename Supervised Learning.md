---
layout: page
title: Supervised Learning
subtitle: Logistic Regression, LightGBM, Random Forest, XGBoost
---

<p style="text-align: justify;">
For this project, we attempted a variety of supervised classification methods that are well suited to binary classification problems with severe class imbalance. In this section, we describe some background theory, our approaches and results obtained from this step.
</p>

<p style="text-align: justify;">
  <b>1. Logistic Model</b>
  Logistic 
</p>

<p style="text-align: justify;">
  <b>2. Random Forest Classification</b>
</p>
Random forest is a classical tree-based ensemble learning method that constructs multiple individual decision trees in order to evaluate a class assignment of a data point.
<p style="text-align: justify;">
  <b>3. XGBoost Classifier</b>
</p> 
XGBoost is a tree-based ensemble learning framework that implements gradient boosting method.  

<p style="text-align: justify;">
  <b>4. LightGBM Classifier</b>
</p>
LightGMB is another ensemble learning framework using gradient boosting method. It is similar to XGBoost but known to run faster and occupy less memory compared to XGboost.



<p style="text-align: justify;">
  <b>Approach and Results</b>
</p>
 We tried these supervied learning methods on two cases of data - 1. the preprocessed data following the previous steps, and 2. PCA implmeneted to this preprocessed data. After training each model, we let the model produce prediction of the test data and recorded their score through kaggle submission. The hyper-parameters were manually and lightly tuned to obtain moderate test scores. Followig table shows the results.
 
Table 1: Result from each model

<table style="width:100%">
  <tr>
    <th>Model(s) Name</th>
    <th>Hyper-parameters</th>
    <th>Prediction Score</th>
    <th>Prediction Score with PCA</th>

  </tr>
  <tr>
    <td>Logistic Regression</td>
    <td></td>
    <td>Type of device used for transaction</td>
  </tr>
  <tr>
    <td>Rabdom Forest Classification</td>
    <td>C</td>
    <td>Additional metadata about device</td>
  </tr>
  <tr>
    <td>XGBoost Classifier</td>
    <td> #</td>
    <td>0.928964</td>
    <td>0.921232</td>
  </tr>
  <tr>
    <td>LightGBM Classifier</td>
    <td>0.922326</td>
    <td>0.913388</td>
  </tr>
</table>
 
