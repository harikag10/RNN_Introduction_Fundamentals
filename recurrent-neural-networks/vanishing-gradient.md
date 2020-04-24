# Vanishing Gradient

Before discussing the vanishing gradient let us understand in more detail about the **Gradient descent** , which is one of the most widely used algorithms for optimization that uses the concept of derivatives to find the minimum of a function.

And the function which we want to minimize here is the 'cost function', also referred to as the loss function.

As we know, the gradient descent algorithm finds the global minimum of the cost function that is going to be an optimal setup for a network

**How do we minimize any function?**

![Parabola](../.gitbook/assets/image%20%281%29.png)

Consider we are at the green dot and we want to reach the minima, the red dot here. We need to decide in which direction we want to move. So gradient descent is used to make these decisions using derivatives, which is calculated as the slope of the graph at any particular point.

The learning rate is the size of the steps taken to reach the minima. And we update the next position or the weights in our case using this formula, which we have come across earlier $$W_{new} = W_{old} - (n*dL/dW) $$ 

So the direction in which the weights move depend on the slope at that point, which may be positive or negative and hence the weights get updated accordingly. So, if the point is to the right of the minima , the slope is positive and the weight value decreases or moves towards left to reach the minima and similarly if the point is towards the left of minima, it gets increased as the slope is negative here.

Now, the foundation being laid, lets discuss the issue of vanishing gradients in RNN.

In RNNs

* Information travels through time, which means that information from previous time point is fed as input to the next time point.
* We can calculate the error, at each point.

Lets look into error which is calculated after forward pass,

In the back propagation process, we adjust our weight matrices with the use of a gradient. In the process, gradients are calculated by continuous multiplications of derivatives. The value of these derivatives may be so small, that these continuous multiplications may cause the gradient to practically “vanish”.

RNNs suffer from the problem of vanishing gradients, which hampers learning of long data sequences

For instance we have a sentence like ' I went to France, - - - -. And now I speak \_? '

So in this particular sentence, after _France_, there are say 4-5 words and then the sentence , _I speak_ and we need to predict the next word. In order to do that , we need to go way back in the sentence to understand the context and then predict the word as _'French'_ in this case.

This is commonly referred to as the 'Long term dependency'

