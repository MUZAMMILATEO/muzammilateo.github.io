---
title: ""Leveraging Mixed Data CNN-LSTM with Fractional Order Optical Flow for Early Fire Detection and XAI-Guided Segmentation"
collection: publications
category: manuscripts
permalink: /publication/fire-detection-cnnlstm/
excerpt: 'This paper proposes a hybrid CNN-LSTM model combined with fractional-order optical flow for early fire detection, fusing static and dynamic features of fire to improve detection and localisation.'
date: 2025-06-30
venue: 'Engineering Applications of Artificial Intelligence (under review)'
slidesurl: 
paperurl: 'http://dx.doi.org/10.2139/ssrn.5372325'
bibtexurl: 
---

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

**Fire outbreaks** pose a severe risk to human life and property, with causes ranging from **electrical faults and cooking accidents** to **natural disasters and negligence**. Their **unpredictable and fast-spreading nature** makes early detection critical for prevention and mitigation.  

This work introduces a **novel hybrid framework** for **early fire detection**, leveraging both **static features** (colour, shape, texture) and **dynamic features** derived from **segmentation-based fractional-order optical flow**. The contributions include:  

- A **mixed data preparation strategy**, where each training sample pairs a reference image with its corresponding sequence of **4D fire descriptors** (mean flow, weighted flow, sink/source matching, flow variance).  
- A **lightweight CNN-LSTM model** designed to fuse static and dynamic cues for robust classification and localisation of fire.  
- Integration of **explainable AI (XAI)-guided segmentation**, providing interpretable fire regions to support trust in AI predictions.  

The proposed system demonstrates strong **early detection capabilities**, outperforming existing state-of-the-art methods. Extensive **ablation studies** highlight the significance of each module, confirming the effectiveness of combining CNN, LSTM, and fractional-order optical flow within a unified framework.  

</div>

<div style="text-align:justify; text-justify:inter-word; margin-top:15px; font-size:0.9em; font-style:italic;">
  <strong>Recommended citation:</strong> Muzammil Khan, Nitish Kumar Mahala, and Pushpendra Kumar. Leveraging Mixed Data CNN-LSTM with Fractional Order Optical Flow for Early Fire Detection and XAI-Guided Segmentation. Engineering Applications of Artificial Intelligence (under review), 2025.
</div>
