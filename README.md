# Alex Hamil Portfolio

## Capstone Project: Home Credit Default
Repository containing Alex Hamil's portfolio of work for the data science project Home Credit Default.

# Table of Contents
- [Business Problem Statement](#Business-Problem-Statement)
- [Our Solution to the Problem](#Our-Solution-to-the-Problem)
- [My Contribution to the Project](#My-Contribution-to-the-Project)
- [Solution's Value to the Business](#Solutions-Value-to-the-Business)
- [Challenges Our Group Faced](#Challenges-Our-Group-Faced)
- [What I learned from the Project](#What-I-earned-from-the-Project)


## [Business Problem Statement](#Business-Problem-Statement)
Home Credit is in the business of trying to provide financial products to customers in unique and diverse markets where the traditional tenets of regulated banking aren't always present. They provide financial products and services to customers that have insufficient or nonexistent traditional credit histories and metrics used to apply for loans and other financial services. In lieu of this, they have alternative data that can be used to try to predict a customer’s ability to repay loans and qualify for services.

The purpose of this project is to create a model that allows Home Credit to build an accurate credit risk profile of their customers based on nontraditional financial data.

## [Our Solution to the Problem](#Our-Solution-to-the-Problem)
* Our solution to the problem started by cleaning and understanding the data and its limitations prior to model selection.
* Next we tried several different models to see which would handle the data and its imbalances the best.
* Finally we decided to create several different models and train them on different segments of the downsampled majority class, while resampling sections from the minorty target variable and finally combining the results in an ensemble model.

## [My Contribution to the Project](#My-Contribution-to-the-Project)
My contributions to the project where centered on creating the models and the graphical representation of the confusion matrices and the ROC-AUC curves.  I have attached the code that was used to generate both the XgBoosted model and the composite model that we ultimately used for out primary model.  This code also includes the graphical measurement metrics for ROC-AUC and the confusion matrices. 

![](/images/Regression%20ROC%20Curve.png)

## [Solution's Value to the Business](#Solutions-Value-to-the-Business)

The Model's classification will be able to help the business understand the costs associated with   
Sensitivity - false positives (identifying customers as credit worthy that are actually risky)  
Specificity - False negatives (identifying customers as risky that would be good candidates for financial products) 

![Specificity](images/Business%20Impact%20Specificty.png)

![Sensitivity](images/Business%20Impact%20Sensitivity.png)

Understanding these rates can help the business consider risk based pricing- where interest rates and credit amounts are adjusted for clients prone to default.

## [Challenges Our Group Faced](#Challenges-Our-Group-Faced)
* With the overwhelming amount of data in the majority class. We found it helpful to downsample the data for this class. This helped reduce overfitting our model to the majority characteristics of customers that are capable of repayment. 
* The limited data available about the minority class meant that we had to resample some of the same data from this class while using various data samples from the majority class. This allowed us to use a larger sample of data and potentially capture more patterns and interactions in the data.
* Capturing the nuances of the data by averaging multiple prediction models helped us to reduce variance and account for different aspects of the data. As you can see we were able to account for 85% of the variance in the data with our ensemble model. 

## [What I learned from the Project](#What-I-earned-from-the-Project)
I learned the importance of developing adequate domain knowledge, importance of understanding your data and its limitations, and the importance of resilient modeling methods.  

Having enough domain knowledge is crucial because it allows you to understand the real-world importance of the features and variables you are studying. This is critical for selecting important variables and effective feature engineering.  

Knowing your data and its limitations is important because it allows you to adjust for important missing variables, and guard against overfit or poor ROC-AUC results. Imbalanced data can minize important details of the target variable or contributing variables.  

Knowing when and how to use multiple modeling methods and the best methods for sampling the most amount of data is important. This will allow the model to account for as much variance as possible while trying to avoid overfit. 
