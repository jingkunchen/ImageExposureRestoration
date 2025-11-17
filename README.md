# Balancing Light and Shadow: A Benchmark for Multi-Modal Image Exposure Restoration via Frequency–Phase-Driven RGB-IR Integration
---

## Abstract

Capturing high-quality images under dynamic and extreme illumination remains a long-standing challenge in computer vision. In real-world scenarios, scenes often exhibit deep shadows, harsh highlights, and abrupt lighting transitions, which lead to severe under- or overexposure that obscures critical details and impairs detection, segmentation, and classification. Traditional single-modal approaches relying on RGB or infrared (IR) imaging fall short in these conditions. In dark regions, RGB images introduce excessive noise, while in bright areas, overexposure washes out important details. Similarly, IR imaging, though effective in extreme lighting, fails to capture detailed textures and colors, limiting its performance. To address these issues, we present a novel multi-modal framework that integrates RGB and IR imaging to correct exposure in challenging scenarios. Our approach begins with a two-dimensional Fourier transform to decompose each modality into amplitude and phase components. It then employs a cross-modal fusion strategy to integrate robust IR illumination cues with detailed RGB structural information. We validate our framework through extensive experiments on the HDRT dataset, spanning industrial sites, university campuses, urban, and natural landscapes. The results show significant improvements across image quality metrics (PSNR, SSIM, LPIPS, VSI$_{err}$, and EE) as well as gains in downstream task performance.

The code is currently being used in ongoing related work and is being refactored to improve readability.
It will be released once this work has been completed.

### Dataset Details

- **HDRT Dataset Overview:**  
  The HDRT dataset is designed to support multi-modal exposure correction research. It comprises 10,000 scenes, with each scene providing four images (totaling 40,000 images):
  - **Low-Exposure (LE) RGB Image:** Severely underexposed image.
  - **High-Exposure (HE) RGB Image:** Severely overexposed image.
  - **Normal-Exposure (Reference) RGB Image:** Properly exposed image serving as the ground truth.
  - **Infrared (IR) Image:** Captures robust illumination cues under extreme conditions.

- **Access:**  
  The dataset is publicly accessible at [Hugging Face HDRTDataset](https://huggingface.co/datasets/jingchao-peng/HDRTDataset).

---

## Repository Structure

- **/manuscript:**  
  Contains the draft manuscript (PDF format) with full details on our theoretical background, network design, experiments, and ablation studies.

- **/code:**  
  Source code for the proposed framework, including scripts for training, evaluation, and inference.

- **/data:**  
  Documentation and scripts to assist with downloading and preparing the HDRT dataset.

- **/supplementary:**  
  Additional experimental details and extended results supporting the main paper.

---

## Usage

### Getting Started

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/jingkunchen/BLS.git
   cd BLS
