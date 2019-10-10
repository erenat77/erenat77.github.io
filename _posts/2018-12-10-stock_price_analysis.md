---
title: "Deep learning Project : Stock price Analysis"
date: 2018-12-10
tags: [machine learning, deep learning, data science, neuron network, LSTM, Stock Analysis]
header:
  image: "/images/RNN_rolled.png"
excerpt: "Machine Learning, Stock Analysis, Data Science"
mathjax: "true"
---
# Stock Price Analysis with LSTM

## General Information about RNN models
*  In the last few years, there have been incredible success applying RNNs to a variety of problems: speech recognition, language modeling, translation, image captioning.
*  RNN and LSTM and derivatives use mainly sequential processing over time. See the horizontal arrow in the diagram below:
![My helpful screenshot](/images/RNN-unrolled2.png)
*  This arrow means that long-term information has to sequentially travel through all cells before getting to the present processing cell. This means it can be easily corrupted by being multiplied many time by small numbers < 0. This is the cause of vanishing gradients.
*  To the rescue, came the LSTM module, which today can be seen as multiple switch gates, and a bit like ResNet it can bypass units and thus remember for longer time steps. LSTM thus have a way to remove some of the vanishing gradients problems
![LSTM](/images/LSTM.png)
## Architecture of LSTMs
* A typical LSTM network is comprised of different memory blocks called cells
(the rectangles that we see in the image).  There are two states that are being transferred to the next cell; the cell state and the hidden state. The memory blocks are responsible for remembering things and manipulations to this memory is done through three major mechanisms, called gates. Each of them is being discussed below.
1. Forget gate:
![fgate](/images/fgate.png)
* A forget gate is responsible for removing information from the cell state. The information that is no longer required for the LSTM to understand things or the information that is of less importance is removed via multiplication of a filter. This is required for optimizing the performance of the LSTM network.
* This gate takes in two inputs; h_t-1 and x_t.
  * **h_t-1** is the hidden state from the previous cell or the output of the previous cell
  * **x_t** is the input at that particular time step
2. Input Gate
![igate](/images/igate.png)
* The input gate is responsible for the addition of information to the cell state. This addition of information is basically three-step process as seen from the diagram above.
  * Regulating what values need to be added to the cell state by involving a sigmoid function. This is basically very similar to the forget gate and acts as a filter for all the information from h_t-1 and x_t.
  * Creating a vector containing all possible values that can be added (as perceived from h_t-1 and x_t) to the cell state. This is done using the tanh function, which outputs values from -1 to +1.  
  * Multiplying the value of the regulatory filter (the sigmoid gate) to the created vector (the tanh function) and then adding this useful information to the cell state via addition operation.
3. Output Gate
![ogate](/images/ogate.png)

## My model to estimate the next close value of this particular Stock

* Import the date and separate the data as train and test
* Visualize the data over time
* Checked the correlation btw features and decide which feature will be used for this Analysis
* Use past 60 days data to estimate the following date **close** value

You might reach the repository through this [link](https://github.com/erenat77)
### H3 Heading

Here's some basic text.

And here's some *italics*

Here's some **bold** texts.

What about a [link](https://github.com/erenat77)

Here's a bulleted list:
* First
+ seconds
- Third

Here is numbered list
1. First
2. second
3. Third

Python code block:
```python
  import numpy as np

  def test_func(x,y):
    return np.sum(x,y)
```

Here is some inline code `x+y`.

Here is an image:
<img src="{{site.url}}{{ site.baseurl }}/image/data_sci2.jpg" alt="linearly separable data">

Here is some math:
$$z=x+y$$
$$z=x/y$$
