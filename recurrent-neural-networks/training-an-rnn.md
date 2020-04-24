# Training an RNN

To train any Artificial Neural Network, we use an algorithm called Back propagation. It refers to the process of updating the network weights to minimize the loss or error in predictions.

The process can be described as below- 

1. First we propagate the input through the network to get an output .
2. An error is computed by comparing the predicted output with the actual output
3. We then calculate the derivatives of the error/loss with respect to the weights that we want to update
4. The weights are adjusted
5. The process is repeated

To train a Recurrent Neural Network , we use back propagation as in any feed forward neural network. But as the back propagation happens for every time stamp, it is commonly referred to as Back propagation through time \(BPTT\).

Lets discuss the issues faced during back propagation-

* Training a neural network implies we need to update the weights associated to the layers.The weights are updated as follows

 $$W_{new} = W_{old} + (n*dL/dW) $$ 

$$W_{new} $$- new value of weight, $$W_{old} $$- old value, n - learning rate and L- Loss or the error in prediction, defined as

```text
(Actual o/p - Predicted o/p)^2
```

dL/dW - is the gradient of the loss with respect to the weight we want to update.

* When this dL/dW is too small &lt;&lt; &lt;&lt; 1 - this implies change in W is too small , so there is not much difference in the value of weights and it takes a lot of time to reach the global minima, where the learning of the network stops. This is called as the **Vanishing Gradient Problem**

For example, if we want to predict the next word in a sentence and the sentence is too long, which would require us to go back by many steps to understand the context. This would lead to the dL/dW to become small and this is also referred to as **long term dependencies**

On the contrary, the gradient dL/dW can become too large , which leads to huge changes in the weights and this leads to the Exploding Gradient Problem **Exploding Gradient Problem**

Let us further discuss the Vanishing Gradient problem

