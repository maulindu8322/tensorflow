# What is Keras? 

Keras is a
deep-learning framework for Python that provides a convenient way to define and 
train almost any kind of deep-learning models.

Keras has the following key features:
- It allows the same code to run seamlessly on CPU or GPU.
- It has a user-friendly API that makes it easy to quickly prototype deep-learning
models.
- It has built-in support for convolutional networks (for computer vision), recurrent networks (for sequence processing), and any combination of both.
- It supports arbitrary network architectures: multi-input or multi-output models,
layer sharing, model sharing, and so on. This means Keras is appropriate for
building essentially any deep-learning model, from a generative adversarial network to a neural Turing machine.

# Keras, TensorFlow, Theano, and CNTK

Keras is a model-level library, providing high-level building blocks for developing
deep-learning models. It doesn’t handle low-level operations such as tensor manipulation and differentiation. Instead, it relies on a specialized, well-optimized tensor
library to do so, serving as the backend engine of Keras. Rather than choosing a single
tensor library and tying the implementation of Keras to that library, Keras handles the
problem in a modular way (see figure 3.3); thus several different backend engines can
be plugged seamlessly into Keras. Currently, the three existing backend implementations are the <b> TensorFlow backend, the Theano backend, and the Microsoft Cognitive
Toolkit (CNTK) backend </b>. In the future, it’s likely that Keras will be extended to work
with even more deep-learning execution engines.



![Illustration](https://miro.medium.com/max/504/1*zumzj_UJzenHYx0Gyyulyw.png)


 The typical Keras workflow looks just like that example:
1. Define your training data: input tensors and target tensors.
2. Define a network of layers (or model ) that maps your inputs to your targets.
3. Configure the learning process by choosing a loss function, an optimizer, and
some metrics to monitor.
4. Iterate on your training data by calling the fit() method of your model.

There are two ways to define a model: using the <b> Sequential class </b> (only for linear stacks of layers, which is the most common network architecture by far) 
or the <b> functional API </b> (for directed acyclic graphs of layers, which lets you build completely arbitrary architectures).
