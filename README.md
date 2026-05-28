# diffusion-soc-2026
SoC 2026 — Diffusion Models from Scratch
# Week 1 — MNIST Classification

**Mentee:** Yashwanth
**SoC Track:** Diffusion Models from Scratch — SoC 2026

## Final results
- **Test accuracy:** 98.12%
- **Best validation accuracy:** 98.12% at epoch 10
- **Final train loss:** 0.0400

## Design choices
- **Architecture:** MLP — 784 → 256 → 256 → 10, ReLU activations, Dropout(0.2)
- **Optimizer:** Adam with lr=1e-3
- **Batch size:** 128
- **Epochs trained:** 10
- **Validation split:** 10% of training data, seed=42

## What I learned
This week I learned what the training loop actually does step by step.
loss.backward() computes gradients through backpropagation and optimizer.step()
uses them to update the weights. I also learned that a Dataset class just needs
to answer two questions: how many samples exist, and give me sample number idx.

## What I'd do differently
Try a CNN architecture next time since it uses the spatial structure of images
rather than flattening them, and would likely reach higher accuracy faster.

## How to reproduce
1. Open week1_mnist.ipynb in Colab with a T4 GPU runtime.
2. Run all cells top to bottom.
3. Checkpoint saves automatically to best_model.pt.
