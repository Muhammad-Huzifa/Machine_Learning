# Reproduction notes

The original report describes earlier experiment results. The underlying original model files, result CSVs, and exact environment are not in this repository, so those numerical claims have not been independently reproduced here.

The current workflow normalizes input values, splits rows before fitting preprocessing, and persists the fitted preprocessing with the classifier. Previously, single-row `get_dummies(..., drop_first=True)` could discard every supplied category, making inference differ from training.

Run `train.py` to produce metrics for the current implementation. Record the data source, train/test row counts, seed, estimator, command, and package versions. Do not use synthetic test-fixture results as Adult benchmark scores.

The original numbered exploration scripts came from `ML-End-to-End-project`, source commit `7b1eb1993b9ed1f3d8b7de4f14f041fedea1fe64`. That duplicate repository has been retired; its history is in the verified source backup supplied to the owner. Current supported commands are `train.py` and `predict.py`.
