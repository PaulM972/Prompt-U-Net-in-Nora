# Prompt U-Net: Clinician-Guided AI for Context-Aware Segmentation 

[![Live Demo](https://img.shields.io/badge/Demo-Launch%20in%20Browser-green?style=for-the-badge)](https://www.nora-imaging.com/)
[![Status](https://img.shields.io/badge/Paper-Preprint-blue?style=for-the-badge)](prompt_unet_pre_print.pdf)

> **"A leap towards generalizable, lightweight, and user-controllable AI in clinical workflows."**

Authors: Paul Machauer, Dr. Marco Reisert, Prof. Dr. Janis Keuper 

## Scientific Core Innovation
Prompt U-Net transforms static segmentation into an **interactive, context-aware process**. Unlike "black-box" models, it leverages **In-Context Learning** to adapt to unseen anatomical structures using minimal data, while beating important baseline models.

Due to its design, the architecture achieves significantly lower computational complexity and a reduced memory footprint compared to established baselines. These optimizations make Prompt U-Net uniquely suited for real-time, in-browser inference, bringing high-performance AI directly into clinical and laboratory workflows with zero installation.

---

## Deployment: Clinical Accessibility via TF.js
To bridge the gap between research and clinical application, this project is deployed using TensorFlow.js. We demonstrated that, compared to resource-intensive models, it is possible to achieve high-fidelity segmentation locally on standard consumer hardware without compromising accuracy.

**Why this matters for Clinicians/Researchers:**
1. **Zero-Setup:** No Python/Docker/GPU drivers needed. Works instantly in any browser.
2. **Data Privacy:** Full **client-side inference**. Medical data never leaves the local machine.
3. **In-context learning:** Perfect for real-time interaction during imaging or screening.

---

## Interactive Demo
### Watch our one minute demo video on YouTube 
[![Demo Video (YouTube)](images/demo_thumb.png)](https://youtu.be/pYGCIfeopFA)
### Or use it yourself on your device inside [Nora Imaging](https://www.nora-imaging.com/)
- [Nora Imaging Documentation](https://www.nora-imaging.org/doc)
1. Press 'M' to memorize the segmentation you made
2. Press 'N' on another slice of the same axis to create a segmentation
3. Go ahead if the result meets your expectations. If not, edit it and memorize it
---

## Features:
- **Dual-Encoder Architecture:** Simultaneously processes medical images and 2D user-provided prompts.
- **In-Context Learning:** Enables rapid adaptation to new tasks without retraining.
- **Self-Supervised Feedback (SSF):** Automatically ensures volumetric consistency. The model uses its own predictions from adjacent slices as internal "context" to refine the current segmentation without human intervention.
  *   *Note: While a core part of the research paper for 3D consistency, SSF is not yet included in the Browser Demo.*
- **Interactive Feedback (IF):** Enables "Human-in-the-loop" refinement. A clinician can provide a manual correction on a missegmented area, which is fed back into the dual-encoder to instantly update and improve future masks.
- **Data Efficiency:** Outperforms established baselines with reduced data requirements.

<img src="images/Figure_1.png" style="width: 60%; max-width: 600px;">
<img src="images/Figure_2.png" style="width: 35%; max-width: 600px;">

---

## Technical Documentation & Publication
For an in-depth discussion of the methodology, loss functions, and initial benchmark results, please refer to our preprint:

**[Preprint](prompt_unet_preprint.pdf)**

> **Note on Project Evolution:** 
> This project is under active development. While the preprint provides the foundational scientific framework, the current implementation (especially the TF.js web version) has evolved further. The future publication will include architectural refinements and further research, for example into computational complexity and memory footprint. 
