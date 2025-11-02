# deep-learning-project-few-shot
Implementation of a Few-Shot Adaptation method (based on CoOp/CoCoOp) to adapt pre-trained Vision-Language Models (CLIP) for fine-grained classification
# Few-Shot Adaptation using Vision-Language Models

This repository contains the official project for the "Deep Learning 2025" course at the University of Trento.

## 1. Project Goal

The primary objective of this project is to implement and analyze an advanced **Few-Shot Adaptation** method. The goal is to adapt a pre-trained Vision-Language Model (like **CLIP**) for a fine-grained classification task (the Oxford Flowers dataset) while preserving its ability to generalize to new, unseen classes (base-to-novel generalization).

## 2. Methodology

The implementation is based on the principles of **Parameter-Efficient Fine-Tuning (PEFT)** and **Prompt Learning**, inspired by state-of-the-art papers such as:
* **CoOp** (Learning to Prompt for Vision-Language Models)
* **CoCoOp** (Conditional Prompt Learning for Vision-Language Models)

The model is trained on a small subset of "base" classes (10 shots per class) and evaluated on its Top-1 Accuracy for both "base" and "novel" classes, using the Harmonic Mean as the final metric.

## 3. Technologies Used

* **Python 3.x**
* **PyTorch**
* **NumPy**
* **Pandas**
* **Matplotlib**
* **Jupyter Notebook** (run on Google Colab)

## 4. How to Run

The entire project is self-contained in the `[Deep_Learning_Few_Shot_Project.ipynb]` notebook.


**IMPORTANT: Compute Requirements**
Due to the computational demands of the models (e.g., CLIP ViT-B/16) and the dataset size, this project **cannot be executed on standard Google Colab instances** due to memory and server limitations.

Execution requires a high-performance environment with a dedicated GPU, such as an **Amazon Web Services (AWS) EC2 instance** or a similar cloud compute service.
