# ImageCaption

**ImageCaption** is a toy project aimed at learning and experimenting with image captioning—generating descriptive sentences from input images.

## Overview

This project is implemented using **PyTorch 2.0.1** and focuses on integrating computer vision with natural language processing. It uses a pre-trained image encoder and two optional text decoders: LSTM or GPT-style Transformer blocks.

## Dataset

The project uses the **Flickr30k** dataset available on Kaggle.

## Model Architecture

- **Image Encoder**: A pre-trained **ResNet-50** model is used. Its final classification layer is removed, and a linear layer is added to project the image features to match the word embedding dimension. The output embedding is used as the first token for the decoder.
  
- **Text Decoder**:
  - Option 1: LSTM
  - Option 2: Transformer encoder (simulating GPT using masked self-attention)

The models are implemented in `model.py`.

## System Requirements

- OS: Linux
- GPU: Nvidia Tesla V100-SXM2 with 32 GB memory
- CUDA Version: 11.7
- NVIDIA Driver Version: 515.65.01

## Configuration

All configuration parameters and hyperparameters are defined in `config.py`.

## Getting Started

### 1. Build Vocabulary

Run the following command to create the vocabulary:

```
python vocab.py
```
