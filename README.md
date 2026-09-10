# PhishLang: Deep Learning for Intrusion Detection

A portfolio project for detecting phishing webpages from extracted webpage text. It combines dataset preparation, exploratory analysis, and a MobileBERT-based text-classification experiment.

## What This Demonstrates

- Practical handling of imbalanced security data
- Text preprocessing for webpage content
- Transfer learning with a transformer classifier
- Model training and evaluation in an interactive notebook
- Awareness of responsible-use and data-handling concerns in security research

## Start Here

Open [`assignment (5).ipynb`](assignment%20(5).ipynb). The notebook documents the complete experiment, including environment checks, data preparation, training, and evaluation.

The notebook was originally developed for Google Colab and currently uses Google Drive paths. It is therefore a documented experiment rather than a one-command application. The project-specific setup and reproducibility notes are in [`assignment/README.md`](assignment/README.md).

## Repository Contents

| Path | Purpose |
| --- | --- |
| `assignment (5).ipynb` | Main experiment notebook |
| `assignment/README.md` | Detailed setup, limitations, and responsible-use notes |
| `assignment/requirements.txt` | Python dependency ranges |
| `assignment/src/model/` | Tokenizer metadata used by the experiment |
| `assignment/phishlang_clientside_app/` | Client-side prototype screenshots |

Large local datasets, scraped samples, recordings, generated logs, and model checkpoints are excluded from version control. They are not required to understand the approach and should only be shared when licensing and privacy have been verified.

## Limitations

- The current notebook has hard-coded Colab/Google Drive paths.
- No complete trained model checkpoint or small public smoke-test dataset is included.
- Reproducibility depends on the dataset version, package versions, random seeds, and hardware.
- This experiment should not be used as the sole control for blocking or labeling real websites.

## Roadmap

The next engineering steps are to extract reusable preprocessing and inference code into `src/`, replace hard-coded paths with configuration, add a small licensed test fixture, pin a tested environment, and add automated evaluation checks.

## Responsible Use

Use this project only for defensive security research and education. Do not collect, store, or publish credentials, private data, or live phishing infrastructure. Obtain permission and verify licensing before redistributing webpage samples.