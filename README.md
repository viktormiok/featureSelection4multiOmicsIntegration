![](https://img.shields.io/badge/language-R_and_Python-orange.svg) ![version](https://img.shields.io/badge/GiHub_version-1.1.0-519dd9) ![GitHub code size in bytes](https://img.shields.io/github/languages/code-size/viktormiok/AstrocytesHeterogenityARC) ![GitHub issues](https://img.shields.io/github/issues/viktormiok/AstrocytesHeterogenityARC)

# featureSelection4multiOmicsIntegration

**Feature Selection for Multi-Omics Data Integration**, the repository presents a statistical workflow for feature selection in multi-omics datasets. The workflow is demonstrated using adrenocortical carcinoma (ACC) genomics data, integrating eight different methods from three categories: **supervised methods, factor analysis, and network models**. The aim is to identify biologically relevant features across multiple omics layers, facilitating a holistic understanding of complex biological processes.

# Abstract 
Multi-omics data are collections of data from various categories of biomolecules belonging to a single sample or individual, collected using different techniques for each type
of biomolecule. Multi-omics data have become ubiquitous thanks to the advancement of
biomolecular research technologies, but many statistical methods remain on single-omics
data analysis, which leads to a poor overall understanding of complex biological processes. In
this thesis, we demonstrated a statistical workflow to select features from the multi-omic
adrenocortical carcinoma (ACC) genomics data, using eight different methods from three
categories: Supervised methods, Factor analysis, and Network models. We concluded that
features selected using Factor analysis and Network models were more similar to each other,
with Supervised methods selecting a more different set of features.

# Table of Contents

- [Introduction](#introduction)
- [Methods](#methods)
- [Results](#results)
- [Discussion](#discussion)
- [Limitations](#Limitations)
- [Future Prospects](#Future_Prospects)
- [References](#References)

# Introduction

Multi-omics data combine information from various biomolecular categories (e.g., genomics, proteomics, metabolomics) collected from the same biological samples. Integrated analysis of such data enables a holistic view of biological processes, with applications in disease research and nutrition science. This thesis develops and demonstrates a statistical workflow for feature selection in multi-omics data, using ACC cohort data as a case study [Zhuang_202...ter thesis | PDF].

# Methods
Eight feature selection techniques are implemented, grouped into three categories:

- **Supervised Methods:** Penalised regression (lasso, elastic net), group-adaptive penalised regression (Squeezy, Xtune), and Globaltest.

- **Factor Analysis:** FABIA, robust FABIA ensemble (Superbiclust), Multiple Factor Analysis (MFA), Multi-Omics Factor Analysis (MOFA).

- **Network Models:** Gaussian Graphical Models (GGM, via rags2ridges).
  
All methods are applied to high-dimensional ACC data, including RNA sequencing, microRNA sequencing, proteomics, and mutation data. Data processing steps include standardisation, log/square-root transformation, and harmonisation of variable names. [Zhuang_202...ter thesis | PDF]

# Results

**Supervised Methods:** Penalised regression models (Glmnet) and Globaltest identified features associated with clinical outcomes. Group-adaptive methods (Squeezy, Xtune) showed limited benefit over standard penalised regression.

**Factor Analysis:** FABIA and MOFA revealed latent structures and biclusters/factors, with robust ensemble methods improving stability. MFA highlighted major sources of variance across omics layers.

**Network Models:** GGM visualised relationships and communities among features, identifying hubs and highly connected variables.

**Pathway Analysis:** Gene Ontology (GO) profiling was performed for selected features, using clusterProfiler and multiMiR. [Zhuang_202...ter thesis | PDF]

# Discussion

The thesis compares the overlap and differences in selected features across methods. Supervised and unsupervised approaches often select distinct sets of features, with multi-omics-aware methods providing more balanced selections across datasets. The workflow demonstrates the importance of method choice and external information in multi-omics feature selection. [Zhuang_202...ter thesis | PDF]
