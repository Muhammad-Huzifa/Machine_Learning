# Dataset guide

| Input | Location | Lessons |
| --- | --- | --- |
| Original patient records | `data/tabular/patient_records.csv` | Patient-record logistic regression |
| External salary CSV | `data/tabular/salary_data.csv` | Simple/polynomial regression and SVR |
| External Titanic training CSV | `data/tabular/titanic_train.csv` | Titanic logistic regression |
| Synthetic arrays generated in the notebook | No download | Multiple regression and NumPy logistic regression |
| Official UCI Adult files | `projects/adult_income/data/` | Adult Income project |

See [input schemas](../data/tabular/README.md) and [Adult Income data instructions](../projects/adult_income/data/README.md). Keep each original dataset's attribution and terms. Use fresh notebook kernels and run only after its input files are available. The clinical-looking patient example is classroom code, not a validated medical tool.

## New self-contained lessons

These inputs are generated in the notebook or bundled with scikit-learn. No external file, dataset download, credentials, or GPU is required after installing dependencies.

| Lesson | Input |
| --- | --- |
| [Preprocessing and leakage-safe pipelines](../notebooks/02_modeling_workflow/01_preprocessing_and_pipelines.ipynb) | Generated mixed-type tabular data |
| [Classification metrics and cross-validation](../notebooks/02_modeling_workflow/02_metrics_and_cross_validation.ipynb) | Generated imbalanced binary classification |
| [K-nearest neighbors and SVM classification](../notebooks/03_classical_models/01_knn_and_svm_classification.ipynb) | Built-in Iris dataset |
| [Decision trees, random forests, and boosting](../notebooks/03_classical_models/02_decision_trees_and_ensembles.ipynb) | Built-in Wine dataset |
| [Text classification with TF-IDF and Naive Bayes](../notebooks/03_classical_models/03_text_classification_naive_bayes.ipynb) | Handcrafted weather/sports teaching sentences |
| [Clustering with K-means and DBSCAN](../notebooks/04_unsupervised_learning/01_clustering_kmeans_dbscan.ipynb) | Generated blobs and curved clusters |
| [PCA and dimensionality reduction](../notebooks/04_unsupervised_learning/02_pca_and_dimensionality_reduction.ipynb) | Built-in 8×8 handwritten digits |
| [Reproducible tuning and model persistence](../notebooks/05_model_selection/01_tuning_and_model_persistence.ipynb) | Generated regression data |

Built-in digits here are 8×8 images, not MNIST. Synthetic/handcrafted examples are teaching data; their scores do not validate a production model. Each supervised lesson keeps test data out of fitting and model/epoch selection. Clustering is explicitly exploratory.
