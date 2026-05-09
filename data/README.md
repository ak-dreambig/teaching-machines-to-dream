
# Data

This folder is for local data files when running notebooks locally.

No datasets are included in this repository. All datasets are publicly
available on Kaggle and should be downloaded from there.

## Required Datasets

| Dataset | Used In | Download |
|---------|---------|----------|
| Adult Census Income | TMD-01, TMD-06, TMD-07 | [Download from Kaggle](https://www.kaggle.com/datasets/uciml/adult-census-income) |
| Credit Card Fraud | TMD-02 | [Download from Kaggle](https://www.kaggle.com/datasets/mlg-ulb/creditcardfraud) |
| Intel Image Classification | TMD-04 | [Download from Kaggle](https://www.kaggle.com/datasets/puneet6060/intel-image-classification) |

## Local Setup

After downloading, place files in this structure:

```
data/
├── adult-census-income/
│   └── adult.csv
├── creditcardfraud/
│   └── creditcard.csv
└── intel-image-classification/
    └── seg_train/
        └── seg_train/
            ├── buildings/
            ├── forest/
            ├── glacier/
            ├── mountain/
            ├── sea/
            └── street/
```

Then update the file paths in each notebook accordingly.

When running on Kaggle, paths are set automatically and no
manual setup is needed.
