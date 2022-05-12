---  
layout: single  
classes: wide  
title: Are error metrics and loss the same during model training? 
date: 2022-05-12 11:00:00 +05:30  
header:  
  teaser: assets/images/blog/error-metric.jpg  
  caption: Image Credits Unsplash  
categories:  
 - Technology  
tags:  
 - machine learning  
 - deep learning   
 - artificial intelligence 
 - error metric
 - loss function
 - sgd
---  
<img src="/assets/images/blog/error-metric.jpg" alt="error metric vs loss" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>A "Loss" and "Metric" are the 2 things which we look at the end of each epoch[^1] to check the performance of a model. These are very closely related but are not exactly the same. Let's look at their significance.

There is an important distinction between an error metric and a loss function. A Metric is a function that measures the quality of the prediction using the validation set and it is printed at the end of each epoch. A common type of metric is error metric and accuracy (which is 1-error metric). However, the entire purpose of loss is to define a "measure of performance" that a training system can use to update the weights automatically. 

If we do a slight change in the parameters(weights) of a loss function, we might see how loss varies or a set of parameters which improves or deteriorates the model performance but this change in parameters can be so little that it might not change our predictions and due to this error rate does not change. But our model can use this information to improve model performance.

>loss and metric are closely related but metric is for human consumption as it is easier for humans to understand the model's performance and loss is something which our computer uses, to measure the model's performance and decide on updating the parameters.

[^1]:An Epoch is an event when our model has looked at each of the data points in the training set once.