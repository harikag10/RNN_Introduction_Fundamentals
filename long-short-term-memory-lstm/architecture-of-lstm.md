# Architecture of LSTM

LSTMs are special kind of RNNs, designed explicitly to overcome the long term dependency problem. The repeating modules of neural networks in LSTM have a complex structure compared to that of RNN. The repeating module in LSTM has four interacting layers

* Memory cell
* Forget gate
* Input gate
* Output gate

![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM3-chain.png)

Now lets familiarize with the notations![alt text](https://colah.github.io/posts/2015-08-Understanding-LSTMs/img/LSTM2-notation.png)

* Memory/Cell-state - This is represented as the horizontal layer running through the top of the diagram. It has some linear transformations such as pointwise multiplication and addition
* Gates - These are used to optionally let information through using sigmoid neural network layers, which outputs in either 0 or 1, representing the information which we want to leave or the information we want to persist.

