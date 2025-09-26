# Automated Pathway Reconstruction using Attention Guided Graph Neural Network (AG-GNN)

This repository contains a Graph Neural Network (GNN) pipeline for protein analysis, implemented in PyTorch and PyTorch Geometric. The notebook protein_gnn_final.ipynb provides an end-to-end workflow for protein-graph construction, model training, evaluation, and biological interpretation.

# 📌 Project Overview

Proteins can be represented as graphs, where:

Nodes → amino acids or residues

Edges → structural/chemical interactions (e.g., bonds, spatial proximity, PPI edges)

This project applies Graph Attention Networks (GATs) to protein-related tasks:

Node classification → predict functional properties of amino acids

Link prediction → infer residue interactions (protein–protein or within a protein)

Graph-level classification → predict overall protein properties

The pipeline also integrates biological pathway enrichment (using KEGG genes) to link predictions back to biological insights.

# ⚙️ Dependencies

Install required packages:

pip install torch torchvision torchaudio
pip install torch-geometric
pip install scikit-learn pandas numpy matplotlib networkx

# 📂 File Structure

protein_gnn_final.ipynb → main notebook with full pipeline

models/ → trained models saved as .pkl files (after running)

results/ → evaluation metrics, confusion matrices, plots

# 🚀 Usage

Open and run the notebook:

jupyter notebook protein_gnn_final.ipynb


The workflow includes:

Data preprocessing (convert protein/PPI data → graph format)

Model definition (custom GAT encoder, link predictor)

Training with PyTorch Geometric

Evaluation with scikit-learn metrics

Biological enrichment analysis

# Outputs generated:

Accuracy, precision, recall, F1-score → CSV files

Confusion matrices → images

Saved models → .pkl

# 🧩 Code Structure
# 🔹 Classes (3 total)

GATModel → Full Graph Attention Network model

GATEncoder → Encoder module for feature extraction

LinkPredictor → Predicts interactions (edges) between protein nodes

# 🔹 Functions (32 total)
Data & Graph Preparation

print_structure() → prints dataset structure

visualize_ppi_graph() → plots protein-protein interaction (PPI) network

add_node_embeddings() → assigns embeddings to nodes

convert_to_pyg_data() → converts raw dataset to PyTorch Geometric format

prepare_node_classification() → prepares data for node-level prediction

prepare_link_prediction() → prepares data for link prediction

# Training & Evaluation

train() → training loop

evaluate() → validation loop

evaluate_test() → test set evaluation

get_neg_edges() → negative sampling for link prediction

# Model Internals

__init__(), forward(), decode() → defined within GATModel, GATEncoder, and LinkPredictor

# Biological Analysis

fetch_kegg_pathway_genes() → fetches KEGG pathway gene sets

enrichment_analysis() → performs biological enrichment

jaccard() → computes Jaccard similarity between sets

(Additional utility functions handle preprocessing, evaluation metrics, and saving results.)

# 📊 Outputs

Metrics: Accuracy, precision, recall, F1-score (CSV)

Plots: Training curves, confusion matrices

Models: Trained GNNs saved as .pkl for reuse

Biological insights: Pathway enrichment results

# 🔮 Extensions

Experiment with alternative GNNs: GraphSAGE, GCN, GIN

Hyperparameter tuning (layers, heads, dropout)

Transfer learning across protein datasets

Deploy as a protein function prediction API

# Author

Pratyush Lenka 23BAI1470

(CSE-AIML) PRE-FINAL YEAR

VELLORE INSTITUTE OF TECHNOLOGY, CHENNAI
