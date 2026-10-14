---
title: Defense - A Dual-Stage Hybrid Random Forest Framework for Forward and Inverse Modeling of Ion Implantation in Si, SiC, and GaAs Substrates
date: 2026-03-07
pinned: false
category: Session
custom_category: ''
research_interests: []
image: /assets/images/pasted-image-1791968296411.png
issuer: ''
issuer_label: ''
gallery:
  - /assets/images/pasted-image-1791968415079.png
  - /assets/images/pasted-image-1791968423889.png
  - /assets/images/pasted-image-1791968430587.png
  - /assets/images/pasted-image-1791968437291.png
  - /assets/images/pasted-image-1791968443804.png
  - /assets/images/pasted-image-1791968450183.png
description: Successfully defended my undergraduate thesis on March 7, 2026, at FET Gallery, JUST, as part of Course EEE-4000 (4 credits), focusing on ML-based ion implantation modeling.
youtube: ''
link: ''
pdf_file: ''
pdf_title: ''
---

### Undergraduate Thesis Defense

**Thesis Title:** A Dual-Stage Hybrid Random Forest Framework for Forward and Inverse Modeling of Ion Implantation in Si, SiC, and GaAs Substrates

**Academic Program:** Bachelor of Science in Electrical and Electronic Engineering (B.Sc. in EEE)

**Course:** EEE 4000 — Course Project/Thesis

**Credits:** 4.0

**Defense Date:** March 7, 2026

**Venue:** Faculty of Engineering and Technology (FET) Gallery, Jashore University of Science and Technology (JUST), Bangladesh

**Student:** Abdullah Shadek Fahim

**Student ID:** 191131

### Supervisory Committee

**Supervisor:** Md. Amzad Hossain, Dr. Eng., Associate Professor, Department of Electrical and Electronic Engineering, JUST.

**Co-supervisor:** Jahedul Islam, Lecturer, Department of Electrical and Electronic Engineering, JUST.

**External Faculty Member:** Dr. Md. Azad Hossain, Department of Electrical and Computer Engineering (ECE), Chittagong University of Engineering and Technology (CUET).

The thesis defense was attended by the faculty members of the Department of Electrical and Electronic Engineering, JUST, along with the external faculty member.

### Abstract

Ion implantation is an indispensable process for the fabrication of semiconductor devices, but simulating it in detail using Monte Carlo tools, such as SRIM/TRIM, is computationally and directionally costly. In this thesis, a dual-stage physics-informed Random Forest surrogate approach has been formulated for rapid forward and inverse ion implantation modelling in silicon (Si), silicon carbide (SiC) and gallium arsenide (GaAs) substrates. By using a physically validated design space of five ion species and implantation energies ranging from 10 keV to 10 MeV with incident angles from 0°–89.9° and target thicknesses up to 10,000 Å, a multi-input Random Forest regressor is trained on stopped ion events separated by a gatekeeper classifier in the forward direction, which predicts nine implantation quantities that include projected range, straggle, lateral dispersion and radial distribution followed by vacancy production and statistics of ion transport. The reverse problem is cast as a constraint-based enumeration of solutions, with the developed surrogate acting as an efficient evaluator to enumerate practical sets of implantation parameters for target depths.

Validation over all substrates and ion species shows excellent predictive accuracy (R² > 0.94 for projected range and R² > 0.98 for backscattering), combined with a decrease in inference time from minutes per SRIM simulation to milliseconds per query, leading to an orders-of-magnitude speed-up in computational performance. Further validation against published SIMS experimental profiles confirms that the surrogate achieves accuracy comparable to SRIM itself, with an average prediction error of 10.9% versus 10.6% for SRIM. The recommended methodology presents an accurate, interpretable and computationally efficient alternative to traditional Monte Carlo or analytical models in the design of ion implantation processes.

### Research Contributions

- Developed a dual-stage, physics-informed Random Forest surrogate framework for forward and inverse ion implantation modeling.
- Investigated ion implantation in three semiconductor substrates: Si, SiC, and GaAs.
- Modeled nine implantation-related physical quantities using a multi-output prediction framework.
- Developed a constraint-based inverse modeling approach to identify practical implantation parameters for desired target depths.
- Evaluated model accuracy across multiple ion species and implantation conditions, including comparison with published Secondary Ion Mass Spectrometry (SIMS) experimental profiles.
- Demonstrated the potential to accelerate semiconductor process modeling by replacing repeated, computationally expensive SRIM evaluations with millisecond-scale surrogate inference.

### Keywords

Ion Implantation, Random Forest, Machine Learning, Surrogate Modeling, SRIM/TRIM, Forward Modeling, Inverse Modeling, Silicon, Silicon Carbide, Gallium Arsenide, Semiconductor Device Fabrication, Physics-Informed Machine Learning.
