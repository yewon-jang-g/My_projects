# Rhinoplasty Graft Stability — Research Development

**Focus:** Computational biomechanics · 3D Finite Element Analysis  
**Tools:** CATIA · ANSYS SpaceClaim · ANSYS Mechanical  
**My role:** First author; research conception, methodology, geometric modeling, material property estimation, loading setup, result interpretation, and manuscript development.

[← Research Progress](./README.md) · [ASEE-NCS 2026 paper (PDF)](../Reports/Rhinoplasty/rhinoplasty.pdf)

## 1. Research motivation

My interest in studying rhinoplasty from a biomechanical perspective was inspired by its prevalence in South Korea and conversations with people who had undergone the procedure. I wanted to understand how different graft-stabilization strategies could respond to everyday external loads and higher-force events during healing.

The resulting work compared **fascia-wrapped diced cartilage (DC-F)** with **platelet-rich fibrin-embedded diced cartilage (DC-PRF)**.

**Supporting material:** [Initial proposal](./assets/Rhinoplasty/Idea_propasal.pdf)
## 2. Developing the nasal model

I developed nasal geometry using **CATIA and SpaceClaim**. I assumed symmetry and modeled **one half of the nose** to reduce computational complexity. The final model contained a nasal soft tissue envelope, graft, nasal bone, lateral cartilage, and septal cartilage.

**Supporting material:** [Early prototype video](./assets/Rhinoplasty/3Dnosemodel_prototype.mp4), [final-model image](./assets/Rhinoplasty/Nose_model.png).

## 3. Literature review and constitutive assumptions

I surveyed the surgical and biomechanical literature and organized material properties and healing assumptions. The study used a **linear elastic approximation** for the modeled tissues, and estimates for the graft's effective properties were informed by mixture relationships and the literature.

Three representative postoperative conditions were assessed:
- **T1:** Immediately after surgery
- **T2:** One month after surgery
- **T3:** One year after surgery

These represent **three assumed mechanical states**, not a biological healing process directly simulated over time.

**Supporting material:** [Literature review spreadsheet](./assets/Rhinoplasty/Literature_review.xlsx).

## 4. Loading scenarios

I used two **static structural** force cases:
- **0.5 N:** Approximation of everyday loading such as eyeglass pressure.
- **5 N:** Higher-force loading applied to the nasal bridge, representing an external impact scenario.

These are prescribed load comparisons, not a transient dynamic collision simulation.

## 5. Findings reported in the paper

The published study reports mesh convergence checking and compares graft stress and deformation across the modeled conditions (Tables 3–4 and Figures 3–4).

At **T2 (one month after surgery)**, for example:

| Loading | DC-F max von Mises stress | DC-PRF (40% cartilage) |
|---|---:|---:|
| 0.5 N | 2.34 MPa | 0.062 MPa |
| 5 N | 2.26 MPa | 0.188 MPa |

DC-F exhibited higher peak stress under the modeled conditions, while deformation and loading sensitivity depended on graft type and postoperative condition. These findings do **not** establish clinical superiority of one procedure for individual patients.

## 6. Technical Limitations & Future Research Direction

Throughout this project, I encountered several challenges in developing realistic biomechanical simulations:

- **Simplified material behavior:** Although biological soft tissues exhibit nonlinear mechanical responses, I adopted linear elastic models to simplify the analysis. This approximation may not fully capture tissue behavior under large deformation.
- **Uncertainty in material properties:** Due to limited patient-specific mechanical data, tissue properties were estimated from published literature and analytical relationships, making it difficult to account for individual variability.
- **Geometric and contact complexity:** Accurately representing nasal anatomy and interactions between grafts and surrounding tissues required geometric simplifications and assumptions about interface conditions.
- **Computational cost and numerical convergence:** Developing detailed 3D models was computationally demanding, while geometric complexity and convergence challenges made repeated simulations difficult. Similar challenges were particularly evident in my earlier syndactyly research.

These limitations motivated my interest in **nonlinear finite element modeling**, particularly hyperelastic material models and nonlinear contact analysis, to better represent the mechanical behavior of soft tissues.

At the same time, my experiences in both rhinoplasty and syndactyly research encouraged me to explore **machine-learning surrogate models** as a potential approach to reduce the computational cost of repeated FEA simulations.

My current goal is to establish and validate an ML surrogate model using an existing linear-elastic FEA framework, with the longer-term objective of extending this approach to **nonlinear soft-tissue simulations and broader computational mechanics applications**.


