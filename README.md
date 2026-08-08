# Predicting Stellar Class

A supervised machine-learning project for classifying astronomical observations using photometric, positional, redshift, and derived features.

## Project Objective

The task is to predict the target `class` from structured astronomical features. The workflow explores the data, cleans it, engineers/uses relevant variables, trains a Random Forest classifier, and tunes the model.

## Data

The notebook works with columns including:

- `alpha`
- `delta`
- `u`
- `g`
- `r`
- `i`
- `z`
- `redshift`
- `spectral_type`
- `galaxy_population`
- `class` — target

The data include astronomical categories such as galaxies and other stellar/extragalactic classes represented in the target variable.

## Workflow

1. Load and inspect the dataset.
2. Clean and prepare columns.
3. Explore feature distributions.
4. Separate predictors and target.
5. Train a `RandomForestClassifier`.
6. Tune the estimator using randomized hyperparameter search.
7. Evaluate the best estimator on held-out data.

## Model

The final workflow uses a **Random Forest classifier** with hyperparameters selected through `RandomizedSearchCV`.

## Recorded Result

The notebook records held-out accuracy of approximately:

**95.996%**

```text
Accuracy ≈ 0.9599607402
```

This is the score produced by the current notebook split and should not be interpreted as an external benchmark unless evaluated under an independently defined competition/test protocol.

## Repository Files

- `data_cleaning.ipynb` — data preparation
- `Dash001.ipynb` — modeling and evaluation
- `README.md`

## Tech Stack

- Python
- Jupyter Notebook
- Pandas
- NumPy
- scikit-learn
- Matplotlib / visualization tools

## Limitations

- The reported result is tied to the notebook's current train/test procedure.
- A stronger version should document class balance and per-class performance.
- Accuracy alone can hide minority-class errors.
- Repeated cross-validation would provide a more reliable uncertainty estimate.

## Future Improvements

- Add confusion matrix and per-class F1-score.
- Add stratified cross-validation.
- Compare with gradient boosting / LightGBM.
- Inspect feature importance.
- Add calibration analysis.
- Add explicit dataset citation and license.

## Author

**Divyadarshee Dash**
