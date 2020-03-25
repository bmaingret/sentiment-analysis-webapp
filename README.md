# Deploying a ML model on AWS SageMaker
[*Udacity Machine Learning Engineer Nanodegree Program*](https://www.udacity.com/course/machine-learning-engineer-nanodegree--nd009t) | Machine Learning in Production Project

This repository contains my project for the *Machine Learning in Production* module of the Machine Learning Engineer Nanodegree from Udacity.

Boiler code and utility functions were provided directly by Udacity and are not of my work.
[Udacity Github repository](https://github.com/udacity/sagemaker-deployment)

AWS API Gateway has changed a bit since Udacity's code was released, but the general idea stands.

One thing not mentioned in the notebook is to set up CORS coorectly for the created API.

## Overview

This project aims to deploy a machine learning model on AWS.

The model will be an LTSM neural network used to classify movie reviews in two categories: positive or negative.

Both model training and deployment is done on AWS SageMaker, and we used PyTorch as NN framework.

Then a simple web page allows to input a movie review and have it classified by the deployed model thanks to AWS API Gateway and Lambda Services:

* API Gateway is used solely for forwarding the request to the defined lambda
* Lambda service is used to handle the HTTP request and response, and invoke our model.
    
![App <-> API <-> Lambda <-> Model](./Web%20App%20Diagram.svg)

## Demo

I might leave the model online for some times depending on AWS free tier...

[Sentiment analysis webapp](https://bmaingret.github.io/sentiment-analysis-webapp/)
