# 🧠 ADG-CLIP
CLIP Few Shot Adaptation on Flower102, Deep Learning course project

Authors: Filippo Adami, Alessandro De Vidi, Matteo Grisenti
Student IDs: 256149, 257845, 257855
Course: Deep Learning 2025

## 📘 Overview
This repository contains the implementation and experimental notebook for the ADG-CLIP project, developed for the Deep Learning 2025 course. The goal of the assignment is to improve the performance of a pre-trained Vision–Language Model (VLM) on the Oxford Flowers102 dataset, using Zero-Shot or Few-Shot techniques.

Our approach focuses exclusively on Zero-Shot learning, avoiding fine-tuning or dataset-specific training. Instead, we enhance CLIP’s reasoning and representation capabilities using two complementary strategies:

1. LLM-Generated Prompts
    - Prompts are automatically created using a Large Language Model that retrieves visual and semantic knowledge from the web.
    - This knowledge base is generated deterministically at runtime, ensuring reproducibility.
    - Since the web retrieval and synthesis process is computationally expensive, we precomputed and stored the results for this notebook.

2. Augmented Visual Inputs
    - Each test image is augmented at runtime using an optimized version of the Zero-1-to-3 diffusion model (arXiv:2303.11328 ).
    - The augmentations generate multiple views of each image, enriching CLIP’s visual understanding and improving similarity estimation.
    - Because each augmentation takes ~40 seconds per image on a T4 GPU (with CPU offload), we pre-generated the augmented dataset and host it on GitHub for direct download.


