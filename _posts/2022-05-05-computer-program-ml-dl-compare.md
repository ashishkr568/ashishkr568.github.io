---  
layout: single  
classes: wide  
title: Difference Between Machine Learning or Deep Learning Model and a normal computer program?  
date: 2022-05-05 14:05:00 +05:30  
header:  
  teaser: assets/images/blog/computer-program-ml-dl-compare.jpg  
  caption: Image Credits Unsplash  
categories:  
 - Technology  
tags:  
 - machine learning  
 - deep learning  
 - computer program  
 - Artificial Intelligence  
---  
<img src="/assets/images/blog/computer-program-ml-dl-compare.jpg" alt="Difference Between ML and Computer Program" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>Data Science, Machine Learning, Deep Learning and Artificial Intelligence are a few of the buzzwords in the current times. Let's see how machine learning and deep learning models different from normal computer programs.  
  
Machine learning model in general terms is more like regular programming which gets the computer to complete a specific task.  
A very simple machine learning model looks like the one below.  
  
{% mermaid %}  
graph LR;  
    Inputs-->Program-->Results;  
{% endmermaid %}  
  
Let's take a very simple program where we need to sort an array. Here we provide the input as an unsorted array to the program and get the output as a sorted array.   
  
The main thing to note over here is that our minds can formulate the exact steps required to sort this array.  
  
Now let's take another example, where we want to classify images of cats and dogs. Can we write down every minute step required to classify them? The answer is No, as our brain classifies without us being consciously aware of it.  
  
If we cannot identify the minute details with which we can classify cats and dogs, then how do we tell computers to do it for us.   
  
The way to another approach to this problem is: instead of telling the computer the exact steps required to solve a problem, we show it examples of the problems to solve and let it figure out how to solve them by itself.  
  
This brings us to our definition of Machine Learning:   
  
>Machine Learning is the training of programs developed by allowing computers to learn from their experience rather than thorough manually coding each step.  
  
To allow a computer to learn from its experience below are the certain requirements that need to be met.  
 - Weight assignment  
 - Monitor performance based on different weight assignment  
 - Mechanism to alter the weight assignment to maximize the performance.  
 
Lets look at each of these reuquirements in details:
  
 - **Weight Assignment:** Weights are just another variable and weight assignment is a particular choice of values for these variables. As per the above diagram, a program's inputs are values that it processes to produce results. For example-  in the case of image identification image pixels acts as inputs and classification as a "dog" or "cat" will be the result. In this case, the weight assignments are other values that define how the program will operate. Since these will affect the program, these will also be another kind of input.   
This adds another input to our previous diagram and the updated one would look like this:  
  
{% mermaid %}  
graph LR;  
Inputs-->Model  
Weights-->Model  
Model-->Results  
{% endmermaid %}  
  
**Note:** We have changed our box form program to model, this follows the modern terminology and also reflects that model is a special kind of program.   
  
Now, this model with weights in addition to input can do many different things based on weights. But how do we check the performance of the program, this brings us to our other requirement.  
  
 - **Monitor performance based on different weight assignments-** This will tell us about the effectiveness of any current weight assignment in terms of actual performance. In the case of our cats and dogs classification, it will tell us the confidence with which our program classifies a cat or a dog.  
With this, we will update our diagram by adding the performance and the updated diagram will look like  
  
{% mermaid %}  
graph LR;  
Inputs-->Model  
Weights-->Model  
Model-->Results  
Results-->Performance  
{% endmermaid %}  
  
**Note:** These weights are also known as model parameters.  
  
- **Mechanism to alter the weight assignment to maximize the performance-** Learning can be entirely automatic only when we can automate the process of varying weights by monitoring performance and maximizing the performance.  The performance will act as feedback for varying the weights. So our above diagram will be updated as below:  
  
{% mermaid %}  
graph LR;  
Inputs-->Model  
Weights-->Model  
Model-->Results  
Results-->Performance  
Performance-->|update|Weights  
{% endmermaid %}  
  
Now let's update the above terminologies with the latest deep learning jargon.  
  
 - The functional form of the model is called architecture.  
 - The weights are called parameters  
 - Results are predictions which are calculated from independent variables, which is the data without including the labels.   
 - The measure of performance is called loss  
 - The loss depends not only on the predictions but also on the correct labels (also known as the target or dependent variables).  
  
So our above model after applying the deep learning jargon looks like the below diagram:  
  
{% mermaid %}  
graph LR;  
Inputs-->Architecture  
Parameters-->Architecture  
Architecture-->Predictions  
Predictions-->Loss  
Loss-->|update|Parameters  
Labels-->Loss  
{% endmermaid %}  
  
Once the model is trained and we have selected our best-performing weights, we can think of weights being part of the model as we are not going to change it anymore.  
This will be identical to our original diagram and can be treated just like a regular computer program.  
  
{% mermaid %}  
graph LR;  
    Inputs-->Model-->results;  
{% endmermaid %}  
  
> Deep learning is a speciality within machine learning that uses neural networks with multiple layers. or in other terms Deep Learning is just a modern area in the more general discipline of machine learning.
