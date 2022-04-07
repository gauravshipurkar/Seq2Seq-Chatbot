# Intent-Based-Chatbot

## Table Of Content

- [Overview](#overview)
- [Motivation](#motivation)
- [Technical Aspect](#technical-aspect)
- [Installation](#installation)
- [To Do](#to-do)

## Overview

The project happens to be an AI Seq-to-Seq based Chatbot,  the model is trained on 3 different datasets out of which it performs better on Cornell Movie Dataset. The model utilized comes under Encoder-Decoder Architecture. 

## Motivation

Customer support is crucial in any functioning of any business, thus more importance should be given to entertaining any necessary query of the customer. But when we run the business, it's extremely important how we segregate the manpower needed, thus the energy given to a specific task. A Seq-to-Seq based Chatbot may help in solving & addressing the queries of the consumer. As it generates its answers based on the questions, it is considered superior to an Intent-based Chatbot. But, the major problem is dataset should be enormous & relevant to a field to get answers based on the context of that field.


## Technical Aspect 

The Chatbot designed is a general chatbot that is trained on movie dialogues. The Cornell movie corpus has movie lines present in the document. I converted them into question & answer format for training purposes. It has resulted in a total of 86000 questions & answers but because of low computation power, I was unable to train the model on that number of questions & answers. Hence, the model is trained on a lesser number of questions. 

![](https://github.com/gauravshipurkar/Seq2Seq-Chatbot/blob/main/encoder-decoder.png)

The libraries utilized are **TensorFlow, Keras, Pandas & NumPy**.  In the preprocessing step, I have converted the upper-case alphabets to lower-case resulting in a reduced vocabulary size useful for training. I have also added important tokens like the pad: necessary for padding the questions & answers, the end of the string: signifying the start of an answer, the start of the string: signifying the end of an answer, and out of vocabulary: signifying an out of vocabulary word. 

The model utilized follows an encoder-decoder architecture. The input string is passed into the embedding layer generating a multi-dimensional vector, then passed into the encoder that generates hidden states proceeded by a decoder for predicting each word in the answer based on the previous timestep.

![](https://github.com/gauravshipurkar/Seq2Seq-Chatbot/blob/main/Result.png)

## Installation

The Code is written in Python 3.8. If you don't have Python installed you can find it [here](https://www.python.org/downloads/release/python-380). To install **Open-CV** you can go [here](https://opencv.org/). To install the required packages and libraries, run this command in the project directory after cloning the repository:

```
pip install -r requirements.txt

```

## To Do

- We can add **Beam Search** algorithm after decoder for better accuracy.
- Front-end project.
