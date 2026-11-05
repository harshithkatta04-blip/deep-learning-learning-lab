# Deep Learning Learning Lab

Hands-on experiments developed while studying deep learning. These are **learning projects, not production-ready applications**. Notebooks preserve the original training/evaluation output; reported metrics have **not been independently reproduced** for this repository.

## Contents

| Notebook | What it covers | Recorded results |
|---|---|---|
| [ANN: Cardiometabolic risk](01-ann-cardiometabolic/ann_cardiometabolic_risk.ipynb) | 8,000-row **synthetic** dataset; EDA, stratified train/validation/test splits, preprocessing, Keras Sequential vs Functional, class weighting, regularization, threshold selection, logistic-regression baseline, model saving/reloading | Final test: accuracy **84.13%**, precision **31.97%**, recall **46.99%**, F1 **0.3805**, average precision **0.3187**. **Not suitable for clinical use.** |
| [CNN: Cats vs Dogs](02-cnn-cats-vs-dogs/cats_vs_dogs_cnn.ipynb) | Image inspection, corruption/duplicate checks, stratified train/validation split, data pipelines, augmentation, a CNN with batch normalization, callbacks and final test evaluation | Final test: **74.80% accuracy**, **75.00% precision**, **74.40% recall**, **0.5279 loss** |
| [CNN: Speech Commands](03-cnn-speech-commands/speech_commands_cnn.ipynb) | 8 spoken commands, waveform-to-spectrogram preprocessing, CNN architecture iterations, confusion matrix, single WAV inference, model export | Final test: **88.17% accuracy**, **0.4645 loss**, on 1,200 test recordings |
| [RNN/LSTM/GRU Experiments](04-rnn-sequence-models/rnn_lstm_gru_experiments.ipynb) | Synthetic sequence classification, backpropagation through time, vanilla RNN vs LSTM vs GRU, gradient-flow and clipping experiments | Exploratory comparisons only; the final report cell includes **manually entered** figures, so it should not be treated as an automated benchmark |

## Setup and reproducibility notes

These notebooks were developed in different environments; use the original environment where possible. `requirements.txt` gives a **general dependency list**, not a tested lockfile. Install dependencies in a virtual environment, then open notebooks in Jupyter or Colab.

**Dataset inputs are not included.**

- **Cardiometabolic ANN:** Expects a synthetic CSV at an author's local Windows path in cell 2. Replace this with your own authorized dataset location (and document the dataset source before sharing publicly). Do not interpret synthetic-model performance as medical validation.
- **Cats vs Dogs:** Expects a zip in a specific Google Drive folder (`/content/drive/MyDrive/archive (3).zip`). Supply a suitably licensed copy of the dataset and update the path. The notebook is Colab-specific.
- **Speech Commands:** Downloads TensorFlow's `mini_speech_commands.zip` from the TensorFlow-hosted URL in the notebook when run in the expected directory structure.
- **RNN experiments:** Several standalone explorations occur in one notebook. Some cells redefine models and variables; sequential execution and independent experiment reproducibility need cleanup. A later report cell manually enters benchmark numbers.

### What to improve next

1. Replace hard-coded local paths with configurable paths or environment variables.
2. Record compatible environment versions and test notebooks from a clean runtime.
3. Add standalone `README.md` files explaining datasets, key findings and limitations per experiment.
4. For the RNN comparison, generate summary tables directly from experiment output rather than manually typed values.
5. Add error analysis, repeat runs with fixed random seeds, and include baseline comparisons where appropriate.

## Responsible usage

These are educational experiments. The health-risk notebook uses synthetic data and **must not be used for clinical decisions**. No large datasets, credentials or model checkpoints are distributed in this repository.
