# Mini GPT from Scratch using PyTorch

A character-level Generative Pre-trained Transformer (GPT) built and trained from scratch using PyTorch. This project demonstrates the fundamental architecture behind modern Large Language Models (LLMs).

## Project Overview

This project implements a small GPT model trained on Shakespeare's text to predict the next character and generate Shakespeare-like text.

The model is built without using pre-built Transformer architectures, providing a practical understanding of how GPT works internally.

## Features

- Character-level tokenization
- Token and positional embeddings
- Self-attention mechanism from scratch
- Causal masking to prevent future-token access
- Multi-head attention
- Feed-forward neural networks
- Transformer blocks with residual connections and layer normalization
- Next-character prediction using cross-entropy loss
- Model training using the AdamW optimizer
- Text generation using temperature, top-k and top-p sampling

## Technologies Used

- Python
- PyTorch
- Google Colab
- Jupyter Notebook
- Git and GitHub

## Model Architecture

The GPT model consists of:

1. Token Embeddings
2. Positional Embeddings
3. Three Transformer Blocks
4. Four Attention Heads per Block
5. Feed-Forward Networks
6. Final Layer Normalization
7. Linear Output Layer

## Training Configuration

| Parameter | Value |
|---|---:|
| Vocabulary size | 65 |
| Context length | 32 |
| Embedding dimension | 64 |
| Attention heads | 4 |
| Transformer layers | 3 |
| Batch size | 16 |
| Training iterations | 400 |
| Total parameters | 159,937 |

## Training Results

The model's loss decreased during training:

| Step | Training Loss | Validation Loss |
|---|---:|---:|
| 0 | 4.409 | 4.409 |
| 100 | 2.518 | 2.517 |
| 200 | 2.366 | 2.367 |
| 300 | 2.275 | 2.287 |
| 400 | 2.209 | 2.177 |

This demonstrates that the model learned patterns in the training text and improved its next-character predictions.

## Text Generation

The model generates text one character at a time using autoregressive sampling.

Generation can be controlled using:

- **Temperature:** Controls randomness.
- **Top-k:** Restricts sampling to the k most likely characters.
- **Top-p:** Uses cumulative probability to select likely characters.

## How to Run

1. Open the notebook in Google Colab.
2. Ensure `shakespeare.txt` is available in the working directory.
3. Run the notebook cells in order.
4. Train the GPT model.
5. Experiment with different text-generation settings.

## Learning Outcomes

Through this project, I explored:

- How tokenization works.
- How self-attention learns relationships between tokens.
- Why causal masking is important in GPT.
- How Transformer blocks are structured.
- How neural networks learn through backpropagation.
- How decoding strategies influence generated text.

## Future Improvements

- Train on a custom dataset.
- Experiment with larger model architectures.
- Implement Byte Pair Encoding (BPE).
- Improve text-generation quality through longer training.

---

**Built with Python and PyTorch.**
