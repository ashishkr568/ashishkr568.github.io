---  
layout: single  
classes: wide  
title: Turn Jupyter Notebook into a Standalone Web Application using Binder 
date: 2022-05-25 23:23:23 +05:30  
header:  
  teaser: assets/images/blog/notebook-to-app.jpg  
  caption: Photo by <a href="https://unsplash.com/es/@halacious?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Hal Gatewood</a> on <a href="https://unsplash.com/s/photos/prototype?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>
categories:  
 - Technology  
tags:
 - deep learning
 - jupyter notebook
 - binder
 - voila
 - ipywidgets
 - app development
 - fastai
---  
<img src="/assets/images/blog/notebook-to-app.jpg" alt="notebook-to-app" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>  
<br>Being a Data Scientist, there are situations when we feel that our findings can be better explained with the help of a working prototype. A prototype can be very helpful in giving a birds-eye view of the solution to stakeholders. But due to limited or no knowledge of web development, we either end up looking for some help and if this doesn't work or takes time, we give up on the idea of creating a prototype.

We can overcome this limitation by creating an application in Jupyter Notebook using [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/) (aka jupyter widgets) and deploy it as a standalone web application using [voilà](https://voila.readthedocs.io/en/stable/using.html) and [Binder](https://mybinder.org/). Let's look at a short description of what these tools do as per the description on their website.

 - [ipywidgets](https://ipywidgets.readthedocs.io/en/latest/) - It is also known as jupyter-widgets or simply widgets, are [interactive HTML widgets](https://github.com/jupyter-widgets/ipywidgets/blob/master/docs/source/examples/Index.ipynb) for Jupyter notebooks and the IPython kernel. Learning becomes an immersive, fun experience. Researchers can easily see how changing inputs to a model impact the results.
 - [Voilà](https://voila.readthedocs.io/en/stable/using.html) - Voilà is used to run, convert, and serve a Jupyter notebook as a standalone app.
 - [Binder](https://mybinder.org/) - An online service for building and sharing reproducible and interactive computational environments from online repositories.


I created a standalone web application using these tools to classify an image of a German Traffic Sign. We will use it to describe the steps required to create your own web application. Click [here](https://github.com/ashishkr568/gtsr/blob/main/3_gtsr_app.ipynb). to view the jupyter notebook used for creating this application. 

*If you are interested in dataset used, exploratory data analysis or model development please click [here](/projects/german-traffic-sign-classifier).* 

### Requirements

Binder and  Voilà help us to deploy our notebook app directly from a GitHub repository. We will need the following files in our GitHub repository.
 - *Requirements.txt file* - It contains details of all python packages required for this app to work.
 - *Our trained model* - This is the model we trained on our dataset.
 - *Supporting files* - Any extra files required either for the model to work or used by the application to simplify the results.


### Create an application in Jupyter notebook

Our web application looks like the below image. It only displays the Markdown text in Jupyter Notebook along with the application.

<img src="/assets/images/projects/gtsr-mybinder-app.png" alt="gtsr-mybinder-app" style="width:10%, height:10%; display: block; margin-left: auto; margin-right: auto;"/>

It's a very simple web application which takes an image as input, classifies it using our model and also provides the confidence score. We are using the upload FileUpload widget to create an upload button and also have an on_click event attached to it. Once the user selects the file to be uploaded, it automatically triggers the on_click event. on_click event is where our model is being consumed and we get the predictions. We also have a few widgets for Labels and display output. 

All these widgets are arranged in a **grid layout** as per requirement and aesthetics.

***Note:** Currently this application is accepting one image at a time, but one can modify it to accept multiple files or files in other formats based on requirements.*

Refer [this](https://github.com/ashishkr568/gtsr/blob/main/3_gtsr_app.ipynb) notebook to go through the coding part.

### Binder Configuration
Once we have created our application in the jupyter notebook, and uploaded all the required files in our GitHub repository, we are ready to launch our application using Binder.

Open [Binder](https://mybinder.org/) and fill in the details as per the below image.
 
<img src="/assets/images/projects/gtsr-mybinder-img.png" alt="gtsr-mybinder-img" style=" height=2%; width=2%; display: block; margin-left: auto; margin-right: auto;"/><br>

 1. **GitHub repository name or URL:** This will be the URL for your GitHub repository.
 2. **Branch:** Name of the Git branch which contains the code to be deployed.
 3. **Path to a notebook file:** Mention the name of the notebook which contains the application after`/voila/render/`. Your Path should look like `/voila/render/notebook_name.ipynb`
 4. **URL:** Since we are triggering it through the GitHub URL, we need to selct URL from the drop down.
 5. **Launch:** This will start building your application.
 6. **Application URL:** You can share the autogenerated URL with stakeholders.

> Binder can be used to create an application out of any GitHub repository with the required files. For example, anyone can deploy German Traffic Sign Classification App from my repository and get a hang of it. **It gives life to our repository codes and anyone can deploy a prototype application to get more details about the projects.**

**Note:** Binder is ideally suited for relatively short sessions. [Click here](https://mybinder.readthedocs.io/en/latest/about/user-guidelines.html) to refer its usage guidelines.

> Hope you enjoyed reading. Happy Learning..!!