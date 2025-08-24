# PlasmaNetwork ⚛️

Welcome to this project focused on applying ML to understand and visualize complex chemical reaction networks.

Reaction mechanisms often include vast amounts of data, making it challenging to pinpoint the most crucial reactions driving a system's behavior. This project provides a workflow to tackle this by:

*   Analyzing simulated species densities and initial conditions using [LoKI-B](https://github.com/IST-Lisbon/LoKI).
*   Processing detailed chemical reaction schemes.
*   Using a machine learning model to determine the 'importance' (weights) of each reaction.
*   Generating insightful visualizations of the reaction network.

## 📂 Project Structure

The core logic is implemented in Python code within the notebook, organized into sections for clarity:

*   **Data Loading and Preparation**: Cells for reading and processing input files (`.txt`, `.in`, `.chem`).
*   **Chemical Reaction Analysis (04_weights.py logic)**: Implementation of the TensorFlow model to calculate reaction weights.
*   **Visualization (05_petrinet.py and 06_graph.py logic)**: Code to generate Petri nets and species-centric graphs using `pygraphviz`.
*   **Mechanism Identification**: Code to analyze reaction contributions to specific species.

The notebook also includes sections demonstrating the application of this workflow to different chemical schemes (Nitrogen-Hydrogen and Argon).
