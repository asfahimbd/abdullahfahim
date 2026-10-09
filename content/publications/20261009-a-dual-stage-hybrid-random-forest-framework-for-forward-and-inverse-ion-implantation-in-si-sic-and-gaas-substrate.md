---
title: A Dual-Stage Hybrid Random Forest Framework for Forward and  Inverse Ion Implantation in Si, SiC, and GaAs Substrate
date: 2026-03-07
pinned: true
pub_type: Thesis
status: ''
authors:
  - author: Abdullah Shadek Fahim
    role: Primary Author
  - author: Md. Amzad Hossain, Dr. Eng. (Associate Professor, EEE, JUST)
    role: Supervisor
  - author: Jahedul Islam (Lecturer, EEE, JUST)
    role: Co-Supervisor
venue: Department of Electrical and Electronic Engineering, Jashore University of Science and Technology
doi: ''
link: https://ion-implant-surrogate.onrender.com
research_interests:
  - Machine Learning
  - SRIM/TRIM
  - Surrogate Modeling
  - Ion Implantation
  - Inverse Process Design
image: /assets/images/11.jpg
gallery:
  - /assets/images/114.jpg
  - /assets/images/115.jpg
  - /assets/images/111.jpg
  - /assets/images/116.jpg
  - /assets/images/112.jpg
brief_abstract: In this thesis, a dual-stage gatekeeper-constrained Random Forest surrogate has been developed for the field of semiconductor ion implantation modeling in Si, SiC, and GaAs across five ions (B, Mg, P, Ar, As). This surrogate predicts nine implantation quantities about 715 times faster than a standard SRIM run, with R2 above 0.94 for projected range and SRIM-level error against published SIMS data. The framework also offers constraint-based inverse recipe generation for target depths. Therefore, this surrogate could be useful for fast and efficient implantation process design.
pdf_file: /assets/images/191131_defense.pdf
pdf_title: Undergraduate Thesis Defense Slide
---

Ion implantation is an indispensable process for the fabrication of semiconductor devices, but simulating it in detail using Monte Carlo tools, such as SRIM/TRIM, is computationally and directionally costly. In this thesis, a dual-stage physics-informed Random Forest surrogate approach has been formulated for rapid forward and inverse ion implantation modelling in silicon (Si), silicon carbide (SiC) and gallium arsenide (GaAs) substrates. By using a physically validated design space of five ion species and implantation energies ranging from 10 keV to 10 MeV with incident angles from 0°-89.9° and target thicknesses up to 10,000 Å, a multi-input Random Forest regressors trained on stopped ion events separated by a gatekeeper classifier in the forward direction which predicts nine implantation quantities that include projected range, straggle, lateral dispersion and radial distribution followed by vacancy production and statistics of ion transport. The reverse problem is cast as a constraint-based enumeration of solutions with the developed surrogate acting as an efficient evaluator to enumerate practical sets of implantation parameters for target depths. Validation over all substrates and ion species shows excellent predictive accuracy (R² > 0.94 for projected range and R² > 0.98 for backscattering), combined with a decrease in inference time from minutes per SRIM simulation to milliseconds per query, leading to an orders-of-magnitude speed-up in computational performance. Further validation against published SIMS experimental profiles confirms that the surrogate achieves accuracy comparable to SRIM itself, with an average prediction error of 10.9% versus 10.6% for SRIM. The recommended methodology presents an accurate, interpretable and computationally efficient alternative to traditional Monte Carlo or analytical models in the design of ion implantation processes.
