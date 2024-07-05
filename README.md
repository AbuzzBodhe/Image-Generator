# Deforum Stable Diffusion Setup and Rendering Script

This repository contains a script to set up an environment and run a stable diffusion model using the Deforum Stable Diffusion repository. It configures various settings and parameters for the model, handles environment setup, and dispatches different rendering tasks based on user input.

## Features

- **Environment Setup**: Installs required packages and clones the Deforum Stable Diffusion repository.
- **Model Configuration**: Supports various model configurations and checkpoints.
- **Animation Parameters**: Extensive settings for 2D, 3D, and video-based animations.
- **Image Generation**: Generates images based on prompts with support for CLIP and aesthetics guidance.
- **Memory Optimization**: Cleans up unused memory for optimized performance.
- **Customizable Settings**: Load settings from a file and adjust parameters as needed.

## Requirements

- Python 3.7+
- Required Python packages listed in the script

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/deforum-stable-diffusion-setup.git
    cd deforum-stable-diffusion-setup
    ```

2. Ensure you have the required Python packages. You can use the provided `setup_environment` function within a Google Colab notebook or manually install the packages:
    ```sh
    pip install xformers==0.0.27.dev841 einops==0.4.1 pytorch-lightning==1.7.7 torchdiffeq==0.2.3 torchsde==0.2.5 ftfy timm transformers open-clip-torch omegaconf torchmetrics==0.11.4 safetensors kornia accelerate jsonmerge matplotlib resize-right scikit-learn numpngw pydantic
    ```

3. Download or clone the Deforum Stable Diffusion repository:
    ```sh
    git clone -b 0.7.1 https://github.com/deforum-art/deforum-stable-diffusion.git
    ```

## Usage

### Setup Environment

The script includes a function `setup_environment()` that installs the necessary packages and clones the Deforum Stable Diffusion repository if running in Google Colab.

### Configure Paths

The `PathSetup` function sets up paths for models, configs, and outputs, with an option to mount Google Drive for storing models and outputs.

### Configure Model

Use the `ModelSetup` function to configure the model's location and version, including options for custom configurations and checkpoints.

### Animation and Image Generation

- Define animation parameters using the `DeforumAnimArgs` function.
- Define image generation parameters using the `DeforumArgs` function.
- Load prompts for image generation.
- Dispatch rendering tasks based on the selected animation mode.

