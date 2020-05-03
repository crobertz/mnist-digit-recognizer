# MNIST digit recognizer challenge

Kaggle challenge for classifying handwritten digits from MNIST dataset.
Details at <https://www.kaggle.com/c/digit-recognizer/overview>.

## MLP
Neural network with two hidden layers with softmax output based on [Google programming exercise.](https://developers.google.com/machine-learning/crash-course/multi-class-neural-networks/programming-exercise)
The first layer has 512 units and the second 256 units.
Each hidden layer is followed by a dropout layer with rate 0.5.

Training is done using Adam optimizer with learning rate 0.003 and categorical cross-entropy loss.
Network was trained using batch size 4000 and 0.2 validation split.
After 50 epochs a training accuracy of 99.29% and validation accuracy of 98.00% was achieved.
On the test set the network achieved an accuracy of 97.728% accuracy.

## CNN
Convolutional neural network with the following sequential architecture:
- One convolution layer with 32 3x3 filters using same padding, followed by a 2x2 max pooling layer
- Three convolution layers with 32 3x3 filters each with no padding, followed by a 2x2 max pooling layer
- A dense layer of 512 hidden units followed by dropout, followed by a dense layer of 256 hidden units followed by dropout
- A dense layer with softmax activation for 10 classes

Each dropout layer has rate of 0.5 and each activation is ReLU except for the final softmax layer.
The network diagram can be viewed in the CNN directory.

Training was done using the same hyperparameters as MLP with the exception of 60 epochs.
Achieved 99.114% accuracy on test set.
