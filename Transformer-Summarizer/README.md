# Transformer Summarizer

## Overview

This assignment focuses on **text summarization using the Transformer architecture**. The model uses an encoder-decoder design based on attention mechanisms to transform longer input text into concise summaries.

The notebook provides the encoder implementation and guides the development of the decoder, allowing the complete Transformer architecture to be assembled and trained for summarization.

The assignment covers data preprocessing, positional encoding, masking, self-attention, encoder and decoder layers, Transformer construction, training, and generating summaries from text.

## Objectives

* Preprocess text data for Transformer-based summarization.
* Understand positional encoding.
* Implement scaled dot-product attention.
* Understand self-attention and causal attention.
* Work with attention masks.
* Understand Transformer encoder-decoder architectures.
* Implement Transformer decoder layers.
* Build a complete Transformer model.
* Train the model for text summarization.
* Generate summaries for input sentences.

## Methodology

### 1. Data Preparation

* Import the summarization dataset.
* Preprocess the input and target text.
* Prepare the data for Transformer-based training.

### 2. Positional Encoding

Since Transformers do not process sequences recurrently, positional information is incorporated into token representations.

Positional encoding provides the model with information about the position of each token in the input sequence.

### 3. Masking

Attention masks are used to control which tokens the model can access.

The assignment explores masking techniques required for handling padding and preventing the decoder from attending to future tokens during generation.

### 4. Self-Attention

The model uses scaled dot-product attention to determine which parts of a sequence are relevant when processing each token.

```text id="h3k1ps"
Query ──┐
Key ────┼──> Scaled Dot-Product Attention ──> Attention Output
Value ──┘
```

### 5. Encoder

The provided encoder processes the input text and generates contextual representations that are passed to the decoder.

The encoder is composed of Transformer layers that use self-attention and feed-forward transformations.

### 6. Decoder

The decoder generates the summary one token at a time.

It incorporates:

* Causal self-attention
* Encoder-decoder attention
* Feed-forward layers
* Residual connections
* Layer normalization

The main implementation work in this assignment focuses on the Transformer decoder.

### 7. Transformer

The encoder and decoder are combined to create a complete Transformer architecture.

```text id="w6a3pt"
Input Article
     │
     ▼
Input Embedding
     │
     ▼
Positional Encoding
     │
     ▼
Transformer Encoder
     │
     ▼
Encoder Representations
     │
     ├──────────────┐
     │              │
     ▼              │
Transformer Decoder │
     │              │
     ▼              │
Generated Tokens ◄──┘
     │
     ▼
Summary
```

### 8. Training

* Initialize the Transformer model.
* Prepare the training configuration.
* Train the model on article-summary pairs.
* Learn to generate concise summaries from longer text.

### 9. Summarization

After training, the model generates summaries by predicting the next token based on the input article and previously generated tokens.

The `next_word` functionality is used during the generation process.

## Key Concepts

* Transformer architecture
* Encoder-decoder models
* Self-attention
* Scaled dot-product attention
* Causal attention
* Positional encoding
* Attention masking
* Transformer decoder
* Cross-attention
* Residual connections
* Layer normalization
* Text summarization
* Autoregressive text generation

## Model Architecture

```text id="c5r9nx"
                INPUT ARTICLE
                     │
                     ▼
                Embedding
                     │
                     ▼
            Positional Encoding
                     │
                     ▼
          ┌─────────────────────┐
          │ Transformer Encoder │
          └─────────────────────┘
                     │
                     ▼
            Contextual Features
                     │
                     ▼
          ┌─────────────────────┐
          │ Transformer Decoder │
          │                     │
          │ Causal Self-Attn.   │
          │ Cross-Attention     │
          │ Feed-Forward        │
          └─────────────────────┘
                     │
                     ▼
             Next-Token Prediction
                     │
                     ▼
                  SUMMARY
```

## Technologies

* Python
* TensorFlow
* NumPy
* Jupyter Notebook

## Learning Outcomes

By completing this assignment, I gained practical experience with the core components of Transformer architectures and their application to text summarization. I practiced implementing attention mechanisms, positional encoding, masking, Transformer decoder layers, and an end-to-end encoder-decoder model.

## Notebook

`Transformer_Summarizer.ipynb`

## Course Information

* **Course:** Natural Language Processing with Attention Models
* **Specialization:** Natural Language Processing
* **Platform:** Coursera
* **Assignment:** Transformer Summarizer

## Purpose

This project is part of my NLP learning portfolio and demonstrates practical experience with **Transformer architectures, attention mechanisms, and neural text summarization**.
