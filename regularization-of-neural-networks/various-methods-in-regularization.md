# Various Methods in Regularization



Regularization refers to controlling the capacity of neural network and prevent it from overfitting. For a better training of RNN, we seperate some part of training dataset to validation dataset. The validation set is used to watch the training process and prevent the network from underfitting or overfitting. Overfitting refers to the difference between training loss and validation loss.

* The L1 and L2 regularization method add a regularization term to a loss function to penalize certain parameter configuration and prevent the coefficients from fitting so perfectly to the training data which leads to overfitting
* Dropout - In general, dropout randomly omits a fraction of the connections between two layers of the network during training.Based on the drop out ratio, we randomly choose a set of neurons to deactivate and this helps in regularizing and it is analogous to feature selection in Machine learning paradigm
* A dropout specifically tailored to RNNs is called [RNNDrop](https://arxiv.org/pdf/1603.05118.pdf)
* For additional regularization techniques please refer [here](https://www.arxiv-vanity.com/papers/1511.08400/)

