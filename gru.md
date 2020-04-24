# GRU



**The whole idea of Gated Recurrent models is to get more direct evidence of the effect of early time steps on much later time steps without having too long sequence matrix multiplications**

We can create shortcut connections

While LSTMs have shown to be viable option for avoiding vanishing or exploding gradients, they have higher memory requirement in their architecture

GRUs are improved version of standard recurrent neural networks also defined as RNNs which have gated mechanism.

* It was introduced by Kyunghyun Cho in 2014. [Refer Here](https://arxiv.org/abs/1406.1078)
* The GRU is like a long short-term memory \(LSTM\) with forget gate but has fewer parameters than LSTM, as it lacks an output gate.
* The GRU is the newer generation of Recurrent Neural networks and is pretty similar to an LSTM. GRU’s got rid of the cell state and used the hidden state to transfer information. It also only has two gates, a reset gate and update gate.

