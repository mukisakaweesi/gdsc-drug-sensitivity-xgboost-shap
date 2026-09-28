# Data

The raw data is not stored in this repository because of its size and the GDSC terms of use. Please download it from the source.

**Dataset:** Genomics of Drug Sensitivity in Cancer (GDSC), Kaggle version
**Link:** https://www.kaggle.com/datasets/samiraalipour/genomics-of-drug-sensitivity-in-cancer-gdsc
**Original resource:** https://www.cancerrxgene.org/
**Shape used in the notebook:** 242,035 rows and 19 columns

## Download steps

1. Sign in to Kaggle and open the link above.
2. Download the dataset and unzip it.
3. Take the merged file (`GDSC_DATASET.csv`, the one with the 19 columns listed below), rename it to `genomic_data.csv`, and put it in the repository root next to `gdsc_drug_sensitivity.ipynb`. The notebook reads it with `pd.read_csv("genomic_data.csv")`.

With the Kaggle CLI (needs a Kaggle API token):

```bash
kaggle datasets download -d samiraalipour/genomics-of-drug-sensitivity-in-cancer-gdsc --unzip
```

## Columns

COSMIC_ID, CELL_LINE_NAME, TCGA_DESC, DRUG_ID, DRUG_NAME, LN_IC50 (target), AUC, Z_SCORE, GDSC Tissue descriptor 1, GDSC Tissue descriptor 2, Cancer Type (matching TCGA label), Microsatellite instability Status (MSI), Screen Medium, Growth Properties, CNA, Gene Expression, Methylation, TARGET, TARGET_PATHWAY.

AUC and Z_SCORE are calculated from the same dose-response curve as LN_IC50. Do not use them as features if you want an honest estimate of predictive performance.
