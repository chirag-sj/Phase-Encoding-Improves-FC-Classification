# Resting State Static Brain Functional Connectivity Classification Using Geometric Methods

## Overview
This project focuses on the classification of resting-state brain functional connectivity (FC) using advanced geometric methods. Specifically, we explore how Symmetric Positive Definite (SPD) matrices, which describe FC, can be used to improve classification by leveraging Riemannian geometry.

## Motivation
Functional Connectivity (FC) matrices are typically computed using Pearson's correlation on fMRI time-series data. While this captures linear relationships, it fails to retain critical phase information from brain signals. By applying the **Hilbert Transform** to the fMRI time series before computing the FC matrix, we can create complex matrices that retain both amplitude (real part) and phase (imaginary part) information.

This enhanced representation provides more nuanced insights into brain connectivity.

## Methodology
### Key Steps:
1. **Functional Connectivity Matrix (FC):**
   - Traditionally, FC is calculated using Pearson's correlation, resulting in SPD matrices that can be projected onto a Riemannian manifold.
   - The geodesic distance between SPD matrices allows for comparison of brain connectivity.

2. **Phase-Based Connectivity (PFC):**
   - To capture phase information, the **Hilbert Transform** is applied to the fMRI time-series signal.
   - Pearson's correlation is then applied to the transformed signal, producing a complex FC matrix.
     - **Real part:** Traditional FC matrix.
     - **Imaginary part:** Phase-based connectivity matrix (non-symmetric).

3. **Tangent Space Projection:**
   - Both the FC and PFC matrices are projected into tangent space for geodesic distance computation.
   - This tangent space representation allows for improved comparison between brain states.

### Key Benefit:
By utilizing the phase-based connectivity, the classification accuracy on the **ABIDE dataset** improves significantly, demonstrating the importance of capturing phase information.

## Dataset
The **ABIDE (Autism Brain Imaging Data Exchange)** dataset is used for training and validation of the classification model. This dataset contains resting-state fMRI data from individuals with Autism Spectrum Disorder (ASD) and controls, providing an excellent testbed for FC-based classification methods.

## Results
The method demonstrates improved classification performance compared to traditional FC methods, particularly due to the inclusion of phase-based connectivity in the Riemannian framework.

## Conclusion
By incorporating the Hilbert Transform and using advanced geometric tools such as tangent space projection, this approach enhances the ability to classify functional connectivity networks. The use of phase information is particularly beneficial, leading to more accurate brain state classification. Experimentation for different classification tasks is in progress.

---

