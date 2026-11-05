Deep Learning: Applied Experiments
A collection of end-to-end deep learning experiments spanning tabular classification, computer vision, audio recognition, and sequence modeling. The notebooks cover data preparation, neural network design, training strategies, evaluation, and comparative experimentation using TensorFlow/Keras and PyTorch.
Projects
Project	Focus	Results recorded in notebook
[Cardiometabolic Risk Prediction — ANN](01-ann-cardiometabolic/ann_cardiometabolic_risk.ipynb)	Binary classification on a synthetic tabular dataset; exploratory analysis, stratified splitting, preprocessing, Keras Sequential and Functional APIs, class weighting, regularization, threshold tuning, and a logistic regression baseline	Test accuracy: 84.13%; F1: 0.3805; recall: 46.99%
[Cats vs Dogs — CNN](02-cnn-cats-vs-dogs/cats_vs_dogs_cnn.ipynb)	Image classification; dataset validation, image pipelines, augmentation, convolutional architecture, batch normalization, callbacks, and evaluation	Test accuracy: 74.80%; precision: 75.00%; recall: 74.40%
[Speech Command Recognition — CNN](03-cnn-speech-commands/speech_commands_cnn.ipynb)	Eight-class speech recognition; waveform processing, spectrogram features, model iterations, confusion-matrix analysis, and audio inference	Test accuracy: 88.17% across 1,200 recordings; test loss: 0.4645
[Sequence Modeling — RNN, LSTM & GRU](04-rnn-sequence-models/rnn_lstm_gru_experiments.ipynb)	Sequence classification; recurrent architectures, backpropagation through time, gradient behavior, and gradient clipping	Exploratory experiments; comparative figures in the final report are manually entered and are not an automated benchmark


The metrics above are recorded in the notebooks and have not been independently reproduced in a clean environment.
Technical Scope
- Frameworks: TensorFlow, Keras, PyTorch
- Data science: NumPy, pandas, scikit-learn, Matplotlib
- Modeling: Feedforward neural networks, convolutional neural networks, recurrent neural networks, LSTM, GRU
- Evaluation: Train/validation/test separation, classification metrics, confusion matrices, model comparisons, and threshold analysis
Repository Structure
deep-learning-learning-lab/
├── 01-ann-cardiometabolic/
│   └── ann_cardiometabolic_risk.ipynb
├── 02-cnn-cats-vs-dogs/
│   └── cats_vs_dogs_cnn.ipynb
├── 03-cnn-speech-commands/
│   └── speech_commands_cnn.ipynb
├── 04-rnn-sequence-models/
│   └── rnn_lstm_gru_experiments.ipynb
├── requirements.txt
└── README.md
Getting Started
1. Clone the repository and create a Python virtual environment.
2. Install the general dependencies:
   pip install -r requirements.txt
3. Launch Jupyter or open an individual notebook in Google Colab.
4. Configure the dataset path and runtime dependencies for that notebook before running its cells.
Environment note: The projects were developed in different environments. requirements.txt is a consolidated dependency reference, not a tested, version-locked environment. TensorFlow and PyTorch compatibility should be verified for the chosen Python version and platform.
Data and Reproducibility
Project	Dataset / execution requirements
Cardiometabolic ANN	Uses a synthetic CSV dataset (8,000 records). The notebook contains a local Windows file path that must be updated to a locally available dataset.
Cats vs Dogs	Uses an image dataset ZIP mounted from Google Drive in Colab. Provide the dataset separately and adjust the archive path.
Speech Commands	Retrieves the TensorFlow-hosted mini Speech Commands dataset from the URL referenced in the notebook.
RNN/LSTM/GRU	Contains multiple independent experiments with reused model/variable names. Execute the relevant sections in sequence; the final comparison table is illustrative rather than programmatically generated.


Datasets and large trained model files are not included in this repository. Refer to the notebook cells for preprocessing and training configurations.
Scope and Limitations
These experiments document model development and evaluation, rather than production deployment. Results may vary across library versions, hardware, random seeds, and dataset preparation. The cardiometabolic dataset is synthetic; its results do not constitute clinical validation and the model must not be used for medical decisions.
Author
Harshith Katta
GitHub: @harshithkatta04-blip
