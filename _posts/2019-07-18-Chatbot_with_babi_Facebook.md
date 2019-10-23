---
title: "Chatbot with BABI dataset from Facebook research"
date: 2019-07-20
tags: [machine learning, deep learning, data science, neuron network, chat bot, RNN Model]
header:
  image:
excerpt: "Machine Learning, NLP, Chatbot, Data Science, python"
mathjax: "true"
---
![Chatbot](/images/chatbot0.jpg)

Chatbot by using the babi dataset released by Facebook research and there's a link below.

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
![example](/images/chatbot31.png)

This is how I created the models
1. Input Memory Representation
2. Output Memory Representation
3. Generating Final Prediction
Eventually, created a **RNN** model with multiple layers

This is how the single layer looks like.
![example](/images/chatbot1.png)

1. The first key component of the single layer is the input memory representation.The first thin we will going to receive is an input set of x1,x2,x3 etc..Those are the sentences or stories to be stored in memory.
![example](/images/chatbot5.png)

2. We're going to convert that entire set of Xs into memory vectors. So those memory vectors we're gonna call **mi**.
![example](/images/chatbot6.png)

3. We'll use cares for embedding this to convert sentences and then we later on have another embedding an encoder process for C sub AI and we'll also be getting that question or query calling Q and that's also going to be embedded so we'll embed that to obtain an internal state which you will

4. Eventually, we're going to compute the match between you and memory M sub AI by taking the inner product followed by a soft Max operation within this single layer so that will look something like this.
![example](/images/chatbot7.png)

5. This is all going to input memory representation. output memory representation each x AI has a corresponding OutPut vector C sub AI and this is given in the simplest case by another embedding matrix which we'll just call C.
![output_embedings](/images/chatbot8.png)

6. The response vector from the memory O is then a sum over the transform inputs C sub I waited by the probability vector for the input and here's the equation 0 is equal to the sum of PMI times see Evi and because the function from input output is smooth we can then compute gradients and back propagate through this.
![output_embedings](/images/chatbot9.png)

7. The final third step is generating a single final prediction. In this step, the sum of the output vector 0 and the input embedding U is passed through a final weight matrix that will label a capital W here and then a soft Max is used to produce the predicted label.

This is how the multiple layers look like.
![output_embedings](/images/chatbot10.png)

Please check my repository at the following link.
![Chatbot_github](https://github.com/erenat77/chatbot_with_Babi_Data_Set.git)

Have fun !
