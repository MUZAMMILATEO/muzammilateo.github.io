---
title: "Temporally-Constrained Monocular Endoscopic Tissue Reconstruction with Perceptually-Guided Depth Enhancement"
collection: publications
category: manuscripts
permalink: /publication/pis-depth-endoscopy/
excerpt: 'This paper presents a temporally-constrained framework for monocular endoscopic tissue surface reconstruction with perceptually-guided depth estimation, integrating deep learning and optimisation-driven techniques.'
date: 2025-06-30
venue: 'Engineering Applications of Artificial Intelligence (under review)'
slidesurl: 
paperurl: ''
bibtexurl: 
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">
Monocular endoscopy offers substantial benefits for patients but presents significant technical challenges, including **loss of depth perception**, **physiological tissue deformation**, **imprecise endoscope localisation**, **limited texture detail**, and a **constrained field of view**.  

To address these limitations, we propose a **temporally-constrained monocular tissue surface reconstruction framework** with perceptually-guided depth estimation, integrating both **deep learning-based** and **optimisation-driven** methodologies.  

The framework incorporates:  
- **Depth Anything** for generating Spatial Depth Estimates (SDEs) from sequential monocular endoscopic images.  
- A novel **Perceptual Image Similarity Depth (PIS-Depth) module**, which refines depth predictions using **Farneback optical flow** and **LPIPS maps**, mitigating artefacts from tissue deformation and motion.  
- A **Rotation-Translation Dog-Leg (RTDL) module**, performing \\( \mathcal{SO}(3) \\) optimisation followed by \\(\mathcal{SE}(3)\\) refinement via a dog-leg optimisation strategy, ensuring precise camera-tissue spatial alignment.  
- **Volumetric fusion** of refined depth and pose estimates using a Truncated Signed Distance Function (TSDF), followed by surface extraction via Marching Cubes to generate comprehensive **3D reconstructions**.  

Extensive validation on **HEVD, SCARED, C3VD, and in-house datasets** shows that our framework significantly outperforms state-of-the-art methods in intraoperative reconstruction **accuracy** and **robustness**.

</div>

<div style="text-align:justify; text-justify:inter-word; margin-top:15px; font-size:0.9em; font-style:italic;">
  <strong>Recommended citation:</strong> Muzammil Khan, Enzo Kerkhof, Matteo Fusaglia, Koert Kuhlmann, Theo Ruers, and Françoise J. Siepel. Temporally-Constrained Monocular Endoscopic Tissue Reconstruction with Perceptually-Guided Depth Enhancement. Engineering Applications of Artificial Intelligence (under review), 2025.
</div>


