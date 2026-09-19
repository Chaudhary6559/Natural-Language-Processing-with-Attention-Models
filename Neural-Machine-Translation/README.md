# Neural Machine Translation

## Overview

This assignment focuses on building an **English-to-Portuguese Neural Machine Translation (NMT)** system using an encoder-decoder architecture with **Long Short-Term Memory (LSTM)** networks and an attention mechanism.

The attention mechanism allows the decoder to access relevant information from different parts of the input sequence during translation, helping the model handle longer sentences more effectively than a basic encoder-decoder architecture.

The model is implemented from scratch using TensorFlow and supports both **greedy decoding** and **Minimum Bayes Risk (MBR) decoding** for generating translations.

## Objectives

* Understand encoder-decoder architectures for neural machine translation.
* Implement an LSTM-based encoder.
* Implement cross-attention between the encoder and decoder.
* Build an LSTM-based decoder.
* Construct an end-to-end NMT model using TensorFlow.
* Train the translation model.
* Generate translations using greedy decoding.
* Implement Minimum Bayes Risk (MBR) decoding.
* Compare candidate translations using similarity-based evaluation.

## Dataset

The assignment uses paired **English and Portuguese sentences** for training and evaluating the neural machine translation model.

The text data is prepared and processed into sequences suitable for training the encoder-decoder architecture.

## Methodology

### 1. Data Preparation

* Load the English-Portuguese translation data.
* Process and prepare sentence pairs.
* Convert text into numerical representations.
* Prepare sequences for model training.

### 2. Encoder

The encoder processes the source English sentence and generates a sequence of hidden representations.

An LSTM is used to capture contextual information from the input sequence.

```text
English Sentence
       │
       ▼
Tokenization / Encoding
       │
       ▼
Embedding
       │
       ▼
LSTM Encoder
       │
       ▼
Encoder Representations
```

### 3. Cross-Attention

The attention mechanism connects the decoder to the encoder representations.

Instead of relying only on a single compressed representation of the input sentence, the decoder can focus on different parts of the source sentence when generating each target token.

```text
Encoder Representations
          │
          ▼
    Cross-Attention
          │
          ▼
       Decoder
          │
          ▼
 Portuguese Translation
```

### 4. Decoder

The decoder uses the attention information together with its recurrent state to generate the Portuguese translation token by token.

### 5. Translator

An end-to-end translator combines the encoder, attention mechanism, and decoder into a complete neural machine translation system.

### 6. Training

* Train the NMT model using TensorFlow.
* Learn relationships between English source sequences and Portuguese target sequences.
* Optimize the model to generate appropriate target-language tokens.

### 7. Inference

After training, the model generates translations from new English sentences.

The assignment explores **greedy decoding**, where the most probable next token is selected at each step.

### 8. Minimum Bayes Risk Decoding

The assignment also implements **Minimum Bayes Risk (MBR) decoding**.

MBR decoding evaluates multiple candidate translations and selects a translation based on its expected similarity to other candidate outputs.

The implementation uses overlap-based similarity measures to compare candidate translations.

## Key Concepts

* Neural Machine Translation (NMT)
* Encoder-decoder architecture
* Long Short-Term Memory (LSTM)
* Attention mechanisms
* Cross-attention
* Sequence-to-sequence learning
* TensorFlow model development
* Greedy decoding
* Minimum Bayes Risk (MBR) decoding
* Translation inference
* ROUGE-1 similarity
* Sequence overlap

## Model Architecture

```text
              English Input
                   │
                   ▼
              Embedding
                   │
                   ▼
              LSTM Encoder
                   │
                   ▼
        Encoder Hidden States
                   │
                   ▼
          ┌────────────────┐
          │ Cross-Attention│
          └────────────────┘
                   │
                   ▼
              LSTM Decoder
                   │
                   ▼
          Portuguese Tokens
                   │
                   ▼
          Generated Translation
```

## Technologies

* Python
* TensorFlow
* NumPy
* Jupyter Notebook

## Learning Outcomes

By completing this assignment, I gained practical experience building an encoder-decoder neural machine translation system with attention. I also practiced implementing LSTM-based sequence models, cross-attention, translation inference, greedy decoding, and Minimum Bayes Risk decoding.

## Notebook

`Neural_Machine_Translation.ipynb`

## Course Information

* **Course:** Natural Language Processing with Attention Models
* **Specialization:** Natural Language Processing
* **Platform:** Coursera
* **Assignment:** Neural Machine Translation

## Purpose

This project is part of my NLP learning portfolio and demonstrates practical experience with **attention-based sequence-to-sequence models and neural machine translation**.
