## Neural Network Basics - week 2

1. What does a neuron compute?

a) A neuron computes an activation function followed by a linear function (z = Wx + b)

**b) A neuron computes a linear function (z = Wx + b) followed by an activation function**

c) A neuron computes the mean of all features before applying the output to an activation function

d) A neuron computes a function g that scales the input x linearly (Wx + b)

2. Which of these is the "Logistic Loss"?

a) L(i)(y^(i),y(i))=max(0,y(i)−y^(i))

**b) L(i)(y^(i),y(i))=−(y(i)log(y^(i))+(1−y(i))log(1−y^(i)))**

c) L(i)(y^(i),y(i))=∣y(i)−y^(i)∣2

d) L(i)(y^(i),y(i))=∣y(i)−y^(i)∣

3. Suppose img is a (32,32,3) array, representing a 32x32 image with 3 color channels red, green and blue. How do you reshape this into a column vector?

a) x = img.reshape((32*32,3))

**b) x = img.reshape((32*32*3,1))**

c) x = img.reshape((3,32*32))

d) x = img.reshape((1,32*32,*3))

4. Consider the two following random arrays "a" and "b":

```sh
a = np.random.randn(2, 3) # a.shape = (2, 3)
b = np.random.randn(2, 1) # b.shape = (2, 1)
c = a + b
```

What will be the shape of "c"?

a) c.shape = (2, 3)

b) The computation cannot happen because the sizes don't match. It's going to be "Error"!

c) c.shape = (2, 1)

d) c.shape = (3, 2)

5. Consider the two following random arrays "a" and "b":

```sh
a = np.random.randn(4, 3) # a.shape = (4, 3)
b = np.random.randn(3, 2) # b.shape = (3, 2)
c = a*b
```

What will be the shape of "c"?

**a) The computation cannot happen because the sizes don't match. It's going to be "Error"!**

b) c.shape = (4,2)

c) c.shape = (3, 3)

d) c.shape = (4, 3)

6. Suppose you have n_x input features per example. Recall that X = [x^{(1)} x^{(2)} ... x^{(m)}]. What is the dimension of X?

a) (m, n_x)
b) (1, m)
c) (m, 1)
d) (n_x, m)

7. Recall that "np.dot(a,b)" performs a matrix multiplication on a and b, whereas "a*b" performs an element-wise multiplication.

Consider the two following random arrays "a" and "b":

```sh
a = np.random.randn(12288, 150) # a.shape = (12288, 150)
b = np.random.randn(150, 45) # b.shape = (150, 45)
c = np.dot(a,b)
```

What is the shape of c?

a) The computation cannot happen because the sizes don't match. It's going to be "Error"!

**b) c.shape = (12288, 45)**

c) c.shape = (12288, 150)

d) c.shape = (150,150)

8. Consider the following code snippet:

```sh
# a.shape = (3,4)
# b.shape = (4,1)

for i in range(3):
  for j in range(4):
    c[i][j] = a[i][j] + b[j]
```
How do you vectorize this?

**a) c = a + b.T**

b) c = a + b

c) c = a.T + b

d) c = a.T + b.T

9. Consider the following code:

```sh
a = np.random.randn(3, 3)
b = np.random.randn(3, 1)
c = a*b
```

What will be c? (If you’re not sure, feel free to run this in python to find out).

a) This will invoke broadcasting, so b is copied three times to become (3,3), and *∗ is an element-wise product so c.shape will be (3, 3)

b) This will invoke broadcasting, so b is copied three times to become (3, 3), and *∗ invokes a matrix multiplication operation of two 3x3 matrices so c.shape will be (3, 3)

c) This will multiply a 3x3 matrix a with a 3x1 vector, thus resulting in a 3x1 vector. That is, c.shape = (3,1).

d) It will lead to an error since you cannot use “*” to operate on these two matrices. You need to instead use np.dot(a,b)

10. Consider the following computation graph.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/CLczrXpHEeeA3RJRlG3Uqg_3c66355aff0ae7db9e27206f188267f0_Screen-Shot-2017-08-05-at-6.30.51-PM.png?expiry=1584662400000&hmac=mLExYKNzoCLev56X5I1JfPV0iq4pLYzm_RYHSPO64Oo)

What is the output J?

a) J = (c - 1)*(b + a)

**b) J = (a - 1) * (b + c)**

c) J = a*b + b*c + a*c

d) J = (b - 1) * (c + a)

