# Movie-Sentiment-Analysis
This project develops a simple web APP that automatically analyze sentiments based on input movie reviews. It utilizes PyTorch deep learning framework and AWS resources(e.g. *SageMaker*). It results from Udacity Machine Learning Engineering 
[Nanodegree program](https://github.com/udacity/sagemaker-deployment/tree/master/Project).

## Setup Instructions

The notebooks provided in this repository are intended to be executed using Amazon's SageMaker platform. The following is a brief set of instructions on setting up a managed notebook instance using SageMaker, from which the notebooks can be completed and run.

### Log in to the AWS console and create a notebook instance

Log in to the [AWS console](https://console.aws.amazon.com) and go to the SageMaker dashboard. Click on 'Create notebook instance'.
* The notebook name can be anything and using ml.t2.medium is a good idea as it is covered under the free tier. 
* For the role, creating a new role works fine. Using the default options is also okay. 
* It's important to note that you need the notebook instance to have access to S3 resources, which it does by default. In particular, any S3 bucket or object, with “sagemaker" in the name, is available to the notebook.
* Use the option to **git clone** the project repository into the notebook instance by pasting `https://github.com/udacity/ML_SageMaker_Studies.git`

### Open and run the notebook of your choice

Now that the repository has been cloned into the notebook instance you may navigate to any of the notebooks that you wish to complete or execute and work with them. Additional instructions are contained in their respective notebooks.

### Notes
The web API uses API Gateway on AWS, which is further put into pipline of Lambda. But it is used only once and deleted later. So if this code is to be used, one needs to create new entry points either via AWS resources or other utilities.


### Relevant Tutorials

* [Population Segmentation](https://github.com/udacity/ML_SageMaker_Studies/tree/master/Population_Segmentation): Learn how to build and deploy unsupervised models in SageMaker. In this example, you'll cluster US Census data; reducing the dimensionality of data using PCA and the clustering the resulting, top components with k-means.
* [Payment Fraud Detection](https://github.com/udacity/ML_SageMaker_Studies/tree/master/Payment_Fraud_Detection): Learn how to build and deploy a supervised, LinearLearner model in SageMaker. You'll tune a model and handle a case of class imbalance to train a model to detect cases of credit card fraud.
* [Deploy a Custom PyTorch Model (Moon Data)](https://github.com/udacity/ML_SageMaker_Studies/tree/master/Moon_Data): Train and deploy a custom PyTorch neural network that classifies "moon" data; binary data distributed in moon-like shapes.
* [Time Series Forecasting](https://github.com/udacity/ML_SageMaker_Studies/tree/master/Time_Series_Forecasting): Learn to analyze time series data and format it for training a [DeepAR](https://docs.aws.amazon.com/sagemaker/latest/dg/deepar.html) algorithm; a forecasting algorithm that utilizes a recurrent neural network. Train a model to predict household energy consumption patterns and evaluate the results.
