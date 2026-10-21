# Yewon Jang

### Computational Mechanics | Computational Biomechanics | Machine Learning

**B.S. in Mechanical Engineering, Hanyang University (2026)**

[Email](mailto:yewonjang1414@gmail.com) · [CV](./CV_final.pdf)

## About Me

I am a mechanical engineering graduate with research experience in **finite element analysis (FEA) and computational biomechanics**. My research interests lie in integrating physics-based simulation with machine learning to develop more efficient and reliable computational methods.

Through my research on syndactyly surgery and rhinoplasty grafts, I encountered limitations of conventional FEA, including high computational costs, numerical convergence difficulties, and simplified material assumptions.

During the syndactyly project, complex 3D contact simulations often required substantial computational time and did not always converge. These challenges led me to explore dimensional simplification and motivated my interest in **machine-learning-based surrogate modeling**.

I am now independently studying how data-driven models can accelerate FEA predictions, with a long-term goal of extending these methods to nonlinear materials and broader computational mechanics problems.

## Research Experience

### 01. Patient-Specific Modeling for Syndactyly Surgery

**ANSYS | Structural FEA | Contact Mechanics | Mesh Convergence**

*ASME IMECE 2025 | Co-author*

Developed the FEA component of a collaborative research framework combining photogrammetry-based hand reconstruction with biomechanical analysis of surgical flaps.

**My Contributions**
- Conducted ANSYS modeling, meshing, and structural simulations.
- Applied anatomy-derived flap dimensions and surgical displacement conditions.
- Addressed difficulties in 3D contact analysis by converting the complex web-space surface into a simplified 2D representation.
- Established boundary conditions and performed mesh convergence studies.
- Evaluated stress concentrations in a hexagonal dorsal flap.

**Key Insight:** The analysis identified elevated stresses near flap corners, particularly along the sutured upper edge. The modeling process also highlighted the trade-off between geometric fidelity and computational feasibility.

[Research Paper — IMECE 2025](./Reports/Syndactyly/IMECE2025-166019_Final.pdf)

### 02. Biomechanical Stability of Rhinoplasty Grafts

**ANSYS | 3D FEA | Composite Material Properties | Structural Analysis**

*ASEE-NCS 2026 | First Author*

Led a comparative study of fascia-wrapped diced cartilage (DC-F) and platelet-rich fibrin-embedded diced cartilage (DC-PRF) grafts under different postoperative conditions.

**My Contributions**
- Formulated the research questions and simulation methodology.
- Constructed 3D nasal models and generated finite element meshes.
- Estimated effective graft properties using literature data and analytical relationships.
- Simulated three healing stages under static loading conditions of 0.5N and 5N.
- Analyzed stress and deformation results and prepared the manuscript.

**Key Finding:** DC-F exhibited substantially higher peak von Mises stresses than DC-PRF under the simulated conditions, with the largest differences occurring approximately one month after surgery.

[Research Paper — ASEE-NCS 2026](./Reports/Rhinoplasty/rhinoplasty.pdf)

### 03. FEA-Assisted Surgical Planning: Review

*Frontiers in Bioengineering and Biotechnology, 2025 | Co-author*

Reviewed computational methods for surgical flap design, focusing on material modeling, geometry, boundary conditions, and simulation reliability.

**My Contributions**
- Reviewed and organized prior research on FEA-assisted flap design.
- Investigated the feasibility of representative flap simulations using ANSYS.
- Examined challenges involving tissue-property uncertainty and simplified mechanical models.

The study reinforced my interest in improving the efficiency and reliability of biomechanical simulations.

[Published Article](https://doi.org/10.3389/fbioe.2025.1611993) · [PDF](./Reports/Syndactyly/Handsurgery.pdf)

## Research Progress & Behind the Simulations

Beyond the final results presented in my publications, I documented the research process behind each project including preliminary simulations, numerical challenges, methodological changes, and lessons learned.

These experiences shaped my interest in developing more efficient computational methods.

- [**Syndactyly — From 3D Simulation to 2D Flap Analysis**](./Progress/Syndactyly.md)
- [**Rhinoplasty — From Research Question to FEA**](./Progress/Rhinoplasty.md)

*Supporting simulation videos, figures, and lab-meeting presentations are available within each project page.*

## Ongoing Independent Project

### ML Surrogate Modeling for FEA Acceleration

**Status: Foundational Study & Research Planning**

**Research Question**

Can machine-learning models trained on FEA simulation data accurately predict mechanical responses under unseen conditions while reducing repeated simulation costs?

**Motivation**

My previous biomechanics projects revealed the computational challenges of detailed 3D simulations. I am pursuing this independent project to explore how machine learning can complement conventional numerical methods.

**Planned Approach**
1. Generate a parametric FEA dataset by varying geometry, material properties, and loading conditions.
2. Extract displacement and representative stress metrics.
3. Develop and compare regression-based surrogate models using Python.
4. Evaluate prediction accuracy and computational efficiency against conventional FEA.
5. Explore the extension from simplified material models toward nonlinear soft-tissue behavior.

**Planned Deliverables:** FEA dataset, Python models, accuracy and runtime comparisons, and reproducible GitHub documentation.

**Long-Term Direction:** Extend ML-assisted simulation beyond surgical biomechanics toward efficient, generalizable methods for nonlinear computational mechanics.

## Robotics & Mechatronics

**Multi-Linked Wheeled Snake Robot**

Developed an eight-segment bio-inspired robotic system with Python-based path-following control.

[Research Paper](./Reports/Snake_robot/A_MultiLinked_Wheeled_Robot_Inspired_by_Serpentine_Motion.pdf), [Poster](./Reports/Snake_robot/Poster_AMultiLinkedWheeledRobotInspiredbySerpentineMotion.pdf)

**Braille Notification Device**

Developed a solenoid-actuated system for converting Korean text into tactile Braille patterns.

[Demonstration Video](./Reports/Braille/Braille_Device_Demo.mp4)

## Technical Skills

- **Simulation:** ANSYS, FEA, Mesh Convergence Analysis, Contact Modeling
- **Programming:** Python, MATLAB
- **CAD:** CATIA, SolidWorks
- **Currently Learning:** Machine Learning, Surrogate Modeling, Nonlinear Computational Mechanics

## Education & Scholarship

**Hanyang University** — B.S. in Mechanical Engineering, 2026

**Ohio Northern University** — Mechanical Engineering Exchange Program, 2024–2025

**Korea–U.S. Student Exchange Program (KIAT)** — Scholarship Recipient, 2024–2025



