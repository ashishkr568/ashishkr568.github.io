---  
layout: single  
classes: wide  
title: Is your Machine Learning model serving the right purpose? 
date: 2022-05-07 07:05:00 +05:30  
header:  
  teaser: assets/images/blog/ml-purpose.jpg  
  caption: Image Credits Unsplash  
categories:  
 - Technology  
tags:  
 - machine learning  
 - deep learning   
 - artificial intelligence  
---  
<img src="/assets/images/blog/ml-purpose.jpg" alt="Difference Between ML and Computer Program" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br> In my earlier blog, we looked at the similarities and differences between our machine learning or deep learning model and regular computer program. If you have not gone through it, I would request you to go through it by clicking [here](/blog/2022/05/05/computer-program-ml-dl-compare/).

Before checking if a machine learning model serves the right purpose, let's first look at a few of the limitations of a machine learning model, and then we will look at a few of the unwanted scenarios a machine learning model can lead to.

Let's first start with the limitations of a Machine learning model:

**Limitations of Machine Learning**
 - A model cannot be created without data
 - A model can only learn to operate on patterns seen in the input data which is used to train it.
 - This learning approach only created predictions not recommended actions. Actions will be something that will be taken based on these predictions.
 - It's not enough to only have training data, a label for each of the training data is required.
 
Apart from these limitations, we also need to take into account if our machine learning model fills the gap between organizational goals and model capabilities. Let's understand this with an example. 

Let's consider the Recommendation system which is widely used to predict products a user might purchase. It is often used in e-commerce industries to display customized products on the home page of a website by showing the highest-ranked items. These models are generally created by looking at the user's buying history or the products they have visited. These recommendation systems will always predict the products which the user has already known about, rather than new products that the user might be interested in hearing about. This is very different from the experience if you go to your local bookseller for buying books, they inquire about your taste and then suggest authors or series that you have never heard of before.

Another limitation of the machine learning model arises when it creates a feedback loop. Let's take an example of a predictive policing model which is created on arrests made in the past. Now we use this model to predict crime, this model will not predict crime rather it will predict arrests. The law enforcement officer using this model will decide to focus more on these areas resulting in higher arrests in these areas. If we then use this new data to retrain our model it will create a feedback loop which fails the entire purpose of this model.

We will look at the steps to overcome these issues in another blog. Till then stay tuned.