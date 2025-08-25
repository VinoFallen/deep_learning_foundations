# Deep Learning Foundations  

This repository documents my learning journey in Deep Learning foundations, inspired by Andrej Karpathy’s **Neural Networks: Zero to Hero** series.  
Each folder contains a progressively more complex neural network implementation built from scratch. From Micrograd, then Makemore to finally GPT.

---

## [Folder 1: Neural Network From Scratch](./nn_from_scratch/)  
- A simple 1-layer NN with 2 neurons and 2 input features.  
- Implements forward pass and basic training with gradient descent.

---

## [Folder 2: NN: Zero to Hero - Micrograd](./zero-hero/micrograd)  
- Reimplementation of Karpathy’s **Micrograd**.  
- Micrograd is a very small autograd engine. It implements Backpropagation using a custom class `Value` which can only use scalar values.    
- Demonstrates how modern frameworks like PyTorch/TensorFlow handle automatic differentiation.  
- Includes a small 2-layer MLP built with Micrograd.

---

## [Folder 3: NN: Zero to Hero - Makemore](./zero-hero/makemore)  
- Reimplementation of Karpathy’s **Makemore** character-level language model.  
- **Part 1: Bigrams**
  - Bigram character-level model:
    1. Counting bigrams → probability-based generation.  
    2. Neural network with one-hot encoding + weight matrix.  
  - We learn that a Neural Network architecture is more scalable.  
  - Finally, when we sample from the mode,l the names obtained are still not usable. We need to continue to improve the neural network - an MLP, in part 2.  
- **Part 2: MLP**
  - Replace the single linear layer with a multi-layer perceptron (MLP).
  - Use embeddings instead of raw one-hot vectors for characters.
  - Add non-linearity (tanh).
  - Model now captures more context beyond simple bigram statistics.
  - Results: Generated names start to look more realistic and diverse, though still imperfect.
- **Part 3: Activations, BatchNorm, Initialization**
  - Introduce Batch Normalization to stabilize training
  - Importance of weight initialization → prevents exploding/vanishing gradients.
  - Better training dynamics and faster convergence.
  - Results: Clear improvement in generated samples.
- **Part 4: Becoming a Backprop Ninja**
  - Deep dive into backpropagation mechanics:
    - Manual gradient calculations.
    - Efficient vectorized implementations.
    - Understanding the computational graph at a deeper level.
  - How to debug, verify, and optimize backprop.
  - Takeaway: Backprop is just careful application of the chain rule.
  - Builds intuition needed for Transformers.

- **Part 5: Building a WaveNet**
  - Extend the context window size beyond bigrams (larger n-gram models).
  - Use architectures inspired by WaveNet: stacked layers with wider receptive fields.
  - Model begins to capture long-range dependencies in character sequences.
  - Result: Generated names are much more coherent, with structure closer to real data.
  - Takeaway: Scaling depth + context naturally leads into sequence models like RNNs, CNNs, and ultimately Transformers.
---

## References
- [Neural Networks: Zero to Hero (Karpathy YouTube Series)](https://youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ&si=zQext0XwhtQW-XZk)
- [micrograd GitHub](https://github.com/karpathy/micrograd)
- [makemore GitHub](https://github.com/karpathy/makemore)
