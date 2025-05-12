# 🧠 Assignment 1 - RNN-Based Educational NLP Model

## 💡 Problem Statement

This assignment focuses on building a simple RNN model in Keras that can perform **two distinct NLP tasks** using educational content:

1. **Text Classification:** Classify educational text snippets into one of three categories — *Math, Science, or History*.
2. **Next Word Generation:** Predict the next 20 words given an input sentence fragment (auto-completion).

The goal is to demonstrate a basic understanding of RNNs using Keras and TensorFlow.

---

## 🧠 Model Architectures

### 1. **Text Classification Model**
- **Embedding Layer**: Converts word indices to dense vector representations.
- **GRU Layer** (or SimpleRNN): Captures sequential dependencies.
- **Dense Layer** (ReLU): For intermediate representation.
- **Output Layer** (Softmax): Predicts class probabilities for 3 categories.


Embedding(input_dim=vocab_size, output_dim=64)
GRU(64) or SimpleRNN(64)
Dense(32, activation='relu')
Dense(3, activation='softmax')

##  Next Word Generation Model

Embedding Layer: Vector representation of tokens.
GRU Layer: Learns temporal structure of text.
Dense Layer (Softmax): Predicts the next word in the sequence.

Embedding(input_dim=vocab_size, output_dim=64)
GRU(100)
Dense(vocab_size, activation='softmax')
