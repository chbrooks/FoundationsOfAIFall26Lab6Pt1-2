### Lab 6, Part 2. PyTorch.

#### #### Due Dec 8, 11:59pm. 

To submit, add your code to this repo.

In this asynchronous lab, you'll get some basic exposure to PyTorch, 
which is a Python library for deep learning. In lab 3, we'll extend this to build
a convolutional neural network (CNN).

To begin, please read through [this tutorial](https://docs.pytorch.org/tutorials/beginner/basics/intro.html).
You should install PyTorch on your own computer and run locally. Work through steps 1-7 (you can skim/skip part
5, which explains how PyTorch implements gradient descent.)

Then, change the dataset used to be CIFAR-10, which we saw earlier. (You can read more about included datasets [here](https://docs.pytorch.org/vision/stable/datasets.html))
You will need to change the initial layer in your network - the FashionMNIST data has an input size of 28x28, 
whereas CIFAR10 is 3*32*32.

Add your new network to this repo. In part 3, we'll modify it to add convolutional layers.

