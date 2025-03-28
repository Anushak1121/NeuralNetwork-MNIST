The MNIST (Modified National Institute of Standards and Technology) dataset is one of the most popular datasets used in machine learning and deep learning

It contains 70,000 handwritten images of the digits from 0 to 9

Each image is of 28x28 dimension and is represented using pixels values between 0 and 255, where

0 stands for black
255 stands for white

We used following approach to check model performance in each case.


Baseline Model:

A baseline model with no hidden layers, using vanilla Gradient Descent, and run with 10 epochs yielded a low accuracy (less than 20%)

Effect of Increasing Epochs:

Increasing the number of epochs results in the model being trained for longer, resulting in improved training accuracy
It does take a longer time for execution, which is expected
It is important to note that while running more epochs improves training accuracy, it might not always yield a better validation accuracy. So, running a model for more epochs can lead to an overfit model

Gradient Descent (GD) vs Stochastic Gradient Descent (SGD):

Implementing Stochastic Gradient Descent involves using smaller batches of data to update the model parameters, which resulted in an improved rate of learning for the model. Consequently, we witnessed a largely better model accuracy (~90%) in fewer epochs compared to the baseline model

Effect of Batch Size:

Using a batch size of 32 or 64 did not result in a huge change in model accuracy compared to the use of the entire data as one batch.
As long as we choose a small batch size (like 32 or 64), we can expect an overall better model performance

Effect of Adding a Hidden Layer:

Adding a hidden layer to the baseline model did not improve the model performance largely, but using SGD along with the addition of a hidden layer yielded hugely better results than the baseline model

Effect of Changing the Hidden Layer Activation Function:

Changing the hidden layer activation has a notable effect on the model performance, with tanh and relu activations yielding better results than sigmoid activation
Effect of Additional Hidden Layers:

Adding more hidden layers (while using SGD and relu/tanh activation) yields slightly better performance than a model with only one hidden layer
