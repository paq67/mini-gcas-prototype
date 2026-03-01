# Mini GACS Prototype — Mood & Style Embedding Pipeline

## Overview

This project implements a lightweight affective computing pipeline to analyze the **mood and stylistic similarity** of art and marketing visuals.

The system processes short videos, extracts frames, generates semantic embeddings using a pre-trained CLIP model, and computes similarity to identify visual mood relationships.

This prototype demonstrates the foundational workflow for a Creative Affective Computing System (GACS) aligned with GenTA’s vision.

---

## Dataset

The repository contains three short videos used as input:

* 14487894_3840_2160_24fps.mp4
* 5352609-hd_1080_1920_25fps.mp4
* 5738706-hd_1920_1080_24fps.mp4

These videos represent distinct visual styles to enable mood comparison.

---

## Pipeline Workflow

1. Load videos from the `data/` folder
2. Extract representative frames at fixed intervals
3. Compute CLIP embeddings for each frame
4. Normalize embeddings and run validation checks
5. Compute pairwise cosine similarity
6. Visualize similarity using a heatmap
7. Retrieve top-k similar frames

Frames and embeddings are generated dynamically and are not stored in the repository.

---

## Results Summary

The similarity heatmap reveals clear clustering patterns:

* Frames from the same video show high similarity
* Abstract visuals cluster due to shared colors and textures
* Lifestyle footage groups based on composition
* Nature scenes display consistent calm visual characteristics

These results indicate that embeddings capture perceptual mood rather than pixel similarity.

---

## Connection to GenTA

This pipeline demonstrates how embedding-based similarity can be used to:

* Generate a creative-level “vibe score”
* Enable similarity search for creatives
* Serve as features for predicting engagement metrics (CTR, ROAS)

---

## Repository Structure

```
mini-gacs-prototype/
│
├── notebook.ipynb
├── README.md
├── report.pdf
├── requirements.txt
│
└── data/
    ├── 14487894_3840_2160_24fps.mp4
    ├── 5352609-hd_1080_1920_25fps.mp4
    └── 5738706-hd_1920_1080_24fps.mp4
```

---

## Setup

Install dependencies:

```
pip install -r requirements.txt
```

---

## Running the Pipeline

1. Open `notebook.ipynb`
2. Run all cells sequentially
3. Outputs generated:

   * Extracted frames (temporary)
   * Embedding matrix
   * Similarity heatmap

---

## Verification Steps

The pipeline includes:

* Embedding shape validation
* NaN checks
* Self-similarity assertion
* File existence validation

These ensure robustness and reproducibility.

---


**Pavanadithya Karnan**

