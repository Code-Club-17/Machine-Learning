# Machine Learning
### ML Terminology (supervised)
## Labels :
A label is the thing we're predicting—the ***y*** variable in simple linear regression. The label could be the future price of wheat, the kind of animal shown in a picture, the meaning of an audio clip, or just about anything.
## Features :
A feature is an input variable—the ***x*** variable in simple linear regression. A simple machine learning project might use a single feature, while a more sophisticated machine learning project could use millions of features, specified as:***x1,x2,x3...xN***

In the spam detector example, the features could include the following :
   * words in the email text.
   * sender's address.
   * time of day the email was sent.
   * email contains the phrase "one weird trick."

**Examples**
An example is a particular instance of data, ***x***. (We put ***x*** in boldface to indicate that it is a vector.) We break examples into two categories:
   * labeled examples.
   * unlabeled examples.
   
A ***labeled example*** includes both feature(s) and the label. That is: **labeled examples: {features, label}: (x, y)** 

Use labeled examples to ***train*** the model. In our spam detector example, the labeled examples would be individual emails that users have explicitly marked as "spam" or "not spam."

For example, the following table shows 5 labeled examples from a data set containing information about housing prices in California:

***features={housingMedianAge,totalRooms,totalBedrooms}***

***label={medianHouseValue}***

housingMedianAge| totalRooms | totalBedrooms | medianHouseValue	
------------ | ------------- | -------------- | ---------------
15 | 5612 | 1283 | 66900
19 | 7650 | 1901 | 80100
17 | 720  | 174  | 85700
14 | 1501 | 337  | 73400
20 | 1454 | 326  | 65500

An ***unlabeled example*** contains features but not the label. That is:  **unlabeled examples: {features, ?}: (x, ?)**

Here are 3 unlabeled examples from the same housing dataset, which exclude **medianHouseValue**:

***features={housingMedianAge,totalRooms,totalBedrooms}***

housingMedianAge | totalRooms | totalBedrooms
---------------- | -----------| ------------
42 | 1686 | 361
34 | 1226 | 180
33 | 1077 | 271

Once we've trained our model with labeled examples, we use that model to predict the label on unlabeled examples. In the spam detector, unlabeled examples are new emails that humans haven't yet labeled.

## Models

A model defines the relationship between features and label. For example, a spam detection model might associate certain features strongly with "spam". Let's highlight two phases of a model's life:
   * ***Training*** means creating or ***learning*** the model. That is, you show the model labeled examples and enable the model to gradually learn the relationships between features and label.
   * ***Inference*** means applying the trained model to unlabeled examples. That is, you use the trained model to make useful predictions **y'**. For example, during inference, you can predict **medianHouseValue** for new unlabeled examples.

## Regression vs. classification

A ***regression*** model predicts continuous values. For example, regression models make predictions that answer questions like the following:
   * What is the value of a house in California?
   * What is the probability that a user will click on this ad?
   
A ***classification*** model predicts discrete values. For example, classification models make predictions that answer questions like the following:
   * Is a given email message spam or not spam?
   * Is this an image of a dog, a cat, or a hamster?
   
Key Terms
---------
   ***classification model***
   
   A type of machine learning model for distinguishing among two or more discrete classes. For example, a natural language                  processing classification model could determine whether an input sentence was in French, Spanish, or Italian.
   
   ***inference***
   
   In machine learning, often refers to the process of making predictions by applying the trained model to unlabeled examples. In          statistics, inference refers to the process of fitting the parameters of a distribution conditioned on some observed data.               (See the Wikipedia article on statistical inference.)
   
   ***regression model***
   
   A type of model that outputs continuous (typically, floating-point) values.
