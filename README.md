# NEU6630-Chohan
# Assignment 1.2: Benchmarking Molecular Structure Extraction

## Project Overview

This project uses MolScribe to test molecular structure extraction from six research papers provided by the instructor. The goal was to create a complete Python workflow that loads the files, runs the model, saves the predicted SMILES, and calculates evaluation metrics.

The project was completed in Google Colab using a T4 GPU.

## Files Used

The instructor provided six PDF files:

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

1. Open the Jupyter notebook in Google Colab.
2. Change the runtime to a T4 GPU.
3. Run the Environment Setup section.
4. Upload the six PDF files and the ground-truth CSV when prompted.
5. Run each remaining section in order.
6. Download the generated CSV and JSON result files.

## Results

The pipeline produced the following results:

- Ground-truth records: 222
- PDF pages processed: 104
- Successful inference calls: 104
- Failed inference calls: 0
- Non-empty SMILES predictions: 96
- Valid SMILES predictions: 81
- Average confidence score: 0.4114
- Exact matches: 0
- Exact-match rate: 0.0000
- Average best Tanimoto similarity: 0.006333

## Evaluation Method

Each predicted SMILES from a PDF page was compared with the confirmed molecules connected to the same paper.

The evaluation included:

- Exact matching using canonical SMILES
- Tanimoto similarity using Morgan fingerprints
- Prediction confidence scores
- Valid and non-empty SMILES counts

## Important Limitation

MolScribe is designed to process isolated molecular structure images. In this project, the model processed complete PDF pages that also contained text, tables, figures, and other information.

Because of this, the results should be viewed as page-level diagnostic results rather than true molecule-level accuracy. This likely explains the zero exact matches and low average Tanimoto similarity.

A future improvement would be to detect and crop individual molecular structures before sending the images to MolScribe.

## Output Files

- `molscribe_predictions.csv` contains the predicted SMILES and confidence scores.
- `metrics.csv` contains general pipeline results.
- `evaluation_results.csv` contains the detailed page-level evaluation.
- `evaluation_metrics.csv` contains the overall exact-match and Tanimoto metrics.
- `final_summary.json` contains the final benchmark summary.
- `requirements.txt` contains the required Python packages and versions.

## Tools Used

- Python
- Google Colab (Gemini Troubleshooting Assistant)
- MolScribe
- RDKit
- PyMuPDF
- pandas
- GitHub
