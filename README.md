# Grapheme-to-Phoneme Sequence Modelling

This project implements and evaluates LSTM encoder–decoder models for grapheme-to-phoneme conversion using PyTorch. The task maps an input word, represented as a sequence of characters, to its corresponding sequence of phonemes.

## Model Architectures

Three decoder configurations are compared:

1. **No Context**
   The decoder is initialised using the final hidden and cell states produced by the encoder.

2. **Fixed Context**
   The final encoder hidden state is supplied to the decoder at every timestep as a fixed context vector.

3. **Attention**
   Dot-product attention is used to compute a dynamic context vector over the encoder hidden states at every decoding timestep.

## Repository Structure

```text
grapheme-to-phoneme-seq2seq/
├── notebook/
│   └── g2p-sequence-modelling.ipynb
├── report/
│   └── project_report.pdf
├── results/
│   ├── architecture_loss_curves.png
│   ├── attention_heatmap_dickensheets.png
│   ├── attention_heatmap_vulgarization.png
│   ├── length_analysis_grouped_bar_chart.png
│   ├── phoneme_length_distribution.png
│   ├── preliminary_training_loss_curves.png
│   └── word_length_distribution.png
├── data/
│   └── README.md
├── requirements.txt
└── README.md
```

## Technologies

* Python
* PyTorch
* NumPy
* pandas
* Matplotlib
* editdistance

## Running the Project

1. Clone this repository.
2. Install the dependencies:

```bash
pip install -r requirements.txt
```

3. Place the following files in the `data/` directory:

```text
g2p_train.csv
g2p_val.csv
g2p_test.csv
```

4. Open and run:

```text
notebook/g2p-sequence-modelling.ipynb
```

## Evaluation

The models are evaluated using phoneme error rate, exact-word accuracy, training behaviour and performance across different word-length groups.

The experiments compare how no-context, fixed-context and attention-based decoding influence prediction quality, particularly for longer and irregular words.
