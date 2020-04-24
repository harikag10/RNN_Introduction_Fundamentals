# Architecture of GRU

![alt text](https://miro.medium.com/max/1400/1*jhi5uOm9PvZfmxvfaCektw.png)

**Update Gate**: First, we have the Update gate. This gate decides what information should be thrown away or kept. Information from the previous hidden state and information from the current input is passed through the sigmoid function. Values come out between 0 and 1. The closer to 0 means to forget, and the closer to 1 means to keep.

**Reset Gate :** The reset gate is another gate is used to decide how much past information to forget.

Several similarities and differences between GRU networks and LSTM networks are outlined in [here](https://arxiv.org/abs/1406.1078).The study found that both models performed better than the other only in certain tasks.

