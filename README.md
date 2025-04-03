🧠 Contextual Diffusion Model for MNIST
This project implements a conditional diffusion model using a Contextual U-Net architecture to generate handwritten digits from the MNIST dataset.

🔍 Key Features:
Dataset: 28x28 grayscale MNIST images (digits 0–9)

Architecture: U-Net enhanced with residual convolution blocks

Conditional Generation: Class-conditioned via Classifier-Free Guidance and context masking

Diffusion Process:

Forward Diffusion: Adds Gaussian noise using a linear beta schedule

Reverse Process: Learned by the model using MSE loss

Sampling Control: guide_w allows adjustment of how strongly the output aligns with the target class

Optimizer: Adam with linearly decaying learning rate

Data Pipeline:

Normalize and convert images to tensors

Batch and shuffle (batch size = 256)

One-hot encode class labels

📦 Output:
Generates MNIST-like digit images conditioned on target classes with adjustable guidance strength.
