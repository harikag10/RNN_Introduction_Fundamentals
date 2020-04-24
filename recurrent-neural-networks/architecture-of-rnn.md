# Architecture of RNN

The below image shows an RNN being unfolded to a full network, $$x_t$$is input to the network at time t, $$h_t$$is the hidden state at time t also referred to as the memory of the network. It is calculated based on previous hidden state and current input.

Represented by $$h_t= f(Ux_t + Wh_t +b_h) $$

![](../.gitbook/assets/rnn.png)

Here U and W are weights for input and previous state value input respectively, $$b_h $$is the bias associated to the hidden network and f is the non-linearity applied to the sum to generate final cell state.

And output at time t is calculated as shown below :

$$O_t = f(Wh_t + b_o) $$ 

$$b_o $$ is the bias for the output layer

Now, having understood about the maths behind the architecture of an RNN , lets see how to train the network.

