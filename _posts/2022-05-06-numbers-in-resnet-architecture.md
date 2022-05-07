---  
layout: single  
classes: wide  
title: What are the numbers at the end of ResNet Architecture and does it have any significance on model performance and overfitting? 
date: 2022-05-06 12:30:00 +05:30  
header:  
  teaser: assets/images/blog/numbers-in-resnet.jpg 
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
<img src="/assets/images/blog/numbers-in-resnet.jpg" alt="numbers-in-resnet.jpg" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>ResNet is one of the standard architectures which is widely used in computer vision problems. It is both fast and accurate for many datasets and problems. 

Let's see what the number 34 in ResNet34 signifies. These numbers tell how many layers are present in this variant of architecture. Other options are 18, 50, 101 and 152.

*So how do we select a particular architecture for our problem?*

This depends on the size of the data we have for training. Models with a higher number of layers take longer to train and are prone to overfitting. In case we have a small amount of data we should start with a smaller number of layers but with bigger data architecture with more layers can give more accurate results.