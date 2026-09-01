# Numerical Experiments — PhyDrop-GP

This repository contains the **numerical experiments presented in Chapter 6 of the thesis**, which investigate the proposed **PhyDrop-GP (Physics-Informed Dropout Gaussian Process)** framework for probabilistic prediction and uncertainty quantification.

The experiments compare the proposed physics-informed formulation with a conventional **Gal-style Monte Carlo Dropout** model. The main objective is to examine whether incorporating known physical structure into the probabilistic learning objective improves predictive performance, physical consistency, extrapolation, and the quality of epistemic uncertainty.

## Experiments

The notebook contains four numerical studies:

**Experiment 1 — Hamiltonian Dynamical System**
A nonlinear Duffing-type Hamiltonian oscillator is used to study long-horizon prediction and extrapolation. The experiment investigates whether the Hamiltonian constraint improves learned dynamics and reduces error outside the training regime.

**Experiment 2 — Fluid Dynamics**
A synthetic Taylor–Green vortex is used to test learning from sparse and noisy observations. The models are evaluated on an unseen spatial and temporal regime using predictive accuracy, calibration, epistemic uncertainty, and Navier–Stokes residuals.

**Experiment 3 — C-MAPSS RUL Prediction**
The NASA C-MAPSS turbofan degradation dataset is used as a real-world-style application. A discrete RUL degradation constraint is incorporated into the physics-informed objective, and the models are evaluated under both in-distribution and distribution-shifted operating conditions.

**Experiment 4 — Layer-Relevance Analysis of Dropout**
A Hamiltonian harmonic oscillator is used to investigate how dropout-induced epistemic uncertainty is distributed across neural-network layers. Uniform and layer-dependent dropout configurations are compared to identify which layers contribute most strongly to predictive uncertainty.

## Purpose

Collectively, these experiments evaluate PhyDrop-GP from several complementary perspectives:

* predictive accuracy,
* probabilistic uncertainty quantification,
* extrapolation and distribution-shift behaviour,
* physical consistency,
* calibration,
* and the role of individual network layers in uncertainty propagation.

The results support the central thesis that **physics-informed probabilistic learning can provide a useful trade-off between predictive accuracy, physical consistency, and informative epistemic uncertainty**, particularly in settings where models must operate beyond the observed data distribution.

## Notebook

The accompanying Google Colab notebook contains the **full simulation code, model implementations, training procedures, evaluation metrics, plots, and numerical results** used to produce the experiments reported in Chapter 6.

The notebook is intended to provide a reproducible computational record of the numerical studies described in the thesis.
