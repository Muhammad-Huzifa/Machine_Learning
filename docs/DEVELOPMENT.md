# Development and validation

Check active notebook JSON and Python syntax from the root:

```bash
python scripts/check_notebooks.py
```

Run the Adult Income correctness checks in its project environment:

```bash
cd projects/adult_income
python -m pip install -r requirements.txt
python -m unittest discover -s tests -v
```

The notebook check does not execute data downloads, model training, or API applications. Record the dataset, split, seed, configuration, package versions, and measured evaluation results for a real run. Changes to preprocessing must preserve training/inference consistency.
