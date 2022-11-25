# Using MLflow receipe (seems to be a recommended setup) to set up the machine learning pipeline

This machine learning pipeline allows us to repeat model training process with simple Databricks API calls or MLflow API calls. (I'm still trying to sort out the details.)

## `recipe.yaml`

This is the main configuration file for an MLflow Recipe.

Dependencies
- variables defined in notebooks in the `profiles/` directory (e.g., local.yaml)

Important details in the file
- target column
- positive class label
- primary metric used to evaluate the model
- steps of the model - ingest, split, transform, train, evaluate, register

To Do
- [ ] Set up dataset to use for automatic predictions and model scoring
- [ ] RE-CONFIGURE how data is split. (We need specific styles of data splits eventaully)

Fixes
- [ ] If using a cross validator works, I think I should only split the data into training and testing (no validation)

## `profiles/`

### `local.yaml`

Defined in this file
- Experiment information (name, tracking uri - storage loc for experiment, artifact location)
- Ingestion configuration

To Do
- [ ] Set up scoring data if I want to evaluate data at the same time

## `steps/`

### `ingest.py`

- [ ] Can I use this script to "balance" the data? Parse out an equal number of positive and negative samples.

### `transformer.py`

### `train.py`

Script has one method: `estimator_fn()`
- This script creates a decision tree classifier and uses a dataframe passed as an input to train a model with cross validation
