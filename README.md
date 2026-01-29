# IMDB Movie Review Sentiment Analysis

Streamlit app that classifies IMDB movie reviews as positive or negative using a pre-trained SimpleRNN model.

## Preview

![App Screenshot](./assets/ui-screenshot.png)

> If you want the screenshot to render, place the provided image at `assets/ui-screenshot.png`.

## Features

- Real-time sentiment classification of movie reviews
- Probability score shown alongside the label
- Pre-trained Keras model loaded from `simple_rnn_imdb.h5`
- Clean Streamlit UI for quick testing

## Project Structure

```
.
├─ main.py
├─ requirements.txt
├─ simple_rnn_imdb.h5
├─ prediction.ipynb
├─ simplernn.ipynb
└─ README.md
```

## Setup

1. Create and activate a virtual environment (optional but recommended).
2. Install dependencies:

```
pip install -r requirements.txt
```

## Run the App

```
streamlit run main.py
```

Then open the local URL printed in the terminal.

## How It Works

- The app uses the IMDB word index to encode input text.
- Reviews are padded to length 500 before prediction.
- The model outputs a score; values > 0.5 are **Positive**, else **Negative**.

## Notes

- The word index comes from `tensorflow.keras.datasets.imdb`.
- The model file `simple_rnn_imdb.h5` must be present in the project root.

