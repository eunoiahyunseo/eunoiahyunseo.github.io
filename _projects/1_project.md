---
layout: page
title: Discrete Flow Matching
description: Kaist Visual AI Group
img: /assets/img/project1_cover.png
importance: 1
category: 2025
related_publications: true
---

## Overview

This project investigates the **core differences between Continuous and Discrete Flow Matching** for generative modeling. Developed during an internship at KAIST Visual AI Group, the work focuses on building a testbed to compare these approaches on discrete datasets including MNIST and sketch data.

<div class="card mt-3 p-3" style="background-color: #f8f9fa; border-left: 4px solid #007bff;">
<strong>Key Research Question</strong><br>
Why use flow matching over autoregressive transformers for sketch generation?
</div>

---

## Motivation

| Autoregressive Transformers | Flow Matching |
|:----------------------------|:--------------|
| Sequential token generation | Parallel generation |
| Cannot revise past decisions | Iterative refinement |
| Limited task flexibility | Flexible conditioning |

---

## Approach

**Dual Modality Architecture**
- CNN encoder for rendered sketch images (UDF representation)
- Transformer encoder for stroke sequences

**Key Components**
- **VQ-VAE**: Discrete codebook learning for structured representations
- **CFG**: Classifier-Free Guidance adapted for discrete state-space models
- **MDM vs DFM**: Ablation study comparing Masked Diffusion and Discrete Flow Matching

**Target Tasks**
- Stroke infilling
- Layout generation with given strokes
- Sketch generation with given layout

---

## Datasets

| Dataset | Description |
|:--------|:------------|
| MNIST | 32x32 grayscale handwritten digits |
| QuickDraw | Simple stroke-based sketches |
| Creative Sketch | Complex multi-stroke sketches with labels |


---

## Resources

<div class="d-flex flex-wrap gap-2">
<a href="https://github.com/eunoiahyunseo/KAIST-2025-S" class="btn btn-sm z-depth-0" target="_blank">
<i class="fab fa-github"></i> GitHub
</a>
<a href="https://docs.google.com/document/d/1gcpfwZzmCA1nm4xvd3n6gAilxnc74WnXASg-0vQ_B6s/edit?tab=t.0#heading=h.5s4fspjurb46" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-file-alt"></i> Progress Report
</a>
<a href="https://docs.google.com/presentation/d/1ZFcuu2macX0Q3xDZchJ6sZb1xhJgZVtI/edit?slide=id.p1#slide=id.p1" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-file-powerpoint"></i> Slides
</a>
</div>
