# GNN-protein-classification

This project explores the use of Graph Neural Networks (GNNs) for protein structure classification using the TUDataset from PyTorch Geometric. The task is to distinguish between enzymes and non-enzymes based on graph representations of proteins.

## 🧬 Dataset

- **Source**: TUDataset via PyTorch Geometric
- **Graphs**: 1113 protein graphs
- **Nodes**: Amino acids
- **Edges**: Pairs of amino acids < 0.6 nm apart
- **Classes**: Enzyme or Non-enzyme

## 🧪 Methods and Techniques

### 🔁 Data Preprocessing
- **Cayley Graph Propagation** to alleviate over-squashing and improve message passing.
- **Feature Augmentation** via dropout and noise injection.
- **Normalization** and **Imbalance Handling**.

### 🧠 Architectures Used
- **GCN** (Graph Convolutional Network)
- **GIN** (Graph Isomorphism Network)

Each model includes:
- 3 GNN layers
- Batch normalization
- Global mean pooling
- Dropout
- Fully connected classifier

### ⚙️ Hyperparameter Tuning
- Grid search over dropout rate, learning rate, hidden dimensions, etc.
- Optimizers: Adam, AdamW
- Best accuracy: **GIN with 76% test accuracy**

### 📊 Evaluation Metrics
- Test accuracy
- Loss curves
- Model comparisons pre- and post-hyperparameter tuning

## 📁 Files

- `3_Graph_Classification.ipynb` – Main code notebook with experiments and results
- `GNNs_Report.pdf` – Detailed write-up with architecture explanations and analysis

## 📦 Installation

```bash
git clone https://github.com/KonouzA/GNN-protein-classification.git
cd GNN-protein-classification
