# Machine Learning

A collection of 15 classical ML notebooks and an end-to-end Adult Income classification project. Learn regression, preprocessing, evaluation, classical classifiers, clustering, PCA, tuning, and persistence. Neural networks and detection lessons live in the separate [Deep Learning collection](https://github.com/Muhammad-Huzifa/deep-learning).

## Learning path

| Section | Lessons | Topics |
| --- | --- | --- |
| [Foundations](notebooks/01_machine_learning/README.md) | 7 | Linear/polynomial/logistic regression and SVR |
| [Modeling workflow](notebooks/02_modeling_workflow/README.md) | 2 | Pipelines, missing values, encoding, metrics, cross-validation |
| [Classical classifiers](notebooks/03_classical_models/README.md) | 3 | KNN, SVM, trees, ensembles, TF-IDF and Naive Bayes |
| [Unsupervised learning](notebooks/04_unsupervised_learning/README.md) | 2 | K-means, DBSCAN, PCA |
| [Model selection](notebooks/05_model_selection/README.md) | 1 | Hyperparameter search and pipeline persistence |

New to ML? Start with the regression foundations, then follow the modeling workflow before comparing models. For a path that needs no external dataset files, use the [eight self-contained lessons in the notebook catalog](notebooks/README.md). Each includes objectives, explanations, examples, and practice.

## Setup

Use Python 3.11 or 3.12:

```bash
git clone https://github.com/Muhammad-Huzifa/machine-learning.git
cd machine-learning
python -m venv .venv
```

| Terminal | Activate the environment |
| --- | --- |
| Windows Command Prompt | `.venv\Scripts\activate.bat` |
| Windows PowerShell | `.\.venv\Scripts\Activate.ps1` |
| Windows Git Bash | `source .venv/Scripts/activate` |
| Linux/macOS | `source .venv/bin/activate` |

```bash
python -m pip install -r requirements.txt
jupyter lab
```

Select the environment's Python kernel, restart it, and run the chosen notebook from top to bottom. The eight new lessons use small generated, handcrafted, or built-in datasets; after dependency installation, they need no download or GPU. Read [the dataset guide](docs/DATASETS.md) for the original salary, Titanic, patient-record, and Adult inputs.

## Adult Income project

```bash
cd projects/adult_income
python -m pip install -r requirements.txt
python scripts/download_data.py --help
python train.py --help
python predict.py --help
```

The [project README](projects/adult_income/README.md) covers UCI data preparation, training, saved pipelines, prediction, and optional FastAPI/Streamlit applications. Install the optional requirements when running those applications.

## Structure

| Path | Purpose |
| --- | --- |
| `notebooks/01_machine_learning/` | Seven preserved foundation lessons |
| `notebooks/02_modeling_workflow/` | Preprocessing and evaluation |
| `notebooks/03_classical_models/` | Classical and text classifiers |
| `notebooks/04_unsupervised_learning/` | Clustering and PCA |
| `notebooks/05_model_selection/` | Tuning and persistence |
| `projects/adult_income/` | Training, prediction, and optional serving |
| `data/`, `artifacts/` | Input guides and ignored local outputs |
| `requirements/`, `scripts/`, `docs/` | Environments, checks, and provenance |

## Validation

```bash
python -m pip install -r requirements/validation.txt
python scripts/check_notebooks.py
python scripts/execute_lessons.py
```

The execution command runs the eight new lessons in fresh kernels without writing outputs into source notebooks. GitHub Actions runs this command and the five existing Adult Income tests. All 26 new lesson code cells passed local CPU execution; the original seven notebooks are preserved. These educational runs do not establish a real Adult benchmark or validate the optional API/UI. See [development notes](docs/DEVELOPMENT.md) and [source provenance](docs/SOURCE_MAP.md).

Muhammad Huzifa — [GitHub](https://github.com/Muhammad-Huzifa)
