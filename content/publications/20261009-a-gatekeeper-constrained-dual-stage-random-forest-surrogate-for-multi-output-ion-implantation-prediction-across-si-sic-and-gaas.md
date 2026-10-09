---
title: A Gatekeeper-Constrained Dual-Stage Random Forest Surrogate for Multi-Output Ion Implantation Prediction Across Si, SiC, and GaAs
date: 2026-06-24
pinned: false
pub_type: Journal
status: Under Review
authors:
  - author: Abdullah Shadek Fahim
    role: Primary Author
  - author: Musavvir Haque, Abu Taher, Nure Modina Sathi, Jahedul Islam, Md. Mehedi Hasan, Md. Amzad Hossain
    role: Co-Author
venue: 'Nuclear Instruments and Methods in Physics Research Section B: Beam Interactions with Materials and Atoms'
doi: 10.2139/ssrn.7580999
link: ''
research_interests:
  - 10-Fold Cross-Validation
  - SRIM/TRIM
  - Surrogate Modeling
  - Ion Implantation
  - Random Forest
  - Python
  - Data Generation Pipeline
  - Silicon Carbide
  - Gallium arsenide (GaAs)
  - Wide-bandgap Semiconductor
image: /assets/images/graphical.jpg
gallery: []
brief_abstract: Modern semiconductor devices rely on ion implantation to define dopant profiles that dictate crucial electrical properties. However, accurately simulating these profiles for process design using the standard simulation tool, SRIM/TRIM, demands substantial computational time. We address this significant limitation by introducing a gatekeeper-constrained dual-stage Random Forest surrogate model...
pdf_file: /assets/images/Supplementary Materials.pdf
pdf_title: Supplementary Materials
---

Modern semiconductor devices rely on ion implantation to define dopant profiles that dictate crucial electrical properties. However, accurately simulating these profiles for process design using the standard simulation tool, SRIM/TRIM, demands substantial computational time. We address this significant limitation by introducing a gatekeeper-constrained dual-stage Random Forest surrogate model. First, a classifier separates stopped ions from transmitted ones, preventing zero-range samples from contaminating the training data. Next, a regressor simultaneously predicts nine critical physical quantities, including ion range, straggle, and radiation damage, using a single unified model. This surrogate was trained across three substrates (Si, SiC, GaAs) and five ion species for energies of 10 to 10,000 keV and implantation angles up to 89.9°. Under ten-fold cross-validation, the model achieves a mean R² of 0.911 while accelerating computation time by a factor of 715 relative to SRIM. Against independent published experimental measurements, the surrogate attains an 8.3% mean absolute percentage error.
