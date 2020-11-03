# Neural-Seinfeld-Script-Generator
Generates an episode of the TV Series Seinfeld Using LSTM. Uses a single starting word to create a fake script for an episode of the show.

Dependencies - Python 3.x, PyTorch, numpy.

I used a CUDA/GPU to train. Otherwise it takes too long to train on CPU.

Vocabulary size is around 46367 with 109233 lines in the script.


# Architecture
1 embedding layer followed by 2 parallel LSTM layers followed by a linear layer. Adam Optimizer with cross entropy loss was used.

# Hyperparameters
epochs = 15

learning rate = 0.001

embedding dimension = 300

hidden dimension of the LSTM layers = 256

number of LSTM layers = 2

# Neural Seinfeld Script Generation.ipynb
This is the main notebook. Here the architecture is defined, model is trained and validated and then a sample script is generated.

# helper.py
Here several helper functions are present to run parts of the main notebook. Mainly to load data, pre-process data, save the model and load the model etc.

# data
This folder consists of the training and validation data which is basically the script for all episodes of 9 seasons of Seinfeld.

# generated_script_1.txt
This contains a sample script that was generated after running the code.
