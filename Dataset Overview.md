---
layout: page
title: Dataset Overview
subtitle: Dataset description
---
<p style="text-align: justify;">
According to Consumer Sentinel Network Data Book 2019 from the Federal Trade Commission, credit card theft is one of the most common consequences of identity theft. In addition to negatively impacting consumers, merchants lost $9.5 billion in fraudulent transactions in 2019, with the sixth highest number of bad transactions reported in Georgia. Unsurprisingly, minimizing the cost of fraudulent transactions is critical, and several security companies have released public datasets to enable the development of effective fraud detection models. For this project, we will be using the IEEE-CIS Fraud detection dataset published by Vesta Corporation on Kaggle. Prior models on similar datasets have utilized rule induction and decision tree methods to identify fraudulent transactions. We plan to assess several of these techniques, and also attempt different methods of feature engineering/data reduction. </p>

<p style="text-align: justify;">
 <b>1. Dataset Description </b> 
There are two separate categories of data in the data: the id and transaction datasets. The ID dataset consists of identification information (such as the device on which the purchase was made, Operating System used, etc.), while the transaction dataset consists of the information directly tied to the transaction (such as the type of credit card used, billing address, transaction amount, etc.). Each of these additionally have train and test versions respectively. An interesting aspect to this dataset is the presence of certain abstract engineered features. A detailed overview of the features found in each table is shown below:
</p>

Table 1: Overview of the ID dataset

<table style="width:100%">
  <tr>
    <th>Feature(s) Name</th>
    <th>Categorical/String/Numeric? (C/S/N)</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>DeviceType</td>
    <td>C</td>
    <td>Type of device used for transaction</td>
  </tr>
  <tr>
    <td>DeviceInfo</td>
    <td>C</td>
    <td>Additional metadata about device</td>
  </tr>
  <tr>
    <td>id12-id38</td>
    <td>C & N</td>
    <td>Identifying features of buyer/seller (IP,browser, etc.)</td>
  </tr>
</table>

Table 2: Overview of the Transaction dataset

<table style="width:100%">
  <tr>
    <th>Feature(s) Name</th>
    <th>Categorical/String/Numeric? (C/S/N)</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>TransactionDT</td>
    <td>N</td>
    <td>Timedelta of transaction from a certain instant</td>
  </tr>
  <tr>
    <td>TransactionAMT</td>
    <td>N</td>
    <td>Amount of transaction</td>
  </tr>
  <tr>
    <td>ProductCD</td>
    <td>C</td>
    <td>Product code of transaction</td>
  </tr>
  <tr>
    <td>card1 - card6</td>
    <td>C</td>
    <td>Provide information about the type of card used for the transaction</td>
  </tr>
  <tr>
    <td>addr1-2</td>
    <td>S</td>
    <td>Addresses of buyer and receiver</td>
  </tr>  
  <tr>
    <td>P_, R_</td>
    <td>S</td>
    <td>email addresses of buyer and receiver</td>
  </tr>
  <tr>
    <td>C1-C14</td>
    <td>N</td>
    <td>Additional metadata for the card information</td>
  </tr>
  <tr>
    <td>D1-D15</td>
    <td>N</td>
    <td>Datetime metadata</td>
  </tr>
  <tr>
    <td>M1-M9</td>
    <td>C</td>
    <td>Match features (such as the name on card, etc.)</td>
  </tr>
  <tr>
    <td>Vxx</td>
    <td>N</td>
    <td>Vesta engineered features - unknown/undisclosed implication of each column</td>
  </tr>
  <tr>
    <td>isFraud</td>
    <td>C</td>
    <td>Whether the transaction is genuine or fraudulent not (0 or 1) - Only present in training dataset</td>
  </tr>
  
</table>

<p style="text-align: justify;">
<b>2. Objective </b> 

The objective of the problem is to predict a probability for a transaction in the test dataset of being fraudulent (a value between 0 or 1). The submission is evaluated in terms of area under the ROC curve between the predicted value and observed target.
</p>
