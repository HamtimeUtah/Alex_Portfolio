# Capstone Project: Home Credit Default
Repository containing Alex Hamil's portfolio of work for the data science project Home Credit Default.

# Table of Contents
- [Business Problem Statement](#Business Problem Statement)
- [Our solution to the problem](## Our solution to the problem)
- [Usage](#usage)
- [Contributing](#contributing)
- [License](#license)


## Business Problem Statement
Home Credit is in the business of trying to provide financial products to customers in unique and diverse markets where the traditional tenets of regulated banking aren't always present. They provide financial products and services to customers that have insufficient or nonexistent traditional credit histories and metrics used to apply for loans and other financial services. In lieu of this, they have alternative data that can be used to try to predict a customer’s ability to repay loans and qualify for services.

The purpose of this project is to create a model that allows Home Credit to build an accurate credit risk profile of their customers based on nontraditional financial data.

## Our solution to the problem
* Our solution to the problem started by cleaning and understanding the data and its limitations prior to model selection.
* Next we tried several different models to see which would handle the data and its imbalances the best.
* Finally we decided to create several different models and train them on different segments of the downsampled majority class, while resampling sections from the minorty target variable and finally combining the results in an ensemble model.

## My Contribution to the Project

![](/images/Regression%20ROC%20Curve.png)

## Solution's Value to the Business

## Challenges Our Group Faced
* With the overwhelming amount of data in the majority class. We found it helpful to downsample the data for this class. This helped reduce overfitting our model to the majority characteristics of customers that are capable of repayment. 
* The limited data available about the minority class meant that we had to resample some of the same data from this class while using various data samples from the majority class. This allowed us to use a larger sample of data and potentially capture more patterns and interactions in the data.
* Capturing the nuances of the data by averaging multiple prediction models helped us to reduce variance and account for different aspects of the data. As you can see we were able to account for 85% of the variance in the data with our ensemble model. 


