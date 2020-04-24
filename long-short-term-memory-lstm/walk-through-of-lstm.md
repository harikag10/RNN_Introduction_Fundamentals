# Walk through of LSTM



To understand the working of LSTM network, let us consider an example of text prediction, where we are trying to predict the next word based on the previous words.

Firstly, we need to decide what information we want to remember and what to forget. This is decided using a sigmoid layer called the 'forget gate' layer. Here the output of sigmoid activation function as we know is between 0 and 1 for each number in the cell state 𝐶𝑡−1Ct−1, taking as inputs ℎ𝑡−1ht−1, the output from the previous layer and the 𝑥𝑡xt, the current input of the layer. A '0' indicates that we can forget about that information and discard it and '1' indicates that we need to remember it.

![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-f.png)

Let us understand it by going to back to our language model. Suppose, we are talking about a subject's gender, but we have the next input as a new subject, we would want to ignore that information about the gender of the previous subject. This is achieved using the forget gate as discussed above.

The next step is to decide what new information we are going to add to the cell state.

This is done in 2 steps. First the sigmoid layer or the input gate layer is used to decide what values we want to update and then the tanh layer results in a vector of new values that can be added. So the state gets updated with the new values.

![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-i.png)

So in our example, we want to add the information about the gender of the new subject which replaces the old value, that we want to forget.The cell state gets updated.

Finally we want the output. In this case, the sigmoid layer decides what parts of the cell state we want to ouput. The cell state 𝐶𝑡Ct is also passed through tanh which outputs values between -1 and +1. This is multiplied by the output of the sigmoid layer and results in the required parts.

![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-C.png)

𝐶𝑡−1Ct−1 is the old cell state we are updating to new state Ct by multiplying with the function 𝑓𝑡ft, then we add the new value i\*𝐶𝑡Ct

So in our language example, as the network has seen the subject, it might want to output something relevant to what comes next. Say, if a verb is followed next, the network might output if the subject is singular or plural, so that we will know what form of verb to be added.

![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-focus-o.png)

LSTM Suffers from high complexity in the hidden layer. For identical size of hidden layers, a typical LSTM has about four times more paramters than Regular RNN

There are many variants of LSTM,

* One introduced by Gers & Schmidhuber \(2000\), is adding “peephole connections.”, which means that the gate layers can take a look at the cell state.
* Another variation is to use coupled forget and input gates
* Another important variant is the Gated Recurrent Unit, which we are going to dicuss in a little detail here.

