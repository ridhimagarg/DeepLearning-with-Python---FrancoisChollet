## Chapter 1

### Job of a loss function

    - To control the o/p of NN in order to measure how far it is from actual value

### Job of a optimizer

    - In DL, we used to send a feedback in form of score. We adjust value of weights in a direction in which it will lower the loss score. This adjustment is job of optimizer which is implemented with Backprop.

* Lenet is developeed by Yan Lecun in 1989

### SVM in two step

    - Step1: Decision Boundary to Hyperplane.
    - Step2: Maximizing the margin

### Kernel Function

    - It is a tractable function that maps any two input points in a initial space to the distance between two points in your target representation

### Why DL become so famous?

     - Automates crucial steps of ML: feature engineering

### Two essential characteristics of DL 

    - Incremental learning, layer by layer way in which increasing complex respresentation
    - Intermediate incrementaal respresentations(weights) are learned jointly.
    - With joint feature learning, whenever one of its feature adjusts then all other related features updated automatically.

### Wave of Investment

    - In 2013, Google acquire DeepMind in $500 million, one of the biggest acquistion in history.

## Chapter 2

### Convention for shape of images

    - Channel-Last convention used by Tensorflow.
    - Channel-first convention used by Theano

### BroadCasting

    - Axes are added to the smaller tensor will be broadcasted to the larger tensor
    - Smaller tensor is repeated alongside these new axes  to match the ndim of larger tensor.

###

