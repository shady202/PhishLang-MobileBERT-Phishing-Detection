# PhishLang: Phishing Page Detection

Deep-learning coursework project for classifying webpage text as benign or phishing content. The project explores a MobileBERT-based sequence classifier, dataset preparation, model training, and evaluation.

## Project Status

This repository is a research and coursework artifact. The main experiment is documented in [`assignment (5).ipynb`](../assignment%20(5).ipynb). It was authored for Google Colab and currently contains notebook cells that expect files mounted from Google Drive. It is not yet a packaged production service.

## Repository Layout

```text
assignment/
|-- assignment (5).ipynb       # End-to-end experiment notebook
|-- src/model/                 # Lightweight tokenizer/model configuration files
|-- phishlang_clientside_app/  # Screenshots from the client-side prototype
|-- results/                   # Training outputs and TensorBoard artifacts
|-- training_data/             # Local generated data; ignored by Git
|-- benign_samples/            # Local raw samples; ignored by Git
`-- phish_samples/             # Local raw samples; ignored by Git
```

## Why the Data Is Not Committed

The local dataset and generated training files are too large for a normal GitHub repository and may contain third-party webpage content. They are intentionally excluded by `.gitignore`. Do not commit scraped pages, credentials, authentication tokens, private data, or model checkpoints.

To reproduce the experiment, obtain an appropriately licensed dataset separately, place it under `training_data/`, and update the paths in the notebook from Google Drive paths to your local or cloud workspace.

## Local Setup

1. Create a Python 3.10+ environment.
2. Install the notebook dependencies:

   ```bash
   python -m pip install -U pip
   python -m pip install -r requirements.txt
   ```

3. Open `assignment (5).ipynb` in Jupyter or VS Code.
4. Run the environment and data-preparation sections first, then run the training and evaluation sections.

The notebook installs a CPU build of PyTorch by default. For GPU training, install the PyTorch build appropriate for your CUDA version before running the notebook.

## Reproducibility Notes

- The notebook uses the `google/mobilebert-uncased` checkpoint from Hugging Face.
- Training can require substantial memory and storage.
- Results depend on the dataset version, random seeds, package versions, and available hardware.
- The checked-in `src/model/` files are tokenizer metadata only; no complete model checkpoint is included.

## Responsible Use

This project is for defensive security research and education. Use datasets only when you have permission to process them. Do not deploy the model as the sole decision-maker for blocking websites, and do not use captured credentials or live phishing pages for testing.

## Future Improvements

- Replace hard-coded Colab paths with configurable command-line or environment-based paths.
- Add a pinned environment file and a small licensed sample dataset for smoke tests.
- Export evaluation metrics and confusion matrices as reproducible artifacts.
- Add automated tests for preprocessing and inference.
- Extract reusable training and inference code from the notebook into `src/`.