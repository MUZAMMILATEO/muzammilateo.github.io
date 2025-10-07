---
title: 'Making AI Explain Its Confidence: Inside the ELAAI Framework for Tumour Prediction'
date: 2024-10-11
permalink: blog/elaai-framework/
excerpt: "How our Explainable and Likelihood-Aware AI (ELAAI) framework improves tumour prediction in MRI scans while ensuring transparency and clinical trust."
mathjax: true
tags:
  - Medical Imaging
  - Explainable AI
  - MRI
  - Deep Learning
  - Uncertainty
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

### 🧠 Understanding the Challenge
Bladder tumours are difficult to detect early because MRI scans contain vast, complex structures that vary widely among patients.  
AI has shown promise, but most models struggle with *limited annotated data* and a lack of *transparency*, clinicians cannot always understand *why* a model flags a region as abnormal.

### 💡 Introducing the ELAAI Framework
In our recent study from the **University of Twente**, we developed the **Explainable and Likelihood-Aware AI (ELAAI)** framework to make tumour detection both *data-efficient* and *interpretable*.

![ELAAI Overview](/images/blogs/elaai_overview.png)
*Figure: Simplified overview of the ELAAI workflow.*

ELAAI is built on three pillars:

1. **MFA-Net** - a *multi-scale feature aggregation* network that learns bladder anatomy from *normal* MRI scans, reducing the need for tumour-labelled data.  
2. **Refinement Step** - a *knowledge-driven algorithm* that sharpens boundaries and identifies small wall irregularities.  
3. **SLIP-Net** - a *vision transformer-based network* that converts spatial deformation between MRI slices into *pixel-level tumour likelihood maps*.

Together, they provide not only segmentation but also *confidence maps* — visualising *how certain* the AI is about each prediction.

### ⚙️ Key Technical Insight
The core idea is to learn anatomy, not pathology.  
By modelling *what “normal” looks like*, ELAAI detects *deviations* that might indicate tumour onset, even when explicit tumour annotations are scarce.

For example, our deterministic uncertainty module computes:

$$
U_{map} = \mathcal{N}\big( \text{var}(\theta) + \text{var}(M) \big)
$$

where $\theta$ and $M$ represent phase and magnitude variations of inter-slice deformations.  
This allows pixel-level tumour likelihood estimation, effectively quantifying *where* and *how confidently* the model sees abnormalities.

### 🔬 Results in Brief
ELAAI achieved a **Dice score of 0.91** on bladder segmentation and outperformed five state-of-the-art baselines such as **PRANet, HarDNet, and FCBFormer**.  
It was also more robust to noise and low-contrast MRI scans, demonstrating strong generalisation across different patient anatomies.

![Results comparison](/images/blogs/elaai_results.png)
*Figure: ELAAI vs. other likelihood prediction frameworks on bladder MRI scans.*

### 🩺 Why It Matters
The framework enhances **clinical trust** by making predictions explainable and by highlighting *how uncertain* the model is.  
This means clinicians can interpret tumour likelihood maps as *confidence-weighted guidance*, not just binary outputs.

### 🔗 Code and Reference
The complete implementation is available at  
👉 [github.com/MuzammilAteo/ELAAI](https://github.com/MuzammilAteo/ELAAI)

> _This post summarises the follwoing research as:_  
> Khan M., de Groot A.G., Cornel E.B., van der Heijden A.G., Siepel F.J.  
> “Explainable and Likelihood-Aware AI Framework for MRI-Based Pixel-Level Bladder Tumour Prediction,” 2024.

</div>
