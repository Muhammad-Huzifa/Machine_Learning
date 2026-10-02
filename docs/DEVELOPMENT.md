# Development and validation

## Source checks

```bash
python scripts/check_notebooks.py
```

This parses every active notebook and checks Python syntax. It does not execute original external-data or framework experiments.

## Self-contained lesson execution

Install `requirements/validation.txt` and run from the repository root:

```bash
python scripts/execute_lessons.py
python scripts/execute_lessons.py --report artifacts/lesson_execution.json --output-dir artifacts/executed
```

The manifest `docs/NEW_LESSONS.json` selects the eight complete new lessons. Each runs in a fresh Python kernel using the command's interpreter, with a 180-second limit per cell and single-threaded numerical libraries. Failures stop execution. Source notebook outputs remain empty; optional reports/executed copies go into ignored `artifacts/`. Use `--only` with a manifest path for a focused rerun. Restart interactive kernels before validation.

GitHub Actions has a dedicated CPU lesson job that runs full Jupyter execution. Other checks retain their existing scope.

## Local validation — 2 October 2026

All eight new lessons / 26 code cells passed in fresh CPU Python processes with IPython display capture. This environment blocks Jupyter socket connections, so local execution used direct cell execution; the repository command and CI perform full kernel execution.

| Dependency | Local version |
| --- | --- |
| Python | 3.12.14 |
| numpy | 2.3.5 |
| pandas | 2.2.3 |
| scikit-learn | 1.8.0 |
| matplotlib | 3.10.8 |

The lessons check training-only imputer statistics, unseen-category inference, normalized probabilities, and restored pipeline predictions. Train/test splitting and cross-validation keep test observations out of fitting and selection. Educational scores are printed when executed rather than published as benchmark claims.

Run the five existing Adult Income checks in the project environment:

```bash
cd projects/adult_income
python -m pip install -r requirements.txt
python -m unittest discover -s tests -v
```

Original salary/Titanic runs, a real Adult dataset benchmark, and optional API/UI execution were not repeated in this expansion.
