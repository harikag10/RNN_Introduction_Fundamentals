# Bidirectional RNN

In simple terms, a bidirectional RNN is combining two RNNS. It connects two hidden layers of opposite directions to the same output.

* A Bidirectional RNN considers all input available sequences in both the past and future for estimation of output vector.
* One RNN process the sequence from start to end in a forward time direction and another one process the sequence from backwards from end to start in a negative time direction.
* Outputs from forward states are not connected to inputs of backward states and vice versa too.

BRNNs are especially useful when the input context is needed. For example, in handwriting recognition, the performance can be improved if we know the knowledge of the letters before and after the current letter.

**Architecture :**

![alt text](https://camo.githubusercontent.com/bb59e9ee696d40fa06038bab95692e6b26e41a26/68747470733a2f2f64326c2e61692f5f696d616765732f6269726e6e2e737667)

An additional hidden layer is added that passes the information backwards. The input is fed in normal order for one network and in reverse order for the other network. At every time stamp, the outputs of the two networks are concatenated.

