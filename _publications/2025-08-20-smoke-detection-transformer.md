---
title: "Reliable Smoke Detection via Optical Flow-Guided Feature Fusion and Transformer-Based Uncertainty Modeling"
collection: publications
category: manuscripts
permalink: /publication/smoke-detection-transformer/
excerpt: 'This paper proposes an optical flow-guided and transformer-based framework for robust and uncertainty-aware smoke detection, integrating motion encoding with appearance cues for reliable early fire warning.'
date: 2025-08-20
venue: 'Fire Safety Journal (under review)'
slidesurl: 
paperurl: 'https://doi.org/10.48550/arXiv.2508.14597'
bibtexurl: 
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

**Fire outbreaks** remain one of the most pressing threats to human safety and infrastructure, underscoring the importance of **early and reliable smoke detection**. Unlike flames, **smoke exhibits complex spatiotemporal behaviour**, influenced by illumination, motion dynamics, and environmental variability, which challenges conventional detectors.  

This study introduces an **information-fusion framework** for smoke detection that combines **monocular appearance cues** with **optical flow-based motion encoding**. The main contributions include:  

- A **dual-phase fractional-order variational optical flow model**, inspired by the **four-colour theorem**, to preserve motion discontinuities and encode dynamic smoke plumes.  
- A **Gaussian Mixture Model fusion step** that integrates motion and appearance cues into binary smoke masks.  
- A **Two-Phase Uncertainty-Aware Shifted Windows Transformer**, trained first for **accurate smoke segmentation** and subsequently for **joint uncertainty modelling** (aleatoric + epistemic).  

By incorporating a **multi-scale uncertainty head**, the framework not only detects smoke but also estimates the **confidence** of its predictions, enhancing transparency and reliability.  

Extensive evaluations across benchmark datasets show that the proposed approach **outperforms state-of-the-art detectors**, providing a robust, uncertainty-aware solution for **surveillance, industrial safety, and autonomous monitoring systems**.  

</div>

<div style="text-align:justify; text-justify:inter-word; margin-top:15px; font-size:0.9em; font-style:italic;">
  <strong>Recommended citation:</strong> 'Nitish Kumar Mahala, Muzammil Khan, and Pushpendra Kumar. Reliable Smoke Detection via Optical Flow-Guided Feature Fusion and Transformer-Based Uncertainty Modeling. Fire Safety Journal (under review), 2025.
</div>
