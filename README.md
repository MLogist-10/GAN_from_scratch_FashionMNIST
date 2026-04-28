# GAN from Scratch — Fashion MNIST

A fully connected Generative Adversarial Network built from scratch in PyTorch, trained on the Fashion MNIST dataset.

## What it does
Generates synthetic fashion item images (clothing, shoes, bags) by training a Generator and Discriminator in an adversarial loop — no pretrained models, no convolutional layers, just raw GAN mechanics.

## Architecture
- **Generator:** Fully connected layers, takes random noise vector → outputs 28×28 image
- **Discriminator:** Fully connected layers, classifies real vs fake
- **Loss:** Binary Cross Entropy
- **Optimizer:** Adam for both networks

## Why fully connected?
Built this to understand GAN fundamentals from the ground up — FC layers keep the architecture transparent and easy to reason about. Outputs are slightly noisy, which is expected without convolutions. Next step would be a DCGAN with conv layers.

## Results
Outputs are recognizable fashion items but with some noise — a clear sign the model is learning structure but hasn't fully converged. Training longer or switching to a DCGAN architecture would sharpen results.

## Stack
- Python, PyTorch
- Fashion MNIST (via `torchvision.datasets`)

## Run it
Open the notebook end to end — no extra setup needed beyond PyTorch and torchvision.
