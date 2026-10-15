# NEU6630-Chohan
# Assignment 1.2: Benchmarking Molecular Structure Extraction

## Project Overview

This project uses MolScribe to benchmark molecular structure extraction from six research papers provided by the instructor. MolScribe was used with instructor approval as the SMILES extraction tool for this assignment.

The goal was to create a simple Python pipeline that:

- Loads the provided benchmark files
- Converts the PDF pages into images
- Runs MolScribe on the page images
- Saves the predicted SMILES and confidence scores
- Calculates evaluation metrics
- Saves the results in CSV and JSON files

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

## Repository Files

This repository contains:

- `Assignment_1_2_Benchmarking_Code_Aurinder_Chohan.ipynb`
- `requirements.txt`
- `molscribe_predictions.csv`
- `metrics.csv`
- `evaluation_results.csv`
- `evaluation_metrics.csv`
- `final_summary.json`
- `.gitignore`
- `README.md`

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

1. Open the Jupyter notebook in Google Colab.
2. From the Colab menu, select `Runtime`.
3. Select `Change runtime type`.
4. Choose a T4 GPU as the hardware accelerator.
5. Run the Environment Setup section.
6. Upload the six PDF files and the original ground-truth CSV when prompted.
7. Run each remaining notebook section in order.
8. Download the generated CSV and JSON output files.

No API keys, passwords, credentials, or personal computer paths are required.

## Pipeline

The notebook follows this workflow:

```text
PDF files
→ PDF page images
→ MolScribe inference
→ Predicted SMILES and confidence scores
→ Evaluation metrics
→ CSV and JSON result files
