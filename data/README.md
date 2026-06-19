# Dataset Setup

The dataset files used for this project are not included in this repository because they were provided for university coursework and may not be licensed for public redistribution.

To run the notebook, place the following files inside this `data/` directory:

```text
data/
├── g2p_train.csv
├── g2p_val.csv
├── g2p_test.csv
└── README.md
```

## Expected File Format

Each CSV file should contain the following columns:

```text
word,phonemes
```

Example:

```csv
word,phonemes
example,IH0 G Z AE1 M P AH0 L
```

The `word` column contains the written input word.

The `phonemes` column contains the corresponding phoneme sequence, with individual phonemes separated by spaces.

## Dataset Splits

* `g2p_train.csv` is used for model training.
* `g2p_val.csv` is used for validation and model comparison.
* `g2p_test.csv` is used for final evaluation.

## Important

The notebook expects these filenames and paths exactly:

```text
data/g2p_train.csv
data/g2p_val.csv
data/g2p_test.csv
```