# Wan2GP on Google Colab

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Square-Zero-Labs/Wan2GP-on-Colab/blob/main/wan2gp-google-colab.ipynb)

## Overview

This repository provides a single Google Colab notebook that automates setting up the [Wan2GP](https://github.com/deepbeepmeep/Wan2GP) AI video generation platform in a fresh GPU-backed Colab runtime.

**Warning:** free Colab GPU runtimes usually provide only 15 GB of T4 VRAM, which is too small for most Wan2GP checkpoints; stick to the `Wan 2.2 TextImage2Video 5B FastWan` model and select 480p to run without memory errors.

Run the notebook top to bottom to clone Wan2GP, install all system and Python dependencies, and launch the Gradio interface from Colab.

## Notebook workflow

1. **Confirm GPU runtime** – prompts you to enable a GPU accelerator before continuing.
2. **Configure the workspace path** – adjust `WAN2GP_ROOT` if you want the Wan2GP checkout stored in a custom location.
3. **Download or update Wan2GP** – clones the upstream repository or pulls the latest changes when it already exists.
4. **Install system dependencies** – installs video and audio libraries required by Wan2GP.
5. **Install Python dependencies** – pins PyTorch + CUDA wheels compatible with current Colab runtimes and installs Wan2GP requirements.
6. **Launch Wan2GP** – starts the Gradio UI; keep the cell running while you interact with Wan2GP.

## Requirements

- Google account with access to Colab GPU runtimes (free tier works; paid tiers provide more VRAM).
- Stable internet connection while the setup cells run (downloads the Wan2GP repository and model weights).

## Tips

- Colab may time out inactive sessions; rerun the notebook from the top to rehydrate the environment.
- Keep the final cell running to maintain the public Gradio link; stopping it will terminate the interface.

## Contributing

Issues and pull requests are welcome. If you notice changes in Colab runtimes or Wan2GP dependencies, please open a PR so the notebook stays up to date.
