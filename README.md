# PlasmaNetwork

## Chemical Reaction Network Analysis using Machine Learning

This repository contains Python code for analyzing and visualizing chemical reaction networks. It leverages machine learning, specifically TensorFlow, to determine the relative importance (weights) of different reactions within a chemical scheme based on species densities and initial fractions. The analysis includes visualizing the reaction network using Petri nets and species-centric graphs.

## Project Structure

The notebook demonstrates a workflow for analyzing chemical schemes. The key steps are:

1.  **Data Loading**: Reading chemical simulation output files (`chemFinalDensities.txt`, `.in`, `.chem`) into pandas DataFrames.
2.  **Data Wrangling**: Processing the raw data to extract relevant information, such as normalized species densities and initial fractions.
3.  **Machine Learning Analysis (04_weights.py)**: Using a TensorFlow model to calculate weights for each reaction based on their contribution to the final species densities. This involves setting up a model that relates initial species fractions and reaction rates to final species densities and training the model to find the reaction weights that minimize the difference between predicted and actual densities.
4.  **Visualization (05_petrinet.py and 06_graph.py)**: Generating visual representations of the chemical reaction network:
    *   **Petri Net**: A bipartite graph showing species (circles) and reactions (rectangles), with edges indicating the flow of species in reactions. Reaction nodes are colored based on their learned weights (positive for blue, negative for orange).
    *   **Species-Centric Graph**: A graph focusing on the direct connections between species involved in reactions, filtered by reaction importance.
5.  **Finding Mechanisms**: Identifying reactions that destroy specific species based on the reaction definitions.

## Chemical Schemes Analyzed

The notebook includes examples of applying this workflow to different chemical schemes:

*   **Nitrogen-Hydrogen (CS17)**: Analysis of a complex scheme involving various nitrogen and hydrogen species and their reactions.
*   **Argon (Simple Scheme)**: Analysis of a simpler scheme focusing on Argon species and their excited states.

## Requirements

*   Python 3.6+
*   pandas
*   numpy
*   tensorflow
*   pygraphviz
*   graphviz (system library)

## Setup

1.  Clone this repository.
2.  Install the required Python packages:

    sudo apt-get update
    sudo apt-get install graphviz libgraphviz-dev
