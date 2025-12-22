# Diffusion Models with Direct Feedback Alignment (DFA)

This repository contains the implementation of Diffusion Models trained with Direct Feedback Alignment (DFA), as part of the Master's Thesis research.
I investigate the biological plausibility of diffusion models by replacing Backpropagation (BP) with DFA in the U-Net training loop.

The original codes are the below "keiji-miura" GitHub pages. My codes are based with them.

https://github.com/keiji-miura/minDiffusionModel/blob/main/Minimum_diffusion_model_for_MNIST.ipynb
https://github.com/keiji-miura/FA-based_CNN_Autoencoder/blob/main/FA_CNN/FA_function.py

## Features
- Training Methods: Support for both Backpropagation (BP) and Direct Feedback Alignment (DFA).
- Model Architectures: Simple U-Net implementations (UNet1 & UNet2).
- Samplers: Includes DDPM, DDIM, DPM-Solver-2, and DPM-Solver++.
- Evaluation: Automatic calculation of FID, KID, and IS metrics using torch-fidelity.

## Requirements
- Python 3.11.5
- CUDA 11.8 (Recommended for GPU acceleration)

Install the required dependencies:

pip install -r requirements.txt

## Usage

Run the main script to start training or sampling. The script supports interactive input for configuration.

python main.py

Follow the on-screen instructions to select:
1. Num_Timesteps (e.g., 250, 1000) ...train_num_step
2. Training Mode (DFA or BP) ...Learning Rule
3. U-Net Version (1 or 2) ...U-Net Archtecture
4. Image Size (e.g., 8, 16) ...(image_size × image_size) 
5. Sampler (DDPM, DDIM, etc.) ...Sampler

## Reference
- Thesis: "生物学的に尤もらしい学習則を用いた拡散モデルの性能分析" (Performance Analysis of Diffusion Models using Biologically Plausible Learning Rules)
- Author: Kota Arakawa

## License
MIT License
