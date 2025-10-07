---
title: 'Teaching AI to See Cancer: How Transformer Models Segment Prostate Tissue in Whole-Slide Images'
date: 2025-10-02
permalink: blog/prostate-fcbformer/
excerpt: "A look inside a transformer-based segmentation pipeline for prostate cancer detection from histopathology slides, balancing precision, interpretability, and reproducibility."
mathjax: true
tags:
  - Histopathology
  - Whole Slide Images
  - Transformer Models
  - Semantic Segmentation
  - Prostate Cancer
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

### 🧩 Why Segmenting Cancer Tissue Is So Hard

In digital pathology, each **whole-slide image (WSI)** of a biopsy can span several gigapixels — far too large for direct deep learning inference.  
To diagnose prostate cancer, pathologists rely on subtle differences in texture and gland morphology that AI models must learn to detect at **micron-level precision**.

Our recent project at the **University of Twente** focuses on this challenge: teaching AI to segment prostate tissue into four key categories, **background**, **stroma**, **benign glands**, and **tumour regions**, directly from *Hematoxylin and Eosin (H&E)* slides.

![Validation examples](/images/blogs/WSI_results_overlay.png)
*Figure: Model predictions overlaid on the corresponding WSIs to guide clinical decision-making.*

---

### ⚙️ The Idea: FCBFormer for Histopathology

We built on [**FCBFormer**](https://github.com/ESandML/FCBFormer), a transformer-based encoder–decoder architecture originally designed for polyp segmentation.  
The model fuses convolutional and transformer representations to capture both **local cellular structures** and **global tissue organisation**.

Key design components include:
- A **PVTv2-B3** backbone for multi-scale contextual learning.  
- A **residual convolutional branch** to preserve boundary details.  
- A **prediction head** that merges both to produce a 4-channel segmentation map.

---

### 🧮 Making Boundaries and Tumours Sharper

Beyond standard **Cross-Entropy** and **Dice Loss**, we introduced new regularisers that explicitly enforce geometric consistency:

- **Soft Boundary Dice Loss** - aligns predicted edges with gland boundaries.  
- **Dilated Dice Loss** - adds tolerance around small, irregular tumour or benign regions to boost recall.

The total objective was defined as:

$$
L_{total} = L_{CE} + L_{Dice} + \lambda_b L_{Boundary} + \lambda_t L_{TumourDilated} + \lambda_g L_{BenignDilated}
$$

with $\lambda_b = \lambda_t = \lambda_g = 0.7$ balancing the terms.

---

### 🧠 Training and Evaluation

- **Tiles:** $256 \times 256$ px with 64 px overlap to reduce border artefacts.  
- **Optimiser:** AdamW with adaptive learning rate decay.  
- **Augmentation:** mild rotations, flips, and colour jittering (Albumentations).  
- **Environment:** fully Dockerised with deterministic seeding and automatic checkpointing.

Training ran on a single GPU, logging per-epoch metrics for complete reproducibility.

---

### 📊 Results and Insights

The model achieved a **mean IoU of 0.71** across validation WSIs:

| Class | IoU |
|--------|-----|
| Background | 0.99 |
| Stroma | 0.91 |
| Benign | 0.52 |
| Tumour | 0.40 |

Despite modest tumour performance (limited data and imbalance), the model produced coherent segmentations with strong stroma delineation.

![Validation examples](/images/blogs/WSI_results.png)
*Figure: Model predictions vs. ground truth for prostate tissue segmentation.*

---


### 🧫 Why This Matters

Even partial automation can save pathologists significant time.  
By pre-highlighting suspicious gland regions, such models act as **assistive diagnostic tools**, not replacements.  
The qualitative overlays are especially useful for **annotation bootstrapping**,  speeding up dataset expansion for future supervised learning.

---

### 🚀 What’s Next

We plan to extend the framework with:
- **Multi-resolution learning** (low- and high-mag fusion).  
- **Self-supervised pretraining** on unlabelled WSIs.  
- **Multi-instance learning (MIL)** to link patch-level predictions to slide-level outcomes.

---

### 💻 Explore the Code

Implementation and training pipeline are available at:  
👉 [github.com/MuzammilAteo/HighRes-Histopathology-Semantic-Segmentation](https://github.com/MUZAMMILATEO/HighRes-Histopathology-Semantic-Segmentation)

</div>




</div>

<!-- Load MathJax for rendering inline and display math -->
<script>
  window.MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$', '$$'], ['\\[', '\\]']]
    },
    svg: { fontCache: 'global' }
  };
</script>
<script async id="MathJax-script" src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js"></script>

