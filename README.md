# Machine Learning: original notebooks

This repository retains the original learning notebooks. Their organized versions are available in the [Machine Learning and Deep Learning collection](https://github.com/Muhammad-Huzifa/Neural-Networks-and-Deep-Learning-Using-Pytorch-and-Tensor-Flow/tree/codex/consolidate-ml-deep-learning), with topic indexes, separate framework environments, dataset instructions, and a migration source map.

## Use the organized collection

While the consolidation pull request is under review, clone its branch:

```bash
git clone --branch codex/consolidate-ml-deep-learning https://github.com/Muhammad-Huzifa/Neural-Networks-and-Deep-Learning-Using-Pytorch-and-Tensor-Flow.git
cd Neural-Networks-and-Deep-Learning-Using-Pytorch-and-Tensor-Flow
python -m venv .venv
```

Activate the environment using `.venv\Scripts\activate.bat` in Windows Command Prompt, `.\.venv\Scripts\Activate.ps1` in PowerShell, `source .venv/Scripts/activate` in Git Bash, or `source .venv/bin/activate` on Linux/macOS.

```bash
python -m pip install -r requirements/base.txt
jupyter lab
```

TensorFlow/PyTorch lessons need the additional environment described in the collection README. The original notebooks here may refer to local datasets or machine-specific paths; use the migrated versions for the current organization.

## Original notebook index

| Original notebook |
| --- |
| [Logistic Regression_from_Scratch](Logistic%20Regression_from_Scratch.ipynb) |
| [Logistic-Regression_with-Real_DataSets](Logistic-Regression_with-Real_DataSets.ipynb) |
| [Logistic_Regression_From_Scratch_With_Real_Data_Set](Logistic_Regression_From_Scratch_With_Real_Data_Set.ipynb) |
| [Mutiple_Linear_Regression_from_Scratch](Mutiple_Linear_Regression_from_Scratch.ipynb) |
| [Polynomial_Linear_Regression_With_Degree_2,3,4,5](Polynomial_Linear_Regression_With_Degree_2%2C3%2C4%2C5.ipynb) |
| [Simple_Linear_Regression_With_Cost_Function_Gradient_Descent](Simple_Linear_Regression_With_Cost_Function_Gradient_Descent.ipynb) |
| [Support_Vector_Regression](Support_Vector_Regression.ipynb) |

## Provenance

The consolidation keeps distinct implementations and records duplicate source cells. This source repository remains available during review; it has not been archived or deleted.

Muhammad Huzifa — [GitHub](https://github.com/Muhammad-Huzifa)
