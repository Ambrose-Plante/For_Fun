# The Annotated _Attention is All You Need_

## Overview

This is an educational/reference implementation of the original encoder-decoder Transformer rather than a project-specific music model. It defines embeddings, positional encoding, multi-head attention, residual sublayers with normalization, position-wise feed-forward networks, stacked encoders, stacked decoders, masking, and an output generator. The encoder builds contextual source representations, while the decoder uses masked self-attention and encoder-decoder attention to autoregressively construct target representations. Training utilities implement batching, masking, optimization, and sequence-learning support around those modules. PyTorch's modern Transformer documentation identifies the same encoder/decoder architecture as the original Transformer design, providing an external reference for the concepts embodied by the notebook. 8

## Algorithmic workflow

1. Embed tokens
2. Add positions
3. Repeated self-attention/feed-forward encoder
4. Masked decoder + cross-attention
5. Output projection/softmax
6. Sequence training
