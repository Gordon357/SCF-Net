# SPAR-Net
# Artifact Aware Reliability Guided Feature Routing for Optical Medical Image Segmentation (SPAR-Net)

Official PyTorch implementation of the paper: **Artifact Aware Reliability Guided Feature Routing for Optical Medical Image Segmentation** (Submitted to IEEE TCSVT).

---

## 🌟 Overview
Optical medical image segmentation is often challenged by acquisition-induced artifacts (specular reflections, hair, bubbles, shadows, etc.). Direct skip-connections can transmit these unreliable shallow features to the decoder, causing segmentation errors. 

To address this, we present **SPAR-Net**, a decision-decoupling framework that separates lateral feature reuse into two sequential stages:
1. **Hierarchical Semantic Purification (HSP)**: Verifies whether a shallow candidate is supported by deeper target semantics.
2. **Adaptive Detail Retrieval (ADR)**: Formulates decoder-conditioned retrieval over the filtered candidate levels.

<p align="center">
  <img src="figures/fig2.png" width="90%" alt="Overall Architecture">
</p>

---

## ⚡ Main Features
- **Plug-and-Play Mechanism**: HSP and ADR can be seamlessly transferred to other encoder-decoder backbones (e.g., standard U-Net).
- **Efficiency**: ADR scales with a complexity of approximately $\mathcal{O}(HWLC)$ instead of the $\mathcal{O}((HW)^2C)$ of spatial self-attention.
- **High Robustness**: Exceptional stability under clinical corruptions (specular reflection, hair, shadow, blur) evaluated via a testing-only perturbation protocol.

