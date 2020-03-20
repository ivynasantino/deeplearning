## The basics of ConvNets - week 1

1. What do you think applying this filter to a grayscale image will do?

[[0 1 -1 0],
 [1 3 -3 -1],
 [1 3 -3 -1],
 [0 1 -1 0]]

a) Detect image contrast

b) Detect 45 degree edges

c) Detect vertical edges

d) Detect horizontal edges

2. Suppose your input is a 300 by 300 color (RGB) image, and you are not using a convolutional network. If the first hidden layer has 100 neurons, each one fully connected to the input, how many parameters does this hidden layer have (including the bias parameters)?

a) 9,000,001

b) 9,000,100

c) 27,000,001

**d) 27,000,100**

3. Suppose your input is a 300 by 300 color (RGB) image, and you use a convolutional layer with 100 filters that are each 5x5. How many parameters does this hidden layer have (including the bias parameters)?

a) 2501

b) 2600

c) 7500

d) 7600

4. You have an input volume that is 63x63x16, and convolve it with 32 filters that are each 7x7, using a stride of 2 and no padding. What is the output volume?

a) 29x29x16

b) 16x16x32

c) 29x29x32

d) 16x16x16

5. You have an input volume that is 15x15x8, and pad it using “pad=2.” What is the dimension of the resulting volume (after padding)?

a) 19x19x12

b) 17x17x10

c) 17x17x8

d) 19x19x8

6. You have an input volume that is 63x63x16, and convolve it with 32 filters that are each 7x7, and stride of 1. You want to use a “same” convolution. What is the padding?

a) 1

b) 2

c) 3

d) 7

7. You have an input volume that is 32x32x16, and apply max pooling with a stride of 2 and a filter size of 2. What is the output volume?


a) 15x15x16

b) 16x16x8

c) 16x16x16

d) 32x32x8

8. Because pooling layers do not have parameters, they do not affect the backpropagation (derivatives) calculation.

a) True

**b) False**

9. In lecture we talked about “parameter sharing” as a benefit of using convolutional networks. Which of the following statements about parameter sharing in ConvNets are true? (Check all that apply.)

[ ] It allows parameters learned for one task to be shared even for a different task (transfer learning).

[ x ] It allows a feature detector to be used in multiple locations throughout the whole input image/input volume.

[ x ] It reduces the total number of parameters, thus reducing overfitting.

[ ] It allows gradient descent to set many of the parameters to zero, thus making the connections sparse.

10. In lecture we talked about “sparsity of connections” as a benefit of using convolutional layers. What does this mean?

**a) Each activation in the next layer depends on only a small number of activations from the previous layer.**

b) Each filter is connected to every channel in the previous layer.

c) Regularization causes gradient descent to set many of the parameters to zero.

d) Each layer in a convolutional network is connected only to two other layers

