# Next Word Prediction using LSTM (PyTorch)

## Overview
This project implements a **word-level Next Word Prediction model** using a **Long Short-Term Memory (LSTM)** neural network in PyTorch.  
Given a sequence of words, the model learns contextual patterns from a text corpus and predicts the most likely next word.

The project is designed with a **clean, end-to-end NLP workflow**, suitable for learning, interviews, and baseline production use.

---

## Key Features
- Word-level language modeling using LSTM
- Proper text preprocessing and vocabulary construction
- Special token handling (`<PAD>`, `<OOV>`)
- Padding-aware loss computation
- Train / validation / test split
- Reproducible training setup
- Separate training and inference logic
- Model saving and loading for reuse

---

## Project Workflow
1. Environment setup and reproducibility
2. Dataset loading and DataFrame creation
3. Text preprocessing
4. Corpus construction
5. Tokenization and vocabulary building
6. Sequence generation using a sliding window
7. Padding and batching
8. Train, validation, and test split
9. LSTM model definition
10. Model training and validation
11. Model evaluation on test data
12. Next-word prediction (inference)
13. Model saving and loading

---

## Model Architecture
- **Embedding Layer**: Converts word indices to dense vectors
- **LSTM Layer**: Captures sequential and contextual information
- **Fully Connected Layer**: Outputs logits over the vocabulary

The model predicts the next word using the final hidden state of the LSTM.

---

## Loss Function and Optimization
- **Loss**: CrossEntropyLoss (padding tokens ignored)
- **Optimizer**: Adam
- **Framework**: PyTorch

---

## Inference
A reusable inference function is provided to:
- Accept raw input text
- Handle padding and `<OOV>` tokens
- Predict the next most probable word

---

## How to Run
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd next-word-prediction-lstm
