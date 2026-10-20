# Syndactyly Surgery: Research Progress

**Focus:** Finite element modeling of surgical flap deformation and stress distribution  
**Tools:** ANSYS  
**My role:** Led FEA model setup, simulation, boundary-condition definition, and mesh-convergence work within a collaborative project.

[← Research Progress](./README.md) · [IMECE 2025 paper](../Reports/Syndactyly/IMECE2025-166019_Final.pdf) · [Related review](../Reports/Syndactyly/Handsurgery.pdf)

## 1. Initial attempt: Simulating the flap in 3D

I first attempted to simulate the interaction between a hand and a surgical flap in three dimensions. After multiple trials, I obtained an initial deformation sequence by prescribing displacement to the lower surface and selected nodes of the flap while applying gravity to the hand.

This early model helped me explore geometric movement, but it did not yet reproduce the full surgical process of extending and suturing the flap across the palmar web space.

**Supporting material:** [3D simulation video](./assets/Syndactyly/3D_Simulation_Sydactyly.mp4), [3D simulation experimental data](./assets/Syndactyly/3D_Experimental_data.pdf)

## 2. Modeling decision: From 3D contact to a measurement-based 2D approach

Reproducing the complete flap transfer and suturing procedure in 3D proved difficult. Complex geometry, contact behavior, mesh distortion, and convergence problems limited the reliability and practicality of repeated simulations.

I therefore shifted to a simplified representation: extract the relevant web space skin surface from the 3D hand model into a 2D representation, then compare the measurements of the extracted skin and the surgical flap to determine appropriate displacement conditions. This made it possible to study flap stress under a more tractable set of assumptions.

**Supporting material:** [File 1 — Extracting 2D skin from the 3D model](./assets/Syndactyly/2D_progress(1).pdf), [File 2 — Determining displacement from skin and surgical flap measurements](./assets/Syndactyly/2D_progress(2).pdf)

## 3. Further exploratory work: Hexagonal and other flap geometries

After establishing the measurement based 2D workflow, I applied it to a hexagonal flap using anatomy derived dimensions. In the published IMECE proof-of-concept, the stress distribution showed concentrations near flap corners, especially along the upper sutured edge.

I also explored an additional flap shape reported in the surgical literature, using its reported dimensions or geometric description to construct and simulate a new configuration using a comparable approach.

This subsequent exploratory model in File 4 should be distinguished from the **published IMECE study, which evaluates a hexagonal flap**. 

**Supporting material:** [File 3 — Hexagonal flap analysis](./assets/Syndactyly/2D_progress(3).pdf), [File 4 — New flap geometry](./assets/Syndactyly/2D_progress(4).pdf).

## 4. What I Learned & Technical Limitations

Throughout this research, I encountered several challenges that highlighted the limitations of conventional FEA:

- **Computational cost:** Complex 3D simulations often required approximately 10 minutes to an hour per attempt. I sometimes had to use two computers to manage multiple simulation attempts, yet some analyses still failed to converge.
- **Numerical convergence:** Mesh distortion, complex contact interactions, and boundary condition choices made it difficult to reproduce the complete surgical procedure in 3D. This experience taught me that a geometrically detailed model is not always a numerically reliable or efficient model.
- **Simplified material behavior:** Although biological soft tissues exhibit nonlinear mechanical behavior, I used linear elastic material models to simplify the analysis. I would like to explore nonlinear FEA, particularly hyperelastic material models, to better represent soft tissue deformation.
- **Patient-specific limitations:** Patient specific geometry alone is insufficient for accurate biomechanical predictions when individual tissue properties remain uncertain.

These challenges motivated me to explore **machine-learning surrogate modeling** as a potential approach to reduce the computational cost of repeated FEA simulations.

In the long term, I hope to combine **nonlinear finite element modeling and machine learning** to develop more efficient and realistic computational methods for soft-tissue biomechanics and broader engineering applications.


