# NEU6630-Chohan
# Assignment 1.2: Benchmarking Molecular Structure Extraction

## Project Overview

This project uses MolScribe to benchmark molecular structure extraction from six research papers provided by the instructor. MolScribe was used with instructor approval as the SMILES extraction tool for this assignment.

The main goal was to build a Python pipeline that loads the provided files, converts the PDF pages into images, runs MolScribe, saves the predicted SMILES and confidence scores, and calculates evaluation metrics.

The project was completed in Google Colab using a T4 GPU.

## Input Files

The instructor provided the following PDF files:

- 1.pdf
- 2.pdf
- 4.pdf
- 6.pdf
- 16.pdf
- 19.pdf

The instructor also provided a CSV file containing 222 confirmed ground-truth SMILES records.

The original PDFs and ground-truth CSV are not included in this public repository.

## Notebook Sections

The notebook is organized into the following sections:

1. Environment Setup
2. Data Preparation and Setup
3. Model Setup
4. PDF Extraction
5. Inference Pipeline
6. Verify Inference Results
7. Metrics and Results
8. Eval Metrics
9. Results Summary
10. Download Submission Files

## How to Run the Project

1. Open the notebook in Google Colab.
2. Change the runtime type to a T4 GPU.
3. Run the Environment Setup section.
4. Upload the six PDF files and ground-truth CSV when prompted.
5. Run each remaining section in order.
6. Download the generated CSV and JSON output files.

No API keys, passwords, or personal computer paths are required.

## Pipeline

The notebook follows this general workflow:

```text
PDF files
→ PDF page images
→ MolScribe predictions
→ SMILES and confidence scores
→ Evaluation metrics
→ CSV and JSON results
