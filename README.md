# Automated-Pathway-Reconstruction-using-Attention-Guided-GNN
# Overview

This project focuses on reconstructing biological pathways from large-scale protein–protein interaction (PPI) datasets using Attention-Guided Graph Neural Networks (GATs).
The framework enables:

Link prediction: Discovering potential new protein–protein interactions.

Pathway reconstruction: Clustering predicted interactions into functional pathways.

External comparison: Matching reconstructed pathways with known biological databases (e.g., KEGG, Reactome).

Generalization: Applying a trained GAT model to new datasets and classifying them into known or novel pathways.

# Features

Build PPI networks from raw STRING database inputs.

Train Graph Attention Networks (GATs) to learn protein embeddings.

Perform link prediction to identify missing or novel interactions.

Cluster embeddings into functional biological pathways using unsupervised ML.

Compare clusters with external reference pathways using similarity metrics (e.g., Jaccard, Cosine).

Support new dataset generalization for pathway classification.

# Tech Stack

Languages: Python

Libraries: PyTorch, PyTorch Geometric, scikit-learn, NetworkX, NumPy, pandas, matplotlib

Data Sources: STRING protein–protein interaction datasets, KEGG/Reactome pathways

# Workflow

Preprocessing: Load and clean STRING protein–protein interaction data.

Graph Construction: Build a PyTorch Geometric graph from proteins and interactions.

GAT Training: Train a Graph Attention Network to learn node embeddings.

Link Prediction: Predict new protein–protein interactions from embeddings.

Pathway Reconstruction: Cluster embeddings into candidate pathways.

External Comparison: Match pathways with KEGG/Reactome via similarity metrics.

New Dataset Generalization: Apply trained GAT to unseen data and classify pathways.

# Evaluation

Link Prediction: AUC, F1-score

Clustering Quality: Silhouette score, Davies–Bouldin index

Pathway Matching: Jaccard similarity, Cosine similarity heatmaps

# Future Work

Incorporate multi-omics data (gene expression, epigenomics).

Extend to cross-species pathway reconstruction.

Develop an interactive visualization dashboard for pathway analysis.

# Author

Pratyush Lenka 23BAI1470
Aayush P Menon 23BAI1470
Research on Graph Neural Networks & Bioinformatics
