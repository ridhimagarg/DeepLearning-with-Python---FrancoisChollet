# Key Take Aways by Deep Learning with Python by Francois Chollet

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

### Analogy: How DL works?

    - Each layer in deep NN applies a transformation which disentangles the data little more. 

### Derivative
    
    - Continuity: A small change in x will result a small change in y - intiution behind continiuity.
    
### Stochastic Gradient Descent

    - Compute the loss (pred- actual)
    - Derivative of loss with parameters(W's)
    - Move parameter (w) little bit in opposite direction of gradient which helps in reducing loss
              w(t+1) = w(t) - step_size * grad(loss w.r.t. w) 

### Prefect Analogy: SGD + momentum

    - It could happen that there is ball on hill which could stuck at local minima instead of global minima. 
    If ball will have enough momentum then it will not stuck at local minima. Momentum is implemented based not only on current slope(accln) but also the velocity (resulting from past accln). 
    Similarly in SGD+momentum, parameter will be updated based on current gradient and previous parameter update.

## Chapter 3

### Choose no. of neurons in layers

    - If one layer drops one information then later layer cannot recover that information. So for 46(lets say) different classes 16-dim layer is limited to learn 46 classes. Hence small layers can act as a bottleneck.


### Cross-entropy and Sparse Cross Entropy Loss

    - Cross entropy is for binary labels and cross entropy loss is for integer classes.

### Data Normalization for test data

    - Normalization of test data happens on mean and variance of training data.

### Tip for small training dataset

    - If small no. of training data then we should choose small networks with few layers and neurons to avoid severe overfitting.

## Chapter 4

### Why validation data?

    Can't we test over testing data means just two splits: training data and testing data.

    - Because of information leakage, we need validation data. while evaluating/optimizing(hyperparameter tuning) our model takes away some information of validation data. Hence, to test over testing data gives us unbiased results without any information leakage.

### Data processing in NN

    - To make learning easier we should follow -:

        => low values (0-1)
        => homogenous data

    - Why there is a need to feature engineering in DL?

        - helps in solving problem easily.
        - if you have less training data then creating more useful features helps in learning better model.

### Story of underfitting and overfitting

    - At the begining, optimization and generalization are correlated i.e, lower the loss of training data, lower the loss on the test data. While this is hapening, you model is said to be underfit i.e, your model not yet leant all the relavant patterns.
    But after certain no. of iterations, generalization stops improving thats where model starts to overfit.

    - To prevent model from learn irrelavant patterns: get more training data to learn relavant patterns.

    - To prevent overfitting: Reducing the number of network's size i.e, no. of neurons, layers. 
    What happens is -> High size of network then high no. of parameters then high memoization capacity(training data mapping with targets) hence it prevents generalization over new data. So smaller sized network for overfitted model is suggested.

    But there is a fight between **too much capacity** and <b>not too much capacity</b>

### Optimization and generalization

    - Optimization and generalization is a universal tension. Acheiving a point where both looks okay is difficult task.

### Accuracy lower on test data than validation data

    - It could happen that information leakage is happening at validation data. So in that case we need to use iterate k-fold validation.

## Chapter 5

### Difference between dense layer and conv layer
    
    - Dense layer learn the global parameters
    - Conv layer learn the local parameters

### Properties of Convnet

    - Transational Invariant: It learns and recognize it anywhere i.e, if it recognizes pattern in the upper-left corne then it will be able to recognize that pattern anywhere. A densely connected layer have to learn anew if location changes.
    Convnet requires less features.

    - They can learn spatial features: First conv layer some easy patterns like edges, lines. Second layer learns more complex pattern. This is the way convnets easily learn complex patterns.

### Convolution defined by key parameters

    - Size of the patches extracted from the inputs -> it typically ranges from 3*3, 5*5, etc.
    - Depth of the output feature map -> The no. of filters computed by the convolution.


### Convolutional Stride

    - Stride concept is rarely used as it is used to downsample the height and width of the image. 
    - To downsample the image, instead of stride, max pooling operation is used.

### Max-Pooling Operation

    - 
    
