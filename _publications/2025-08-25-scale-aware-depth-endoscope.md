---
title: "Unifying Scale-Aware Depth Prediction and Perceptual Priors for Monocular Endoscope Pose Estimation and Tissue Reconstruction"
collection: publications
category: manuscripts
permalink: /publication/scale-aware-depth-endoscope/
excerpt: 'This paper introduces a framework that unifies scale-aware depth prediction with perceptual similarity priors for monocular endoscope pose estimation and tissue reconstruction.'
date: 2025-08-25
venue: 'IEEE Access (under review)'
slidesurl: 
paperurl: 'https://doi.org/10.48550/arXiv.2508.11282'
bibtexurl: 
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">
**Accurate localisation of endoscopes and reconstruction** of the surrounding tissue surface are critical for safer and more effective minimally invasive surgery. Traditional monocular approaches struggle with challenges such as depth ambiguity, tissue deformation, inconsistent camera motion, and limited visual texture.

To address these issues, we propose a unified framework that combines scale-aware depth prediction with perceptual refinement across time. Our method introduces:
- **MAPIS-Depth module**, which integrates state-of-the-art depth models (Depth Pro and Depth Anything) with advanced optimisation to generate pseudo-metric depth estimates. These estimates are then temporally refined using pixel correspondences and perceptual similarity, making the system more robust to tissue motion and deformation.
- For accurate _3D_ registration, we further develop the **WEMA-RTDL module**, ensuring consistent camera tracking and alignment.
- The reconstructed depth data are fused into detailed **_3D_ meshes of the surgical scene** using **Truncated Signed Distance Function (TSDF)** and **Marching Cubes**, providing a reliable spatial representation.

Evaluations on **benchmark datasets (HEVD and SCARED)** show that our framework outperforms existing methods, delivering more stable and precise reconstructions for monocular endoscopy.
</div>

<div style="text-align:justify; text-justify:inter-word; margin-top:15px; font-size:0.9em; font-style:italic;">
  <strong>Recommended citation:</strong> Muzammil Khan, Enzo Kerkhof, Matteo Fusaglia, Koert Kuhlmann, Theo Ruers, and Françoise J. Siepel.  
  Unifying Scale-Aware Depth Prediction and Perceptual Priors for Monocular Endoscope Pose Estimation and Tissue Reconstruction.  
  IEEE Access (under review), 2025.
</div>


