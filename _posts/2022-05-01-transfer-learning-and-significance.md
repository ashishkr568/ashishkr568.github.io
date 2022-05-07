---  
layout: single  
classes: wide  
title: What is transfer learning and what is its significance? 
date: 2022-05-02 20:32:00 +05:30  
header:  
  teaser: assets/images/blog/transfer-learning.jpg
  caption: Image Credits Unsplash  
categories:  
 - Technology  
tags:  
 - machine learning  
 - deep learning   
 - artificial intelligence 
 - image classification
 - image identification
 - resnet
---  
<img src="/assets/images/blog/transfer-learning.jpg" alt="transfer-learning.jpg" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>In the field of deep learning, we have the ability to use the capabilities of a model which was designed to do an entirely different set of tasks as we want to do it now.  These original models are termed as pretrained models.

These pretrained models have weights according to the original datasets. The benefit of using a pretrained model is that it is already very capable. In the case of image classification where we use ResNet as a pretrained model, these models are already very capable of identifying edged, lines and colour gradients. There is no point in retraining our model from scratch as we won't be able to provide that much information and example to our model with the limited amount of data we have.

Now since these pretrained models are trained for a different task,  we need to remove the last layer since that was specifically customized for the original training task and replace it with a new layer having random weights. This last part of the model is known as the head and then we can train this model according to our dataset. This process of updating the parameters of a pretrained model by adding additional epochs for our dataset is known as *fine-tuning* 

These pretrained models can allow us to train more accurate models in lesser time and money.

> *This technique of using pretrained models to do an entirely different set of tasks is known as transfer learning.*