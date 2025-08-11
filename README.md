# Composer Classification using Deep Learning

This project uses deep learning models, including LSTMs and CNNs, to classify musical pieces by their composer. It provides a complete pipeline from data processing to model training, evaluation, and inference.

## 📝 Overview

The goal of this project is to build and evaluate different neural network architectures for their ability to distinguish the unique stylistic signatures of various classical composers. The current implementation focuses on six composers: Bach, Beethoven, Chopin, and Mozart.

## ✨ Features

  * Parses MIDI files to extract sequential note and chord data.
  * Implements a robust file-based data split (train/test) to prevent data leakage.
  * Trains and compares three different deep learning models:
      * A pure LSTM model
      * A pure 1D-CNN model
      * A hybrid CNN-LSTM model
  * Generates detailed evaluation reports, training history plots, and confusion matrices.

## 💾 Dataset

The dataset consists of MIDI files from six classical composers:

  * Johann Sebastian Bach
  * Ludwig van Beethoven
  * Frédéric Chopin
  * Wolfgang Amadeus Mozart

## ⚙️ Methodology

The project is structured into three modular Jupyter notebooks for a clear and reproducible workflow:

1.  **`01_Data_Preprocessing.ipynb`**: Loads all MIDI files, splits the dataset by song to create distinct training and test sets, processes the files into note sequences, builds a vocabulary, and saves the processed data.
2.  **`02_Model_Training_and_Evaluation.ipynb`**: Loads the preprocessed data, builds the three models (LSTM, CNN, Hybrid), trains them, and evaluates their performance on the test set.


## 📂 Project Structure

```
composer-classification/
├── notebooks/
│   ├── 01_Data_Preprocessing.ipynb
│   ├── 02_Model_Training_and_Evaluation.ipynb
│   
├── data/
│   └── (Raw MIDI files for each composer)
├── processed_data_split/
│   └── (Saved .pkl model and data files)
└── README.md
```

## 🚀 How to Run

1.  Place the raw MIDI files into the `data/` directory, organized in subfolders by composer name.
2.  Run the notebooks sequentially, starting with `01_Data_Preprocessing.ipynb`.
3.  Modify the `DATA_PATH` and `SAVE_DIR` variables in the notebooks to match your environment.

## 🛠️ Technologies Used

  * Python 3
  * TensorFlow / Keras
  * music21
  * scikit-learn
  * pandas & numpy
  * matplotlib & seaborn

