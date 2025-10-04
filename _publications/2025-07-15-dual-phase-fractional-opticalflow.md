---
title: "Dual-Phase Level Set-Driven Fractional Order Variational Model for Motion Estimation Leveraging the Four-Color Theorem"
collection: publications
category: manuscripts
permalink: /publication/dual-phase-fractional-opticalflow/
excerpt: 'This paper introduces a dual-phase level set-based fractional order variational model for motion estimation, leveraging the four-color theorem to improve optical flow robustness and boundary representation.'
date: 2025-07-15
venue: 'Applied Mathematical Modelling (under review)'
slidesurl: 
paperurl: ''
bibtexurl: 
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

**Motion estimation**, often addressed via **optical flow**, is a cornerstone of computer vision. Yet, existing optical flow techniques struggle to preserve **dense but discontinuous flow fields** while maintaining robustness against **outliers**.  

This work proposes a **dual-phase level set segmentation-based fractional-order variational model** for optical flow estimation, extending beyond traditional single-level set and integer-order formulations. The model is characterised by:  

- A **robust \\(L_{1}\\)-norm data fidelity term**, enhancing resilience to noise and outliers.  
- A **Marchaud fractional derivative-based regularisation term**, exploiting the non-local properties of fractional calculus to better handle textures and sharp discontinuities.  
- A novel **four-colour-theorem-inspired dual-phase level set design**, applied directly to optical flow fields (not images), which eliminates overlap/vacuum issues and provides accurate boundary representations in complex topologies.  

The optimisation is solved using a **primal-dual algorithm** with **Legendre-Fenchel transforms**, while fractional derivatives are discretised via the **Grünwald–Letnikov scheme**. Gradient descent iterations ensure convergence.  

Experiments across **31 benchmark image sequences** demonstrate that the proposed method achieves **higher accuracy, robustness, and boundary fidelity** than existing state-of-the-art optical flow approaches.  

</div>

<div style="text-align:justify; text-justify:inter-word; margin-top:15px; font-size:0.9em; font-style:italic;">
  <strong>Recommended citation:</strong> Nitish Kumar Mahala, Muzammil Khan, and Pushpendra Kumar. Dual-Phase Level Set-Driven Fractional Order Variational Model for Motion Estimation Leveraging the Four-Color Theorem. Applied Mathematical Modelling (under review), 2025.
</div>


