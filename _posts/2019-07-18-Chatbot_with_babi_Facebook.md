---
title: "Chatbot with BABI dataset from Facebook research"
date: 2019-07-20
tags: [machine learning, deep learning, data science, neuron network, sudoku, Image analysis, Sequential Model]
header:
  image:
excerpt: "Machine Learning, NLP, Chatbot, Data Science, python"
mathjax: "true"
---
![Chatbot](/images/chatbot0.png)

# Chatbot by using the babi dataset released by Facebook research and there's a link below.

[facebook_babi](https://research.fb.com/downloads.babi)

The type of data we're going to be working with has three main components.
It has a story component.
1. Story
2. Question
3. Answer (Yes/No)

Here is an example.
![example](/images/chatbot2.png)

Please check the following paper called "End-to-End Memory Networks"
[End-to-End Memory Networks](https://research.fb.com/downloads.babi)

Overall of the model :
![example](/images/chatbot3.png)

This is how I created the models
1. Input Memory Representation
2. Output Memory Representation
3. Generating Final Prediction
Eventually, created a **RNN** model with multiple layers

Let's discuss the initial step :
- Remember those are the sentences or stories to be stored in memory.
- And we're going to convert that entire set of Xs into memory vectors.
- those memory vectors we're gonna call em sub AI.
- you can see here we essentially have two types of encoders and the bottom one is the M survives.

Please check my repository at the following link\n
[Chatbot_github](https://github.com/erenat77/chatbot_with_Babi_Data_Set.git)

Have fun !
