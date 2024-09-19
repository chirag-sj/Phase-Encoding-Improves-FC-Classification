Resting State Static Brain Functional Connectivity Classification.
Symmetric Positive Definite Matrices compose an arbitrary Riemannian Surface. This enables us to utilize geodesic distance metrics between such matrices.
Functional Connectivity matrices are SPD which mathematically validates the use of geodesic distances for inter-FC comparison using tangent space projection.
But the FC matrices which are calculated using Pearson's correlation fails to capture phase information. This information can be retained by applying Hilbert Transform to the fMRI timeseries signal followed by application of Pearson's correlation.
The elements of such matrix are complex, real part of which is traditional FC but the imaginary non-symmetric part is phase-based connectivity.
We project the phase FC into the Tangent Space which leads to improved FC classification in the ABIDE dataset.
