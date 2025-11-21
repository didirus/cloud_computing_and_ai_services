# Cloud Computing - Google Cloud Platform Workshop

A hands-on tutorial in Dutch, for learning cloud computing concepts with Google Cloud Platform. This project teaches GCP fundamentals through practical exercises with Vertex AI, the Gemini API, Linux CLI, and PyTorch.

## Overview

This workshop walks you through working with Google Cloud Platform services. You'll learn to:

- Set up and navigate GCP environments
- Use the Gemini API via Vertex AI for generative AI tasks
- Work with Linux command line on cloud VMs
- Train neural networks with PyTorch on cloud infrastructure
- Interact with Cloud Storage buckets

## Prerequisites

- Python 3.8+
- Google Cloud Platform account with Vertex AI enabled
- Basic knowledge of Python
- Jupyter Notebook or Google Cloud Workbench

## Setup Instructions

1. **Clone/download this repository**

2. **Create a virtual environment** (recommended):
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Configure environment variables**:
   - Copy `.env.example` to `.env`
   - Fill in your GCP project details and credentials

5. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```

6. **Open the relevant notebook** (see below)

## Notebooks Guide

### 1. [opdrachten/gemini.ipynb](opdrachten/gemini.ipynb)
**Vertex AI & Gemini API** - Learn to work with Google's generative AI.

**What you'll learn:**
- Making your first Gemini API call
- Controlling output with temperature and max_output_tokens
- Getting structured JSON output from LLMs
- Analyzing images with multimodal AI
- Retrieving and analyzing data from Cloud Storage buckets
- Error handling and safety settings

**Best for:** Students who want to learn about generative AI in the cloud.

### 2. [opdrachten/linux_shell.ipynb](opdrachten/linux_shell.ipynb)
**Linux CLI Basics** - Essential command line skills for cloud environments.

**What you'll learn:**
- Navigating the filesystem (ls, cd, pwd)
- File operations (touch, cp, mv, rm)
- Creating and editing files (echo, cat)
- Searching with grep
- System information (ps, htop, df)
- Shell scripting basics

**Best for:** Students new to Linux who need CLI skills for cloud VMs.

### 3. [opdrachten/pytorch.ipynb](opdrachten/pytorch.ipynb)
**PyTorch Neural Networks** - Train a simple neural network on cloud infrastructure.

**What you'll learn:**
- Loading and exploring the MNIST dataset
- Building a feedforward neural network
- Understanding loss functions and optimizers
- Training loops and epochs
- Evaluating model performance
- Experimenting with hyperparameters

**Best for:** Students interested in machine learning on cloud GPUs.

## Solutions

The [uitwerkingen/](uitwerkingen/) directory contains complete solutions:
- `linux_shell_uitwerkingen.ipynb` - Solutions for Linux CLI exercises
- `pytorch-uitwerkingen.ipynb` - Solutions for PyTorch exercises

## Documentation

The [docs/](docs/) directory contains supplementary materials:
- `cloud_concepten.md` - Overview of 20 fundamental cloud concepts
- `gcp_setup.md` - Detailed GCP setup instructions

## Key Concepts Covered

1. **Cloud Computing** - On-demand compute, storage, and services
2. **Vertex AI** - Google's managed ML platform
3. **Generative AI** - Using LLMs via API (Gemini)
4. **Cloud Storage** - Object storage with buckets
5. **Virtual Machines** - Linux VMs in Compute Engine
6. **Neural Networks** - Deep learning fundamentals with PyTorch

## Troubleshooting

**Issue:** `ModuleNotFoundError` when running notebooks
- **Solution:** Make sure you activated the virtual environment and installed requirements

**Issue:** Authentication errors with GCP
- **Solution:** Verify your `.env` file has correct credentials and your GCP project has Vertex AI enabled

**Issue:** Cannot connect to VM via SSH
- **Solution:** Check that your VM instance is running in Compute Engine

**Issue:** PyTorch training is slow
- **Solution:** Consider using a GPU-enabled VM or Google Colab for faster training

## License

This educational material is provided for learning purposes.
