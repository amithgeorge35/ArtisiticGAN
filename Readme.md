# Artistic GAN – Generating Creative Artwork with Deep Learning

## Overview
This project implements a **Generative Adversarial Network (GAN)** to generate **artistic images** by learning patterns, textures, and styles from a dataset of artwork.  
The goal is to explore how adversarial training can be used for **creative image synthesis**, demonstrating core deep learning concepts such as generator–discriminator competition, latent space sampling, and convergence behavior.

---

## Project Highlights
- Implemented a **Generative Adversarial Network (GAN)** from scratch
- Trained a **Generator** to synthesize artistic images from random noise
- Trained a **Discriminator** to distinguish real artwork from generated images
- Visualized generated samples across training epochs
- Demonstrated understanding of **deep learning training dynamics**

---

## Model Architecture

### Generator
- Takes a random latent vector as input
- Uses fully connected / convolutional layers (depending on implementation)
- Upsamples noise into an image representation
- Uses activation functions such as ReLU and Tanh

### Discriminator
- Takes an image as input (real or generated)
- Uses convolutional / dense layers to extract features
- Outputs a probability indicating real vs fake
- Trained using binary cross-entropy loss

The two networks are trained **adversarially**, improving each other over time.

---

## Dataset
- Collection of artistic or stylized images
- Images are resized and normalized before training
- Dataset is used to learn visual patterns and artistic structure

*(Dataset details can be updated based on the exact source used.)*

---

## Training Process
1. Sample random noise vectors
2. Generate synthetic images using the Generator
3. Train the Discriminator on:
   - Real artwork images
   - Generated (fake) images
4. Train the Generator to fool the Discriminator
5. Repeat over multiple epochs until convergence

Generated images are periodically saved to monitor training progress.

---

## Results
- The Generator progressively learns meaningful artistic patterns
- Image quality improves over training epochs
- Early epochs show noisy outputs; later epochs capture structure and style

Sample outputs can be found in the project notebook or output directory.

---

## Files
- **Untitled20.ipynb** – Jupyter Notebook containing model definition, training loop, and visualizations
- **README.md** – Project documentation

---

## Requirements
- Python 3.x
- Required libraries:
  - numpy
  - matplotlib
  - tensorflow / pytorch (depending on implementation)
  - keras (if using TensorFlow/Keras)

Install dependencies using:
```bash
pip install -r requirements.txt
