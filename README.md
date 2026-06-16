# Pothole Detection Using YOLO
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
## Overview

Road potholes pose significant challenges to transportation infrastructure, contributing to vehicle damage, increased maintenance costs, traffic disruptions, and road safety hazards. Traditional road inspection methods rely heavily on manual surveys, which are often time-consuming, labor-intensive, and inefficient for large road networks. 

This project aims to automate pothole detection using computer vision. Specifically, it explores and compares **several YOLO (You Only Look Once) models** to identify the most efficient and accurate approach for real-time and batch processing of road surface imagery.

## Methodology: The Fynesse Framework

This repository strictly adheres to the **Fynesse Framework** to ensure a reproducible, rigorous, and unbiased data science process. The workflow is divided into three core aspects:

1. **Access (`fynesse/access.py`):** Gaining access to street-level imagery and annotated pothole datasets, managing downloads from APIs, and overcoming potential data ingestion challenges.
2. **Assess (`fynesse/assess.py`):** Exploring the nature of the data *without* the final question in mind. This includes profiling image resolutions, checking bounding box annotation formats (e.g., YOLO format conversions), and understanding data distributions and lighting conditions.
3. **Address (`fynesse/address.py`):** Implementing the core analysis. For this project, this involves training, validating, and comparing the performance (mAP, inference speed) of multiple YOLO model architectures to detect potholes.

## Repository Structure

```text
├── notebooks/
│   └── potholes.ipynb   # Main interactive notebook demonstrating the pipeline
├── fynesse/
│   ├── access.py        # Data procurement and loading logic
│   ├── assess.py        # Data quality checks and EDA
│   ├── address.py       # YOLO model training, inference, and evaluation
│   ├── config.py        # Configuration management
│   └── defaults.yml     # Default configuration values (paths, YOLO hyperparameters)
├── tests/               # Comprehensive pytest suite
│   ├── test_access.py
│   ├── test_assess.py
│   └── test_address.py
├── pyproject.toml       # Poetry dependency management
└── README.md
