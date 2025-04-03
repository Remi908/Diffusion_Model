Diffusion Model for MNIST
This project implements a denoising diffusion probabilistic model (DDPM) to generate handwritten digits from the MNIST dataset using a cosine-based noise schedule and a U-Net denoising architecture.

🔍 Key Features:
Dataset: MNIST — 28x28 grayscale digits (0–9)

Preprocessing:

Normalize image pixel values

Shuffle dataset for improved generalization

Forward Diffusion:

Adds Gaussian noise to images over multiple timesteps

Noise magnitude controlled using a cosine schedule

Reverse Denoising Process:

Learns to reconstruct clean images from noisy inputs

Uses U-Net with timestep embeddings for temporal awareness

Sampling:

Final generated image is obtained by reversing the noising process

Guided by learned denoising steps

🧠 Model Architecture:
U-Net with timestep conditioning to handle temporal information during denoising

No explicit class conditioning (i.e., this is unconditional generation)

⚙️ Training Details:
Gaussian noise added at every timestep during the forward process

Cosine schedule used to gradually vary noise over time

Loss: Typically MSE between predicted and actual noise at each timestep

📦 Output:
Generates realistic-looking handwritten digits by progressively denoising pure noise.
![image](https://github.com/user-attachments/assets/cb77e792-f9c6-46a4-8462-5f8c3699dd45)

