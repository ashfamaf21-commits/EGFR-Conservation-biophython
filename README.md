# EGFR-Conservation-biophython
# Cross-Species EGFR Conservation Analysis Using Biopython and Machine Learning

## Overview

This project analyzes the conservation of the Epidermal Growth Factor Receptor (EGFR) protein across selected vertebrate species.

The workflow combines sequence retrieval, multiple sequence alignment, pairwise sequence identity analysis, conservation analysis, phylogenetic analysis, and a simple machine-learning extension.

Biopython was used for sequence retrieval and sequence handling, while MAFFT was used for multiple sequence alignment.

A simple exploratory machine-learning analysis using PCA and K-means clustering was also included to compare sequence-derived features among species.

---

## Objectives

The main objectives of this project were to:

- Retrieve EGFR protein sequences from NCBI
- Compare EGFR sequences across different species
- Perform multiple sequence alignment
- Calculate pairwise sequence identity
- Identify conserved positions
- Explore evolutionary relationships
- Extract simple sequence-based features
- Apply PCA and K-means clustering

---

## Species Included

The following species were analyzed:

- Homo sapiens
- Pan troglodytes
- Mus musculus
- Rattus norvegicus
- Bos taurus
- Danio rerio

---

## Workflow

NCBI Protein Database  
↓  
EGFR Sequence Retrieval using Biopython Entrez  
↓  
FASTA Sequence Collection  
↓  
Multiple Sequence Alignment using MAFFT  
↓  
Pairwise Sequence Identity Calculation  
↓  
Conserved Position Analysis  
↓  
Sequence Feature Extraction  
↓  
PCA  
↓  
K-means Clustering  

---

## Tools and Technologies

- Python
- Biopython
- NCBI Entrez
- MAFFT
- Pandas
- Matplotlib
- scikit-learn
- Google Colab

---

## Sequence Retrieval

EGFR protein sequences were retrieved from the NCBI Protein database using the Biopython Entrez module.

The retrieved protein sequences were saved in FASTA format for further analysis.

---

## Multiple Sequence Alignment

MAFFT was used to perform multiple sequence alignment of EGFR protein sequences from all selected species.

The aligned sequences were then used for:

- Pairwise sequence identity calculation
- Conserved residue analysis
- Sequence comparison
- Phylogenetic analysis

---

## Pairwise Sequence Identity

Pairwise percentage identity was calculated between the aligned EGFR protein sequences.

The results were saved in:

`egfr_identity_matrix.csv`

This matrix allows comparison of EGFR sequence similarity between all selected species.

---

## Conserved Position Analysis

Conserved positions were identified by examining each column of the multiple sequence alignment.

A position was considered conserved when the same amino acid was present across all analyzed species without gaps.

This provided a simple estimate of EGFR sequence conservation.

---

## Sequence-Based Features

The following sequence-based features were extracted:

- Sequence length
- Percentage identity to human EGFR
- Number of alignment gaps
- Percentage of hydrophobic amino acids

These features were used for the exploratory machine-learning analysis.

---

## Machine-Learning Extension

A simple unsupervised machine-learning analysis was performed using sequence-derived features.

### Principal Component Analysis

Principal Component Analysis (PCA) was used to reduce the sequence feature data into two dimensions.

This allowed visual comparison of the species based on their sequence characteristics.

### K-means Clustering

K-means clustering was applied to group species based on the extracted EGFR sequence features.

The clustering analysis was used only as an exploratory comparison and not as a replacement for phylogenetic analysis.

---

## Files in This Repository

- `EGFR_Conservation_Analysis.ipynb`
- `egfr_sequences.fasta`
- `egfr_aligned.fasta`
- `egfr_identity_matrix.csv`
- `egfr_sequence_ml_features.csv`
- `README.md`

---

## File Descriptions

### EGFR_Conservation_Analysis.ipynb

Main notebook containing:

- Sequence retrieval
- FASTA handling
- Multiple sequence alignment
- Sequence identity analysis
- Conservation analysis
- Feature extraction
- PCA
- K-means clustering

### egfr_sequences.fasta

Contains EGFR protein sequences retrieved from NCBI.

### egfr_aligned.fasta

Contains the multiple sequence alignment generated using MAFFT.

### egfr_identity_matrix.csv

Contains pairwise percentage identity values between EGFR sequences.

### egfr_sequence_ml_features.csv

Contains the sequence-derived features together with PCA coordinates and K-means cluster assignments.

---

## Key Skills Demonstrated

This project demonstrates practical experience with:

- Bioinformatics
- Protein sequence analysis
- Biological database access
- NCBI Entrez
- Biopython
- FASTA file handling
- Multiple sequence alignment
- MAFFT
- Pairwise sequence comparison
- Conservation analysis
- Basic phylogenetic analysis
- Feature extraction
- Data preprocessing
- Principal Component Analysis
- K-means clustering
- Scientific data visualization

---

## Interpretation

The analysis allows EGFR conservation to be compared across different vertebrate species.

Closely related species are expected to show higher sequence similarity, while more evolutionarily distant species may show greater sequence differences.

The PCA and K-means analyses provide an additional exploratory view of how the species group based on simple sequence-derived characteristics.

---

## Limitations

- Only a small number of species were included.
- The first EGFR protein sequence returned by the database search was used.
- The sequence-derived features used for PCA and clustering are simple.
- PCA and K-means do not replace phylogenetic analysis.
- Sequence similarity alone does not confirm functional similarity.
- Protein structure and domain-specific conservation were not investigated in detail.

---

## Future Improvements

Possible future improvements include:

- Including more species
- Comparing EGFR functional domains separately
- Performing kinase-domain conservation analysis
- Adding protein structure comparison
- Using conserved domain databases
- Performing more detailed phylogenetic analysis
- Adding additional sequence descriptors
- Using more advanced dimensionality-reduction methods
- Comparing sequence conservation with structural conservation

---

## Purpose

This project was developed as a bioinformatics portfolio project to demonstrate practical use of biological databases, Biopython, sequence analysis, external alignment tools, and simple machine-learning techniques.

---

## Disclaimer

This project was developed for educational and research-training purposes.

The analyses are computational and should not be interpreted as experimental evidence of EGFR function or evolutionary relationships.
