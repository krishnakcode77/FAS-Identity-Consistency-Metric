# Face Authenticity Score (FAS)
### A Reliability Metric for Identity Consistency in Diffusion-Generated Human Faces

## Overview

Recent diffusion-based image generation models can generate highly realistic human faces from textual prompts. However, evaluating the identity consistency and reliability of generated faces remains a major challenge.

This project introduces **Face Authenticity Score (FAS)**, a composite reliability metric designed to evaluate diffusion-generated synthetic human faces using:

- Identity similarity
- Detection confidence
- Image quality
- Generation stability

The framework combines deep face embeddings, cosine similarity analysis, machine learning verification, and trust calibration into a unified forensic-style evaluation system.

--

---

## Problem Statement

Although modern diffusion models produce photorealistic portraits, generated identities often lack consistency across multiple outputs.

This project addresses:

- Identity verification in synthetic faces
- Reliability analysis of diffusion-generated images
- Trustworthiness estimation for AI-generated human portraits
- Synthetic media forensic evaluation

---

## Proposed Face Authenticity Score (FAS)

The proposed reliability metric is defined as:

\[
FAS = 0.50S + 0.20C + 0.15Q - 0.15V
\]

Where:

- **S** = Identity similarity score
- **C** = Face detection confidence
- **Q** = Visual quality score
- **V** = Variance/instability penalty

The final score is normalized between **0 and 1**, where higher scores indicate stronger identity reliability.

---

## Features

- Synthetic face generation using diffusion models
- Face detection and embedding extraction
- Pairwise identity similarity computation
- Face Authenticity Score (FAS) estimation
- Logistic Regression verification model
- Interactive forensic-style dashboard
- Statistical visualization and analysis

---

## Dataset

A custom benchmark dataset of synthetic human faces was created using prompt-guided diffusion generation.

### Dataset Statistics

| Parameter | Value |
|---|---|
| Generated Images | 200 |
| Valid Face Samples | 156 |
| Pairwise Comparisons | 12,090 |

---

## Methodology

### 1. Synthetic Face Generation
- Prompt-guided diffusion image generation
- Controlled random seed variation
- Frontal human portrait generation

### 2. Face Detection & Embedding Extraction
- Deep face analysis models
- Identity embedding generation
- Invalid face filtering

### 3. Pairwise Similarity Analysis
Cosine similarity used for identity comparison:

\[
Sim(x,y)=\frac{x \cdot y}{||x|| ||y||}
\]

### 4. FAS Computation
Composite trust score integrating:
- Similarity
- Detection confidence
- Visual quality
- Stability

### 5. Supervised Verification
Balanced Logistic Regression classifier trained on:
- Matching identity pairs
- Non-matching identity pairs

### 6. Interactive Dashboard
Real-time:
- Face generation
- Similarity analysis
- FAS prediction
- Trust visualization

---

## Technologies Used

- Python
- Jupyter Notebook
- PyTorch
- Diffusers
- InsightFace
- OpenCV
- Scikit-learn
- NumPy
- Pandas
- Matplotlib
- Gradio

---

## Results

### Verification Performance

| Metric | Value |
|---|---|
| Accuracy | 1.00 |
| F1 Score | 1.00 |
| ROC AUC | 1.00 |

### Key Observations

- Mean cosine similarity: **0.222**
- Mean FAS score: **0.406**
- Most generated identities remained distinct
- Sparse high-similarity outliers indicated occasional recurrence

---

## Project Structure

```text
FAS-Identity-Consistency-Metric/
│
├── notebooks/
├── src/
├── dataset/
├── results/
├── report/
├── presentation/
├── README.md
├── requirements.txt
└── LICENSE
