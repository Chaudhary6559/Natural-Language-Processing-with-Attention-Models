# Question Answering

## Overview

This assignment explores **Question Answering using the T5 (Text-to-Text Transfer Transformer) architecture**. Building on the Transformer concepts introduced in the previous assignments, the project demonstrates how a pretrained Transformer can be adapted and fine-tuned for a specific natural language processing task.

The assignment covers preparation of the **C4 dataset**, text-to-text pretraining, tokenization and masking, T5 model initialization, and fine-tuning on the **SQuAD 2.0** question-answering dataset.

## Objectives

* Understand the structure and purpose of the C4 dataset.
* Prepare text data for Transformer pretraining.
* Implement tokenization and masking.
* Understand the text-to-text learning approach used by T5.
* Pretrain a Transformer model using a masked language modeling objective.
* Parse question-answer pairs from SQuAD 2.0.
* Fine-tune a T5 model for question answering.
* Implement a question-answering function using the fine-tuned model.

## Datasets

### C4 Dataset

The **Colossal Clean Crawled Corpus (C4)** is used to demonstrate the text-to-text pretraining process.

The assignment processes portions of the dataset and prepares masked text examples that can be used to train a Transformer model.

### SQuAD 2.0

The **Stanford Question Answering Dataset (SQuAD 2.0)** is used for fine-tuning the T5 model for question answering.

The dataset contains questions associated with passages of text and their corresponding answers.

## Methodology

### 1. C4 Data Preparation

* Load and inspect C4 text examples.
* Process the text into suitable training sequences.
* Convert tokenized data back into natural language when required.

### 2. Tokenization and Masking

Text sequences are tokenized and portions of the input are masked to create examples for the T5 pretraining objective.

```text id="k4n8ps"
Input Text
    │
    ▼
Tokenization
    │
    ▼
Mask Selected Tokens
    │
    ▼
Create Input / Target Pairs
    │
    ▼
T5 Pretraining
```

### 3. T5 Pretraining

A Transformer model is initialized and trained using the prepared C4 examples.

The assignment demonstrates the general process through which a text-to-text Transformer can learn from large-scale unlabeled text.

### 4. SQuAD 2.0 Preparation

Question-answer pairs are extracted from the SQuAD 2.0 dataset.

The data is organized into a text-to-text format suitable for fine-tuning T5.

```text id="p2v7jc"
Context + Question
       │
       ▼
   T5 Model
       │
       ▼
     Answer
```

### 5. Fine-Tuning

The T5 model is fine-tuned using question-answer examples from SQuAD 2.0.

Fine-tuning adapts the pretrained model to the specific task of generating answers from questions and their associated contexts.

### 6. Question Answering

After fine-tuning, the model receives a question and relevant context and generates an answer as text.

The assignment implements a question-answering function that uses the trained T5 model for inference.

## Key Concepts

* T5 (Text-to-Text Transfer Transformer)
* Transformer architecture
* Text-to-text learning
* Transfer learning
* Pretraining and fine-tuning
* C4 dataset
* SQuAD 2.0
* Tokenization
* Masked language modeling
* Sequence-to-sequence learning
* Generative question answering
* Natural language generation

## Workflow

```text id="v5x8rm"
             C4 Dataset
                 │
                 ▼
        Tokenization & Masking
                 │
                 ▼
       T5 Pretraining Objective
                 │
                 ▼
          Pretrained T5
                 │
                 ▼
        SQuAD 2.0 Dataset
                 │
                 ▼
         Fine-Tuning on QA
                 │
                 ▼
        Question Answering
                 │
                 ▼
          Generated Answer
```

## Technologies

* Python
* TensorFlow
* NumPy
* Jupyter Notebook

## Learning Outcomes

By completing this assignment, I gained practical experience with the **T5 text-to-text framework**, Transformer pretraining, token masking, transfer learning, and fine-tuning for question answering.

The assignment also provided hands-on experience preparing large-scale text data and adapting a pretrained generative Transformer to a downstream NLP task.

## Notebook

`Question_Answering.ipynb`

## Course Information

* **Course:** Natural Language Processing with Attention Models
* **Specialization:** Natural Language Processing
* **Platform:** Coursera
* **Assignment:** Question Answering

## Purpose

This project is part of my NLP learning portfolio and demonstrates practical experience with **T5, Transformer-based transfer learning, generative question answering, pretraining, and fine-tuning**.
