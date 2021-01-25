---
layout: post
title:      "Supervised learning "
date:       2021-01-25 07:19:02 +0000
permalink:  supervised_learning
---

## The basics 
A supervised machine learning algorithm relies on labeled input data to learn a function that produces an appropiate output when given new unlabeled data. 

Think of it as a kid, when a kid is first learning, it needs a supervisor, for the sake of the argument this will be us. 
When we want the kid to learn what a tree is, we show the kid pictures, some of them will be trees others will be of other different things. When a picture of a tree shows, we then tell the kid: **This is a Tree**, otherwise, we tell the kid: **This isn't a tree**. 
After a certain period of time the kid will be able to identify, most of the time, the pictures that actually show a tree. **this is supervised learning**

Supervised learning can be used to solve classifictation and regression problems.
***Classification problem*** has a discrete value as an output.The kid and the pictures of trees is an example of classification problem. This means that the picture is a tree or not! Therefore, any problem that has a yes or no output can be said that is a classification problem. 


![](https://github.com/eriikcasstro/dsc-mod-3-project-v2-1-onl01-dtsc-pt-070620/blob/master/table.jpg?raw=true )

In the example above we can see different characteristics of what a classification data could look like. We have a predictor, in this case we have a number of predictors: ***Family, CCavg, Education, Mortgage, Securities Account, Online and Credit card.*** and a label ***Loan***. In the image we are trying to predict if a customer of a bank has a Loan (1) (the label ) based on all the rest of information (predictors). 

It is standard practice that a label is represented with a value 0 or 1. In a classification problem this values are representing No and Yes, respectively. These values are not numerical representations of each, therefore, no mathematical computation should be done with them.


***Regression Problem*** has a number with a decimal point as its outpout. For example, working out the amount of hours a player needs to gain certain points. 

![](https://github.com/eriikcasstro/dsc-mod-3-project-v2-1-onl01-dtsc-pt-070620/blob/master/Regression.jpg?raw=true)


The data used in a Regression Problem will be similar to the data in a Classification problem. We will have an independent variable (or set of independent variables) and a dependent varaible (what we are trying to guess). In our example, we can say that the amount of hours is ***the independent variable*** and the amount of points is the ***dependent variable***.

