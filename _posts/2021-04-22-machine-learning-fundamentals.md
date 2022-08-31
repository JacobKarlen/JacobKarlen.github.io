---
title: Machine Learning Fundamentals
date: 2023-04-22 13:37:22 +0100
categories: [Machine Learning, Fundamentals of Machine Learning]
tags: [ml, machine learning, fundamentals, data science]     # TAG names should always be lowercase
---

## An introduction to the fundamentals of Machine Learning
This post, which is the first post of this blog, will dive in to the basics of Machine Learning
and important fundamental concepts. Most of the ideas come from the book [Hands-on Machine Learning with Scikit-Laern, Keras & TensorFlow](https://www.amazon.com/Hands-Machine-Learning-Scikit-Learn-TensorFlow/dp/1492032646) by Aurélien Géron, and this is basically a documentation of me doing the exercises of the first chapter.

## Definition of Machine Learning
Machine Learning can be defined in many ways but essentially it boils down to the art and science of programming computers in such a way that it can learn and generalize from data without being explicitly programmed. 

## Machine Learning process
The first thing you usually start with when applying Machine Learning to a problem, is to educate yourself on the problem at hand, so you get an idea of what might be important factors and attributes of the problem. You would gather data related to the studied problem and explore it to gain insights, and based on this you would probably make some assumptions on what Machine Learning algorithm to use. You would then select a Machine Learning algorithm and train it with the data (usually a subset of the data, called the training set). 

When you have trained the algorithm or model, you would evaluate it on another set of data (the test set) which only includes data that the algorithm has not seen before, to avoid any bias due to over-fitting (will go into more detail later). Hopefully the evaluation of the solution gives us a better understanding of the problem at hand, and if we want to, we can iterate the process and start over training a new algorithm.

## Why Machine Learning and what is it used for?
Machine Learning is a great approach to solving complex problems where it would be too difficult to explicitly code rules. An example of such a problem is optical character recognition (detection of handwritten characters) which is too complex to manually code rules for, since there are a lot of edge cases and slight differences in people's handwriting. Another such example would be natural language processing (speech recognition) where the program needs to be able to distinguish one word from another. A daunting task to program a solution for manually, but a field where the use of Machine Learning excels. 

Machine Learning is also very useful for analyzing images, for example detecting defect products in production or detecting cancer tumors in brain scans. 

It is also a big part of today's search engines, which utilize Machine Learning to provide relevant search results tailored to you. Machine Learning is also used in fraud detection, marketing and more. Basically Machine Learning is in every field facing complex problems, where you can leverage data and computing power to solve it. Another pro is that a lot of systems based on Machine Laerning can adapt to new data and tune itself to a changing environment.


## Batch learning vs Online learning
Batch learning is when the system needs all the available data to be trained, and it will often take a lot of time and computing power, a reason why it is typically done offline (also refered to as offline learning).

Online learning or incremenral learning is when the system can be trained incrementally with additional data. It is usually trained on small sets of data called mini-batches and each batch incremental training is generally pretty cheap and resource light, why it can be performed online.

Generally, an online learning system is fitted more for systems which receive continues sequential flows of data, such as stock market systems. It can also be better for when the systems environment changes quickly and it needs to be continously retrained to adapt to the changes and remain functional. 

## Supervised Learning vs Unsupervised Learning
In supervised learning the training set includes the desired soultions or target, called labels. In unsupervised learning the system has to learn on its own, without labeled data. Typical supervised tasks are classification (for example detecting if an email is spam or not) and it could also be to predict a target value, for example how much a used car would cost based on the features model, manufacturer, year of manufacture and mileage.

Examples of supervised learning alogrithms include k-Nearest Neighbors, Linear Regression, Support Vector Machines (SVMs) and Neural Networks. Examples of unsupervised learning algorithms include clustering, anomaly detection and association rule learning.

## What is a labeled training set?
A labeled training set is a set of samples which each have instances of feature variables (the predictors) and a label (the target). If we for example wanted to classify images of dogs and non-dogs, the feature variables could be all the pixels of the image (which the prediction would be based on) and the label (our target, the thing we want to predict) would be a boolean where 1 = dog and 0 = non-dog. 

This training set would be used to train the Machine Learning algorithm, and hopefully the algorithm will produce a model which generalizes well and can predict if a given image includes a dog or not with a high degree of accuracy.

Something which often can be a problem is obtaining a labeled set of data, and it might cost a lot to buy or require a lot of manual work to clean the data.