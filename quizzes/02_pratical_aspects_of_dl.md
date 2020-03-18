## Practical aspects of deep learning - week 1

1. If you have 10,000,000 examples, how would you split the train/dev/test set?
a) 33% train. 33% dev. 33% test
b) 98% train. 1% dev. 1% test
c) 60% train. 20% dev. 20% test

2. The dev and test set should:

a) Come from the same distribution
b) Come from different distributions
c) Be identical to each other (same (x,y) pairs)
d) Have the same number of examples

3. If your Neural Network model seems to have high variance, what of the following would be promising things to try?

[] Make the Neural Network deeper
[] Increase the number of units in each hidden layer
[] Add regularization
[] Get more test data
[] Get more training data

4. You are working on an automated check-out kiosk for a supermarket, and are building a classifier for apples, bananas and oranges. Suppose your classifier obtains a training set error of 0.5%, and a dev set error of 7%. Which of the following are promising things to try to improve your classifier? (Check all that apply.)

[] Increase the regularization parameter lambda
[] Decrease the regularization parameter lambda
[] Get more training data
[] Use a bigger neural network

5. What is weight decay?

a) A regularization technique (such as L2 regularization) that results in gradient descent shrinking the weights on every iteration.
b) Gradual corruption of the weights in the neural network if it is trained on noisy data.
c) The process of gradually decreasing the learning rate during training.
d) A technique to avoid vanishing gradient by imposing a ceiling on the values of the weights.

6. What happens when you increase the regularization hyperparameter lambda?

a) Weights are pushed toward becoming smaller (closer to 0)
b) Weights are pushed toward becoming bigger (further from 0)
c) Doubling lambda should roughly result in doubling the weights
d) Gradient descent taking bigger steps with each iteration (proportional to lambda)

7. With the inverted dropout technique, at test time:

a) You do not apply dropout (do not randomly eliminate units), but keep the 1/keep_prob factor in the calculations used in training.
b) You do not apply dropout (do not randomly eliminate units) and do not keep the 1/keep_prob factor in the calculations used in training
c) You apply dropout (randomly eliminating units) but keep the 1/keep_prob factor in the calculations used in training.
d) You apply dropout (randomly eliminating units) and do not keep the 1/keep_prob factor in the calculations used in training

8. Increasing the parameter keep_prob from (say) 0.5 to 0.6 will likely cause the following: (Check the two that apply)

[] Increasing the regularization effect
[] Reducing the regularization effect
[] Causing the neural network to end up with a higher training set error
[] Causing the neural network to end up with a lower training set error

9. Which of these techniques are useful for reducing variance (reducing overfitting)? (Check all that apply.)


[] L2 regularization
[] Data augmentation
[] Xavier initialization
[] Dropout
[] Exploding gradient
[] Vanishing gradient
[] Gradient Checking

10. Why do we normalize the inputs *x*?

a) It makes the parameter initialization faster
b) It makes the cost function faster to optimize
c) It makes it easier to visualize the data
d) Normalization is another word for regularization--It helps to reduce variance

