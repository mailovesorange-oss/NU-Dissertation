Large Language Model (LLM)-Based Anomaly Detection in U.S. Federal COVID-19 Procurement
---
## Project Overview

This repository contains the Python code, Jupyter Notebooks, and supporting documentation for my doctoral dissertation in Data Science at National University.
The study uses a quantitative, non-experimental comparative research design to evaluate the effectiveness of traditional machine learning and large language model (LLM) embedding-based approaches for detecting anomalies in U.S. federal procurement records associated with the COVID-19 pandemic.
The research examines whether different anomaly detection techniques identify unusual procurement transactions and whether combining structured procurement attributes with unstructured textual information improves detection performance.

## Research Objectives
The primary objectives of this study are to:
1.	Evaluate Principal Component Analysis (PCA) for anomaly detection using structured procurement data.
2.	Evaluate Isolation Forest for anomaly detection using structured procurement data.
3.	Evaluate Variational Autoencoders (VAEs) for anomaly detection using structured procurement data.
4.	Evaluate an embedding-based language model approach using unstructured procurement descriptions.
5.	Evaluate a hybrid approach combining structured features and text embeddings.
6.	Compare the detection performance of these approaches using statistical testing.

## Dataset
- Source: SAM.gov Data Bank — COVID-19 Report
- Dataset size: 150,000 procurement records
- Study period: March 13, 2020 through November 14, 2024
- Initial variables: 176
- Selected variables: 22 original procurement attributes retained for analysis, with additional engineered features developed during preprocessing.

The dataset includes structured procurement attributes such as:
- Action Obligation
- Base and All Options Value (Total Contract Value)
- Award Type
- Type of Contract
- Extent Competed
- Funding Department Name
- NAICS Code
- Product or Service Code
- Contract signing and performance dates

The study also examines two unstructured text fields:
- Description of Requirement
- Product or Service Description

The original dataset is publicly available through SAM.gov and is not included in this repository.

## Anomaly Detection Methods

### Method, Approach, and Primary Data
- Principal Component Analysis (PCA), Reconstruction-error-based anomaly detection, structured
- Isolation Forest, Isolation-based anomaly detection, structured
- Variational Autoencoder (VAE), Neural-network-based anomaly detection, structured
- LLM Embeddings, Semantic embedding-based anomaly detection, unstructured text
- Hybrid Model, Combination of structured features and text embeddings, structured and unstructured

## Experimental Design and Evaluation
Because verified anomaly labels are unavailable in the procurement dataset, the study uses synthetically injected anomalies to establish evaluation labels.

The experimental design includes:
- An 80/20 development and independent evaluation split.
- Data preprocessing and model fitting restricted to development records.
- Synthetic anomaly injection for evaluating detection performance.
- Multiple experimental replicates to assess performance and stability.
- Precision@k and Average Precision (AP) as primary evaluation metrics, with Recall@k reported descriptively.
- Friedman tests and Nemenyi post-hoc comparisons for evaluating differences among anomaly detection methods.

## Software and Tools

The research is conducted primarily in Python using Jupyter Notebook. Libraries used or planned include:
- pandas and NumPy
- SciPy
- scikit-learn
- TensorFlow and Keras
- Sentence-BERT
- spaCy
- matplotlib
- seaborn
- scikit-posthocs

Exact dependency versions and reproducibility instructions will be documented as the experimental implementation progresses.

## Reproducibility

The study emphasizes reproducible computational research through version-controlled code, documented preprocessing procedures, controlled random seeds, and consistent experimental evaluation protocols.
Additional instructions for reproducing the experiments will be provided as the modeling and evaluation pipelines are finalized.

## Research Ethics

This research uses publicly available U.S. federal procurement records. The National University Institutional Review Board (IRB) has reviewed the project and determined that IRB oversight was not required because the study does not constitute human-subjects research.
The study also considers potential representation and algorithmic biases associated with procurement characteristics and pretrained language models.

## Project Status

Status: Dissertation research and experimental implementation in progress.

The repository will be updated as data preparation, anomaly detection experiments, statistical analyses, and dissertation documentation are completed.

## Author

Mai Drummond, Doctoral Candidate, PhD in Data Science
National University

## Disclaimer

This repository supports independent academic research. The identification of anomalous procurement records does not, by itself, establish fraud, misconduct, or improper contracting activity.
