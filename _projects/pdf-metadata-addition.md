---
layout: single
classes: wide
collection: projects
title: PDF Metadata Addition Tool
subtitle: Add metadata to any pdf file
date: 2022-05-05 18:00:33 +05:30
header:
  teaser: assets/images/projects/pdf-metadata-addition.jpg
categories:  
 - Technology  
tags:  
 - python  
 - metadata 
 - pdf
---
Programming Language : ![Programming Language](https://img.shields.io/badge/Python-100%25-%233DA639)

Metadata is the data about a particular document. PDF metadata is data about a PDF document. It provides additional information about a PDF document, few of metadata are:

 - title 
 - author
 - date of creation
 - modified date
 - copyright information
 - what application was used to create the file. 

These fields can only be updated using paid version of Adobe Reader or uploading your document to some online portal. But if you don't want to do any of the above, feel free to use this tool.

It has a user friendly GUI (created in python) where you can fill in the required details and add metadata to your documants for free.

You can download the executable (.exe) version of this tool by clicking the below link.

Download [PDF_Metatata_Addition_Tool.zip](https://github.com/ashishkr568/pdf-metadata-addition/raw/main/PDF_Metatata_Addition_Tool.zip)

Below are the steps to use the application.

 1. Fill in the required information and click "Add Metadata"
 <img src="/assets/images/projects/pdf-metadata-filled.PNG" alt="pdf-metadata-addition" style=" height=2%; width=2%; display: block; margin-left: auto; margin-right: auto;"/><br>
 
 2. The updated metadata of pdf file can be verified by opening the updated pdf in Acrobat Reader and Navigate to its Properties section. This will open properties of the pdf file and the metadata data can be viewed in Description and Custom Section.
 <img src="/assets/images/projects/pdf-metadata-check.PNG" alt="pdf-metadata-addition" style=" height=2%; width=2%; display: block; margin-left: auto; margin-right: auto;"/><br>


#### Note
* Download the zip file, extract it and retain the img folder. Do not delete or move, else this application will not work. This is a limitation of tKinter package in Python.

#### Developer Info
This Application is created in python using PyPDF2 and tKinter Package (for GUI).

#### Source Code
[Click Here](!https://github.com/ashishkr568/pdf-metadata-addition) to go to the source code.