---  
layout: single  
classes: wide  
title: Why it is advised to resize an image to 224 pixels while dealing with images in deep learning and what would happen if we increase or decrease the pixel size? 
date: 2022-05-07 10:00:00 +05:30  
header:  
  teaser: assets/images/blog/image-resize.png  
  caption: Image Credits Unsplash  
categories:  
 - Technology  
tags:  
 - machine learning  
 - deep learning   
 - artificial intelligence 
 - image classification
 - image identification
 - resize image
 - 224px
---  
<img src="/assets/images/blog/image-resize.png" alt="Image Resize" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>Have you ever thought about why it is always advised to use 224 in the image transformation function while you deal with any computer vision problem in deep learning? What will happen if you increase or decrease this size? If these are a few of the questions that ever came to your mind then you have been landed in the correct spot.

These 224 pixels have become standard size due to historical reasons (old pre-trained models required this size exactly), but with the current advancements, we can use any size.

Let's see what will happen if we increase the image size. We will allow the model to see greater details in the image which eventually will give better results, but this comes with the cost of increased processing time and memory consumption.

Now if we reduce the image size, the details are also lost and this can reduce the model performance, but it will reduce the memory consumption and computational time.

So whenever we are dealing with image classification problems where the model has to look into greater details and we have the bandwidth of time and can use machines with higher computational power, we can use a bigger image size otherwise, 224 pixels does a good job till now.
