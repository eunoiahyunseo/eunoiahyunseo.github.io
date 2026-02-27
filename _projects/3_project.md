---
layout: page
title: Vehicle Benchmark
description: ETRI Visual Intelligence Lab
img: assets/img/cheonan_pipeline.png
importance: 1
category: 2026
related_publications: false
---

## Overview

This project proposes a **CCTV-only vehicle trajectory forecasting framework** for real urban infrastructure environments.  
Unlike prior work that depends on ego-vehicle sensors, LiDAR-built HD maps, or controlled cooperative setups, this work focuses on **single-view urban CCTV streams** and builds an end-to-end pipeline for dataset construction and trajectory prediction.

<div class="card mt-4 mb-5 p-4" style="background-color: #f8f9fa; border-left: 4px solid #007bff;">
<strong>Key Challenge</strong><br>
Reliable trajectory prediction from infrastructure-only CCTV is difficult due to viewpoint inconsistency, missing depth/LiDAR cues, noisy tracking jitter, and the absence of pre-built HD maps.
</div>

---

## Approach

The full pipeline includes camera geometry recovery, dataset generation, map integration, and forecasting model adaptation:

| Component | Description |
|:----------|:------------|
| **Monocular Camera Calibration** | Estimate homography from CCTV views to BEV using learning-based auto-calibration and RANSAC constraints |
| **Dataset Construction** | Convert detections/tracks into V2X-Seq-style trajectory records (`type`, `x`, `y`, `theta`, timestamp), then generate infrastructure-aligned scenes |
| **HD-Map Integration** | Build map annotations directly from converted BEV space for infrastructure-only prediction |
| **Model Benchmarking** | Evaluate infrastructure-only variants of **HiVT**, **V2X-Graph** (without IA), and proposed **V2ITrajNet** |
| **Interestingness Target Selection** | Rank target agents by motion pattern importance (turning/lateral behavior) to improve training focus |

---

## Key Results

The proposed **V2ITrajNet (with map)** achieved the best performance on the Cheonan-built dataset:

| Model | minADE | minFDE | MR |
|:------|-------:|-------:|---:|
| HiVT (w map) | 1.033 | 1.543 | 0.204 |
| V2X-Graph (w map) | 0.996 | 1.517 | 0.212 |
| **V2ITrajNet (w map, Ours)** | **0.943** | **1.288** | **0.162** |

<div class="card mt-5 mb-5 p-4" style="background-color: #f8f9fa; border-left: 4px solid #28a745;">
<strong>Performance Highlight</strong><br>
Compared with map-enabled baselines, V2ITrajNet achieved the lowest displacement error and miss rate, showing strong suitability for infrastructure-only forecasting.
</div>

<h3 style="margin-top: 2.5rem; margin-bottom: 1.2rem;">Dataset Statistics (Cheonan CCTV)</h3>

| Item | Value |
|:-----|------:|
| Total Scenes | 7,364 |
| Total Rows | 21,389,113 |
| Total Actors | 528,501 |
| Total Targets | 1,501,136 |
| Timestamps per Scene | 80 |

---

## Resources

<div class="d-flex flex-wrap gap-2">
<a href="https://github.com/eunoiahyunseo/ETRI" class="btn btn-sm z-depth-0" target="_blank">
<i class="fab fa-github"></i> GitHub
</a>
<a href="https://www.notion.so/Trajectory-Prediction-2e8ac0eb0a7680f38cf1cec1e8a016c9?source=copy_link" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-globe"></i> Notion
</a>
<a href="https://docs.google.com/presentation/d/1WYbdB6hedZBbOnyC4yAlgybb8zeXq5a0/edit" class="btn btn-sm z-depth-0" target="_blank">
<i class="fas fa-file-pdf"></i> Slides
</a>
</div>
