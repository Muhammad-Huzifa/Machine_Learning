# Machine Learning

Classical machine-learning lessons and an end-to-end Adult Income classification project. This repository contains NumPy, pandas, and scikit-learn work; neural-network and YOLO material is maintained in the separate [Deep Learning collection](https://github.com/Muhammad-Huzifa/Neural-Networks-and-Deep-Learning-Using-Pytorch-and-Tensor-Flow).

## Setup

Use Python 3.11 or 3.12:

```bash
git clone https://github.com/Muhammad-Huzifa/Machine_Learning.git
cd Machine_Learning
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

## Lesson order

| Order | Lesson |
| --- | --- |
| 1 | [01 simple linear regression](notebooks/01_machine_learning/01_simple_linear_regression.ipynb) |
| 2 | [02 multiple linear regression](notebooks/01_machine_learning/02_multiple_linear_regression.ipynb) |
| 3 | [03 polynomial regression](notebooks/01_machine_learning/03_polynomial_regression.ipynb) |
| 4 | [04 logistic regression numpy](notebooks/01_machine_learning/04_logistic_regression_numpy.ipynb) |
| 5 | [05 logistic regression patient records](notebooks/01_machine_learning/05_logistic_regression_patient_records.ipynb) |
| 6 | [06 logistic regression titanic](notebooks/01_machine_learning/06_logistic_regression_titanic.ipynb) |
| 7 | [07 support vector regression](notebooks/01_machine_learning/07_support_vector_regression.ipynb) |

Read [the dataset guide](docs/DATASETS.md) before opening a lesson. Salary and Titanic inputs are external; NumPy array lessons and the bundled patient CSV do not need those files.

## Adult Income project

```bash
cd projects/adult_income
python -m pip install -r requirements.txt
python scripts/download_data.py --help
python train.py --help
python predict.py --help
```

The [project README](projects/adult_income/README.md) covers UCI data preparation, training, saved pipelines, prediction, and optional FastAPI/Streamlit applications. Use the separate optional requirements only when running those applications.

## Structure

| Path | Purpose |
| --- | --- |
| `notebooks/01_machine_learning/` | Seven classical ML lessons |
| `projects/adult_income/` | Training, prediction, persistence, and optional serving |
| `data/tabular/` | Source CSV and external-input instructions |
| `requirements/` | Notebook environment |
| `scripts/` | Offline notebook checks |
| `docs/` | Inputs, development, and source provenance |

Notebook syntax and the NumPy regression lessons were checked. Adult Income has five preprocessing/persistence checks and synthetic CLI validation; those checks do not establish a real Adult benchmark. External dataset runs and optional API/UI execution are not claimed. See [development notes](docs/DEVELOPMENT.md).

Muhammad Huzifa — [GitHub](https://github.com/Muhammad-Huzifa)
