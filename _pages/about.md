---
layout: archive
title: "About Me"
permalink: /
author_profile: true
---
<!-- Theme-aware overrides for About/Contact boxes -->
<style>
  /* Dark mode via site toggle (data-theme) */
  html[data-theme="dark"] .about-box {
    background-color: rgba(20,20,20,0.9) !important;
    border-color: rgba(255,255,255,0.15) !important;
    color: #eee !important;
    box-shadow: 0 3px 8px rgba(255,255,255,0.05) !important;
  }
  html[data-theme="dark"] .about-box a { color: #aad4ff !important; }

  html[data-theme="dark"] .contact-box {
    background-color: rgba(40,40,40,0.9) !important;
    border-color: rgba(255,255,255,0.15) !important;
    color: #ddd !important;
  }

  /* Also support system dark mode if toggle not used */
  @media (prefers-color-scheme: dark) {
    .about-box {
      background-color: rgba(20,20,20,0.9) !important;
      border-color: rgba(255,255,255,0.15) !important;
      color: #eee !important;
      box-shadow: 0 3px 8px rgba(255,255,255,0.05) !important;
    }
    .about-box a { color: #aad4ff !important; }

    .contact-box {
      background-color: rgba(40,40,40,0.9) !important;
      border-color: rgba(255,255,255,0.15) !important;
      color: #ddd !important;
    }
  }

   /* Reduce bottom spacing on the About page */
  .about-box {
    margin-bottom: 0 !important;
    padding-bottom: 25px !important;
  }

  /* Remove bottom margin added by the theme’s content wrapper */
  .page__content {
    margin-bottom: 0 !important;
    padding-bottom: 0 !important;
  }

  /* Optional: tighten footer spacing */
  footer.page__footer {
    margin-top: 15px !important;
  }

</style>

<!-- Light/dark adaptive container -->
<div class="about-box" style="
  background-color: rgba(245, 245, 245, 0.95);
  border: 1px solid #ddd;
  border-radius: 12px;
  padding: 35px 45px;
  margin: 40px auto;
  max-width: 950px;
  box-shadow: 0 3px 8px rgba(0,0,0,0.05);
  text-align: justify;
  text-justify: inter-word;
  line-height: 1.65;
">

<div style="text-align:justify; text-justify:inter-word;" markdown="1">

I am a **Postdoctoral Researcher** at the **University of Twente**, The Netherlands, specialising in **AI-driven medical imaging** and **computer vision**.  
My work focuses on developing intelligent and interpretable algorithms for **tumour diagnosis**, **3D reconstruction**, and **image-guided surgery** using data from **MRI**, **CT**, **X-ray**, **histopathology**, and **endoscopy**. I completed my **PhD in Computer Vision and Machine Learning**.

My broader research interests include:
- Medical image analysis and _3D_ reconstruction  
- Explainable and uncertainty-aware AI  
- Multi-modal data fusion and instance learning  
- Visual SLAM and scene understanding for surgical navigation  

I am proficient in **PyTorch**, **TensorFlow**, **Docker**, and **MLflow**, and experienced in building scalable AI pipelines for research and clinical use.  
I have presented my work at more than **ten international conferences** and actively contribute to collaborative projects on **AI for early disease detection**.

Beyond research, I also enjoy **teaching and mentoring** students in **Python programming**, **image processing**, and **machine learning**, and have supervised multiple **Technical Medicine** projects in collaboration with the **Netherlands Cancer Institute** and **Princess Máxima Centre**.

### Collaborations
I have collaborated with clinical and research partners across The Netherlands and Europe, including:
- **Netherlands Cancer Institute – Antoni van Leeuwenhoek (NKI-AVL)**  
- **Princess Máxima Centre for Paediatric Oncology**  
- **Radboud University Medical Centre (Radboud UMC)**  
- **Andros Clinics**  
- **University of Twente - Robotics and Mechatronics (RaM) Group**  
- **European research consortia under Horizon Europe and NWO programmes**

These collaborations have focused on combining **AI**, **robotics**, and **medical imaging** to support **minimally invasive and image-guided surgery**.

---

</div>

<div class="contact-box" style="
  background-color:#f7f7f7;
  border:1px solid #ddd;
  border-radius:10px;
  padding:15px 20px;
  margin-top:25px;
  font-size:0.9em;
  font-style:italic;
  box-shadow:0 2px 5px rgba(0,0,0,0.05);
" markdown="1"> 
  
### 📬 Contact Me
- ✉️ **Personal Email:** [khanm2004@gmail.com](mailto:khanm2004@gmail.com)  
- 📧 **UT Email:** [m.khan@utwente.nl](mailto:m.khan@utwente.nl)  
- 📍 **Location:** Enschede, The Netherlands
</div>

</div>
