---  
layout: single  
classes: wide  
title: Are error metrics and loss the same during model training? 
date: 2022-05-07 11:55:00 +05:30  
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
<br>There is an important distinction between an error metric and a loss function. The entire purpose of loss is to define a "measure of performance" that a training system can use to update the weights automatically. 

In other words, a good choice for loss is the one which is better for Stochastic Gradient Descend(SGD) to use. But an error metric is for human consumption and is easier for humans to understand. An example of an error metric is error rate and accuracy (which is 1-error rate), these tell us what percentage of data in the validation set are classified correctly.

>Loss is for machine consumption and an error metric is for human consumption and let's not consider loss as a suitable metric and keep both of them separate.