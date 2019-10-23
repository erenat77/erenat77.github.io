---
title: "Deep learning Project : Face recognition and verification"
date: 2019-03-03
tags: [machine learning, deep learning, data science, neuron network, sudoku, Image analysis, Sequential Model]
header:
  image: "/images/sudoku_ex2.png"
excerpt: "Machine Learning, Transfer learning, VGG, Data Science, python"
mathjax: "true"
---
Face Verification with Anchor images embedded


Face recognition problems commonly fall into two categories:
Face Verification - "is this the claimed person?". For example, at some airports, you can pass through customs by letting a system scan your passport and then verifying that you (the person carrying the passport) are the correct person. A mobile phone that unlocks using your face is also using face verification. This is a 1:1 matching problem.
Face Recognition - "who is this person?". For example, the video lecture showed a face recognition video (https://www.youtube.com/watch?v=wr4rx0Spihs) of Baidu employees entering the office without needing to otherwise identify themselves. This is a 1:K matching problem.
FaceNet learns a neural network that encodes a face image into a vector of 128 numbers. By comparing two such vectors, you can then determine if two pictures are of the same person.

In this assignment, you will:
Implement the triplet loss function
Use a pre-trained model to map face images into 128-dimensional encodings
Use these encodings to perform face verification and face recognition


            ## 1. Read the image and format the image as array with openCV library
            ```python
              import numpy as np

              def test_func(x,y):
                return np.sum(x,y)
            ```

            ## 2. Read the image and format the image as array with openCV library

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
