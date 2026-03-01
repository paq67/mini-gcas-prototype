# Mini GACS Prototype - Mood & Style Embedding Pipeline

## Overview

This project implements a lightweight affective computing pipeline to analyze the **mood and stylistic similarity** of art and marketing visuals.

Using short videos as input, the system:

* Extracts representative frames
* Generates semantic embeddings using a pre-trained CLIP model
* Computes similarity across frames
* Visualizes mood clusters

This prototype demonstrates the foundation for a **Creative Affective Computing System (GACS)** aligned with GenTA’s vision of understanding the “feel” of visual content.

---

## Video Sources

The following royalty-free videos were used in this project:

1. **Abstract Visual Clip**
   `14487894_3840_2160_24fps.mp4`

2. **Lifestyle / Marketing Clip**
   `5352609-hd_1080_1920_25fps.mp4`

3. **Nature Cinematic Clip**
   `5738706-hd_1920_1080_24fps.mp4`


---

## Pipeline Steps

1. Upload videos via notebook
2. Extract frames at fixed intervals
3. Compute CLIP embeddings
4. Normalize vectors and validate outputs
5. Compute cosine similarity matrix
6. Visualize similarity heatmap
7. Retrieve top-k similar frames

---

## Results & Observations

The similarity heatmap reveals clear block-like clusters corresponding to each video source.

* Abstract visuals cluster due to shared color patterns and textures
* Lifestyle frames group based on scene composition and human presence
* Nature scenes show high internal similarity reflecting calm aesthetics

These results indicate that embeddings capture **perceptual mood** rather than pixel similarity.

---

## Connection to GenTA

This prototype demonstrates how embedding-based similarity can:

* Generate a **vibe score** for creatives
* Enable creative similarity search
* Serve as input features for predicting engagement metrics (CTR, ROAS)

---

## Repository Structure

```
mini-gacs-prototype/
│
├── notebook.ipynb
├── report.pdf
├── requirements.txt
│
├── data/
│   └── video_sources.md
│
├── frames/
├── embeddings/
```

---

## Setup

Install dependencies:

```
pip install -r requirements.txt
```

---

## How to Run

1. Open `notebook.ipynb`
2. Upload the video files when prompted
3. Run all cells
4. Outputs:

   * Extracted frames
   * Embedding matrix
   * Similarity heatmap

---

## Verification Steps

* Embedding shape validation
* NaN checks
* Self-similarity test
* File existence checks
---

## License

For research and evaluation purposes only.
Video assets belong to original creators.
