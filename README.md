📚 IMDB Movie Review Sentiment Analysis with Simple RNN

This project demonstrates how to use a Simple Recurrent Neural Network (RNN) to classify movie reviews from the IMDB dataset as positive or negative. It covers the full machine learning pipeline: data preprocessing, model training, evaluation, saving, and serving predictions via a Streamlit web application.

🧠 Model Training (simplernn.ipynb)

->Dataset: IMDB movie reviews (from tensorflow.keras.datasets).

->Preprocessing:

   o Tokenized and integer-encoded reviews (limited to 10,000 most frequent words).

   o All reviews are padded to a fixed length of 500 for uniform input size.

->Model Architecture:

   o Embedding layer to convert words into dense vectors.

   o SimpleRNN with 128 units and ReLU activation.
 
   o Dense output layer with sigmoid activation.

->Training:

   o Binary cross-entropy loss

   o EarlyStopping with validation monitoring to avoid overfitting

   o Final model saved as simple_rnn_imdb.keras


   🔍 Prediction Script (prediction.ipynb)
   
->Loads the trained RNN model.

->Contains utility functions for:

   o Decoding encoded reviews.

   o Preprocessing raw user text into model-ready format.

->Example predictions are made on sample reviews, returning the predicted sentiment and its confidence score.


🌐 Streamlit App (app.py)

The Streamlit interface enables real-time sentiment prediction from user-provided movie reviews.

Features:

->Text area input for custom movie reviews.

->Predict button to classify sentiment.

->Output display with sentiment label and prediction probability.
