---
layout: single
classes: wide
collection: projects
title: Cover Letter Generator
subtitle: Generate Cover Letters
date: 2022-05-06 08:33:33 +05:30
header:
  teaser: assets/images/projects/cover-letter-generator.jpg
categories:  
 - Technology  
tags:  
 - python  
 - cover letter 
 - pdf
 - .txt update
---
Programming Language : ![Programming Language](https://img.shields.io/badge/Python-100%25-%233DA639)

Have you ever found yourself stuck in a situation where you have to update only a few fields in a text file and generate a pdf out of it? The worst part of it can be when you have to do it repeatedly. A similar request came from one of my friend who is working in the finance sector where they have pre-defined templates and have to update only selected parts of it such as name, address, contact info and date. Once the fields are updated they need to generate a pdf out of it and share it with the customer. This repetitive task needs to be done multiple times in a day. It's sometimes very sad that technological advancements in the larger organization miss the need of people at the grass-root level.

Based on my discussion with him I thought of creating a python based program which would reduce his unnecessary repetitive task. Since I cannot share the template, I created a dummy problem statement where we need to update the details in a standard cover letter.

This tool contains a GUI and can be updated based on the requirement. Currently, 4 fields can be updated (Name, Date, Job Location and Position) but, one can add more fields as per their requirement by editing the python code.

You can download the executable (.exe) version of this tool by clicking the below link.
Download Cover Letter Generator.

Below is the screenshot of the Application.

 <img src="/assets/images/projects/cover-letter-generator.png" alt="cover-letter-generator" style=" height=2%; width=2%; display: block; margin-left: auto; margin-right: auto;"/><br>

#### Instructions
To use the tool, create a standard cover letter template (sample template) and replace the following (including curly brackets)
Company Name with {company}
Job Location with {location}
Role/Position for which you are applying with {role}
Date will be automatically updated

Once the above required fields are updated, one needs to click on the "Generate Cover Letter" button. This will create a .pdf file with the updated details.

#### Note
* Download the zip file, extract it and retain the img folder. Do not delete or move, else this application will not work. This is a limitation of tKinter package in Python.

#### Source Code
[Click Here](!https://github.com/ashishkr568/cover-letter-generator) to go to the source code.
