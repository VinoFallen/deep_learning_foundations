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

---

## References
- [Neural Networks: Zero to Hero (Karpathy YouTube Series)](https://youtube.com/playlist?list=PLAqhIrjkxbuWI23v9cThsA9GvCAUhRvKZ&si=zQext0XwhtQW-XZk)
- [micrograd GitHub](https://github.com/karpathy/micrograd)
- [makemore GitHub](https://github.com/karpathy/makemore)
