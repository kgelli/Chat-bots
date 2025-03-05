# Question-Answer Chat Bot

A simple question-answering chatbot built using neural networks to understand and respond to queries about object locations and movements.

## Project Overview

This project implements a memory network model that can answer simple questions about stories. The chatbot is trained on the Facebook Babi dataset, which consists of short stories followed by questions.

## Features

- End-to-end memory network architecture
- Processes natural language questions about object locations
- Provides yes/no answers with probability of certainty
- Supports custom stories and questions using vocabulary from the training data

## Model Architecture

The model uses:
- Embedding layers to convert words to vectors
- Memory encoding for both stories and questions
- Attention mechanism to focus on relevant parts of the story
- LSTM layer to process the combined information
- Softmax output layer for final prediction

## Dataset

The model is trained on the Facebook Babi dataset which includes:
- 10,000 training examples
- 1,000 test examples
- Simple stories about people and objects moving between locations

## Requirements

- Python 3
- TensorFlow/Keras
- NumPy
- Matplotlib
- Pickle

## Usage

1. Train the model or use the pre-trained weights (chatbot_120_epochs.h5)
2. Input stories and questions using vocabulary from the dataset
3. Get predictions with confidence scores

## Example

```python
my_story = "John left the kitchen. Sandra dropped the football in the garden."
my_question = "Is the football in the garden?"

# Result
# Predicted answer is: yes
# Probability of certainty was: 0.97079676
```

## Performance

The model achieves over 90% accuracy on the test dataset after 120 epochs of training.

## Limitations

- Limited to the vocabulary in the training dataset
- Only handles yes/no questions
- Designed for simple, direct questions about object locations
