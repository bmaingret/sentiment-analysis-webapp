# Deploying a ML model on AWS SageMaker
[*Udacity Machine Learning Engineer Nanodegree Program*](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t) | Machine Learning in Production Project

This repository contains my project for the *Machine Learning in Production* module of the Machine Learning Engineer Nanodegree from Udacity.

Boiler code and utility functions were provided directly by Udacity and are not of my work.
[Udacity Github repository](https://github.com/udacity/sagemaker-deployment)

AWS API Gateway has changed a bit since Udacity's code was released, but the general idea stands.

One thing not mentioned in the notebook is to set up CORS coorectly for the created API.

The [report.html](./report.html) file is the exported notebook in HTML.

## Overview

This project aims to deploy a machine learning model on AWS.

The model will be an LTSM neural network used to classify movie reviews in two categories: positive or negative.

Both model training and deployment is done on AWS SageMaker, and we used PyTorch as NN framework.

Then a simple web page allows to input a movie review and have it classified by the deployed model thanks to AWS API Gateway and Lambda Services:

* API Gateway is used solely for forwarding the request to the defined lambda
* Lambda service is used to handle the HTTP request and response, and invoke our model.
    
![App <-> API <-> Lambda <-> Model](./assets/Web%20App%20Diagram.svg)

## Files

    .
    ├── assets                  # Images
    ├── train                   # Python scripts to define and train the PyTorch model
    ├── serve                   # Python scripts to load the trained PyTorch model and handle data (de)serialization
    ├── index.html              # Simple UI to input a review to classify and retrieve model
    ├── README.md
    ├── report.html             # Exported notebook to HTML
    └── SageMaker Project.ipynb # Jupyter notebook


## Demo

I might leave the model online for some times depending on AWS free tier...

[Sentiment analysis webapp](https://bmaingret.github.io/sentiment-analysis-webapp/)

## HTML report

[Jupyter Notebook HTML](https://bmaingret.github.io/sentiment-analysis-webapp/report.html)
