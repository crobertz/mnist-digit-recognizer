# MNIST digit recognizer challenge

Kaggle challenge for classifying handwritten digits from MNIST dataset.
Details at <https://www.kaggle.com/c/digit-recognizer/overview>.

## MLP
Neural network with two hidden layers with softmax output.
The first layer has 512 units and the second 256 units.
Each hidden layer is followed by a dropout layer with rate 0.5.

Training is done using Adam optimizer with learning rate 0.003 and categorical cross-entropy loss.
Network was trained using batch size 4000 and 0.2 validation split.
After 50 epochs a training accuracy of 99.29% and validation accuracy of 98.00% was achieved.
On the test set the network achieved an accuracy of 97.728% accuracy.
