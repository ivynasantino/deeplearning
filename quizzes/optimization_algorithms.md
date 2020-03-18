## Optimization algorithms

1. Which notation would you use to denote the 3rd layer’s activations when the input is the 7th example from the 8th minibatch?

a) a^([3]{7}{8})
b) a^([8]{3}{7})
c) a^([8]{7}{3})
d) a^([3]{8}{7})

2. Which of these statements about mini-batch gradient descent do you agree with?

a) You should implement mini-batch gradient descent without an explicit for-loop over different mini-batches, so that the algorithm processes all mini-batches at the same time (vectorization).
b) One iteration of mini-batch gradient descent (computing on a single mini-batch) is faster than one iteration of batch gradient descent.
c) Training one epoch (one pass through the training set) using mini-batch gradient descent is faster than training one epoch using batch gradient descent.

3. Why is the best mini-batch size usually not 1 and not m, but instead something in-between?

[] If the mini-batch size is m, you end up with stochastic gradient descent, which is usually slower than mini-batch gradient descent.
[] If the mini-batch size is m, you end up with batch gradient descent, which has to process the whole training set before making progress.
[] If the mini-batch size is 1, you lose the benefits of vectorization across examples in the mini-batch.
[] If the mini-batch size is 1, you end up having to process the entire training set before making any progress.

4. Suppose your learning algorithm’s cost JJ, plotted as a function of the number of iterations, looks like this:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/KIycr3grEeeJIwrF5BVsIg_f1c324824bd9220c7ee985cce1521404_cost.png?expiry=1584662400000&hmac=FS8KyQwZkLZ5Tbd5GFEyN-Y-B5doVxaXhIpF6K-zEQM)

Which of the following do you agree with?

a) If you’re using mini-batch gradient descent, something is wrong. But if you’re using batch gradient descent, this looks acceptable.

b) If you’re using mini-batch gradient descent, this looks acceptable. But if you’re using batch gradient descent, something is wrong.

c) Whether you’re using batch gradient descent or mini-batch gradient descent, something is wrong.

d) Whether you’re using batch gradient descent or mini-batch gradient descent, this looks acceptable.

5. Suppose the temperature in Casablanca over the first three days of January are the same:

Jan 1st: θ1 = 10ºC 

Jan 2nd: θ2 = 10ºC 

(We used Fahrenheit in lecture, so will use Celsius here in honor of the metric world.)

Say you use an exponentially weighted average with β=0.5 to track the temperature: v0 = 0, v_t = βv_{t-1} + (1-β)θt. If v_2 is the value computed after day 2 without bias correction, and v_2^{corrected} is the value you compute with bias correction. What are these values? (You might be able to do this without a calculator, but you don't actually need one. Remember what is bias correction doing.)


a) v_2 = 10, v_2^{corrected} = 7.5
b) v_2 = 7.5, v_2^{corrected} = 10
c) v_2 = 10, v_2^{corrected} = 10
d) v_2 = 7.5, v_2^{corrected} = 7.5

6. Which of these is NOT a good learning rate decay scheme? Here, t is the epoch number.

a) α = 1/(1+2t) * α0
b) α = e^t * α0
c) α = 0,95^t * α0
d) α = 1/sqrt(t) * α0

7. You use an exponentially weighted average on the London temperature dataset. You use the following to track the temperature: v_t = β * v_{t-1} + (1-β)θt. The red line below was computed using \beta = 0.9β=0.9. What would happen to your red curve as you vary β? (Check the two that apply)

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/W0boqHgrEee6mw7xN92yoA_3a1f4052dc56969b5d7da4024a46836d_temp.png?expiry=1584662400000&hmac=SwrycA90mxPMYSCM19JA4bWNSNAJW7uP53JTXEl5AN8)

[] Decreasing \betaβ will shift the red line slightly to the right.
[] Increasing \betaβ will shift the red line slightly to the right.
[] Decreasing \betaβ will create more oscillation within the red line.
[] Increasing \betaβ will create more oscillations within the red line.

8. Consider this figure:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/fv6gungsEeeJIwrF5BVsIg_6da8c45ffcd4075de23d8e93884937f1_GD.png?expiry=1584662400000&hmac=bVQPFpLoKtJSPBIrOLdEDCoajoyqZndIGQ96ilLhRqM)

These plots were generated with gradient descent; with gradient descent with momentum (β = 0.5) and gradient descent with momentum (β = 0.9). Which curve corresponds to which algorithm?

a) (1) is gradient descent with momentum (small β). (2) is gradient descent. (3) is gradient descent with momentum (large β)

b) (1) is gradient descent with momentum (small β), (2) is gradient descent with momentum (small β), (3) is gradient descent

c) (1) is gradient descent. (2) is gradient descent with momentum (small β). (3) is gradient descent with momentum (large β)

d) (1) is gradient descent. (2) is gradient descent with momentum (large β) . (3) is gradient descent with momentum (small β)

9. Suppose batch gradient descent in a deep network is taking excessively long to find a value of the parameters that achieves a small value for the cost function *J*(W^[1],b^[1],...,W^[L],b^[L]). Which of the following techniques could help find parameter values that attain a small value for *J*? (Check all that apply)

[] Try better random initialization for the weights

[] Try initializing all the weights to zero

[] Try tuning the learning rate \alphaα

[] Try mini-batch gradient descent

[] Try using Adam

10. Which of the following statements about Adam is False?

a) Adam combines the advantages of RMSProp and momentum

b) Adam should be used with batch gradient computations, not with mini-batches.

c) We usually use “default” values for the hyperparameters β1, β2 and ε in Adam (β1 = 0.9, β2 = 0.999, ε=10^−8)

d) The learning rate hyperparameter \alphaα in Adam usually needs to be tuned.

1 ponto
