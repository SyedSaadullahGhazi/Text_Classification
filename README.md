# Text_Classification
Code creates a sentiment analysis model for IMDB reviews using TensorFlow. It loads the dataset, builds a neural network with a pre-trained embedding layer and two dense layers, compiles with binary cross-entropy loss, trains for 20 epochs, and evaluates performance on test data.

This code implements a sentiment analysis model for IMDB movie reviews using TensorFlow and TensorFlow Hub. Let me explain what it's doing step by step:

Imports: The code begins by importing essential libraries:

NumPy for numerical operations
TensorFlow for building and training neural networks
TensorFlow Hub for using pre-trained models
TensorFlow Datasets for loading the IMDB dataset

Data Loading: The code loads the IMDB reviews dataset and splits it into training, validation, and test sets:

The training set contains all the data from the original training split
The validation set uses the first 60% of the original test split
The test set uses the remaining 40% of the original test split
The as_supervised=True parameter indicates that the data should be formatted as (input, label) pairs

Model Architecture:

A sequential model is created
A hub_layer is added (though this layer is not defined in the provided code - it should be a pre-trained embedding layer from TensorFlow Hub)
A dense layer with 16 neurons and ReLU activation is added
A final dense layer with a single neuron and sigmoid activation for binary classification is added

Model Compilation:

Adam optimizer is used
Binary cross-entropy loss function is specified with from_logits=True (though this seems contradictory with the sigmoid activation)
Accuracy is tracked as a metric

Training:

The model is trained for 20 epochs
Training data is shuffled and processed in batches of 100
Validation is performed using the validation set

Evaluation:

The model is evaluated on the test set
Results are stored but not printed in the shown code

There's a potential issue in the code: a duplicate line for loading the dataset, and the hub_layer is used but not defined in the provided code. The hub_layer should be a pre-trained text embedding layer from TensorFlow Hub, likely using something like Universal Sentence Encoder or BERT.
