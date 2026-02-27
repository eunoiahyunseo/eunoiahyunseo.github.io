---
layout: page
title: OSCAR
description: KNU PRMI Lab
img: assets/img/publication_preview/oscar.png
importance: 1
category: 2026
related_publications: true
---

## Overview

**OSCAR** (Optical-aware Semantic Control for Aleatoric Refinement) is a novel framework for converting **Synthetic Aperture Radar (SAR) imagery** into photorealistic optical images. This work addresses the fundamentally ill-posed problem of SAR-to-optical translation.

<div class="card mt-3 p-3" style="background-color: #f8f9fa; border-left: 4px solid #007bff;">
<strong>Key Challenge</strong><br>
Translating SAR observations into photo-realistic optical images is fundamentally ill-posed due to speckle noise, geometric distortions, semantic misinterpretation, ambiguous texture synthesis, and structural hallucinations.
</div>

---

## Approach

OSCAR integrates three core innovations:

| Component | Description |
|:----------|:------------|
| **Cross-Modal Semantic Alignment** | Establishes an Optical-Aware SAR Encoder by transferring robust semantic knowledge from an optical reference model to the SAR processor |
| **Semantically-Grounded Generative Guidance** | Implements a specialized ControlNet combining class-aware text prompts for broader context with hierarchical visual prompts for local spatial direction |
| **Uncertainty-Aware Objective** | Explicitly models aleatoric uncertainty to dynamically adjust reconstruction focus, addressing speckle-induced ambiguity challenges |

---

## Key Results

OSCAR achieves **superior perceptual quality and semantic consistency** compared to state-of-the-art approaches through experimental validation.

---

## Project Site

<div class="embed-responsive embed-responsive-16by9" style="margin-bottom: 1rem;">
  <iframe
    src="https://eunoiahyunseo.github.io/OSCAR/"
    style="width: 100%; height: 600px; border: 1px solid #ddd; border-radius: 8px;"
    allowfullscreen>
  </iframe>
</div>

---

## Resources

<div class="d-flex flex-wrap gap-2">
<a href="https://github.com/eunoiahyunseo/ETRI" class="btn btn-sm z-depth-0" target="_blank">
<i class="fab fa-github"></i> GitHub
</a>
<a href="https://eunoiahyunseo.github.io/OSCAR/" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-globe"></i> Project Site
</a>
<a href="https://arxiv.org/pdf/2601.06835" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-file-pdf"></i> Paper
</a>
</div>

<span style="display:none">{% cite lee2026oscaropticalawaresemanticcontrol %}</span>
