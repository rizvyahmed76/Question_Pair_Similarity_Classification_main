This repository demonstrates how different machine learning and deep learning approaches perform on the Question Pair Similarity problem — a task where the goal is to detect whether two questions have the same meaning.

The project includes five different models, ranging from classical ML algorithms to advanced Siamese neural networks, allowing a complete performance comparison across multiple techniques.

🚀 Models Implemented
🔹 Classical Machine Learning Models (TF–IDF Based)

Logistic Regression
Random Forest Classifier
Support Vector Classifier (SVC)
These models use TF-IDF vectorization to convert text into numerical vectors.

🔹 Deep Learning Models
Siamese LSTM Network with Custom-Trained Word Embeddings
Siamese LSTM Network Using Pre-trained GloVe (300d) Embeddings

This comparison highlights the impact of:

trainable embeddings vs. fixed embeddings
classical ML vs. deep learning
sequential modeling for semantic similarity

📁 Project Structure
Question-Pair-Similarity/

│

├── Images/

│         └── (all the images are saved here)  

│

├── Model/

│      └── (trained models will be saved here automatically)

│

├── train_model.ipynb

├──  english_stopwords.pkl

├──  train.csv

├──  glove.6B.300d.txt

├──  requirements.txt

└── README.md

⚙️ Installation & Setup
1. Create a virtual environment (recommended)

        python -m venv venv
        source venv/bin/activate      # Linux/Mac
        venv\Scripts\activate         # Windows

3. Install all dependencies

       pip install -r requirements.txt

📥 Large File Notice (GitHub File Size Limits)

GitHub does not allow files larger than 100 MB, so the following files are not included in this repository.

❌ 1. siamese_lstm_model.h5

This file is generated automatically during training.
After training, it will be saved to:

Model/siamese_lstm_model.h5

❌ 2. glove.6B.300d.txt (≈ 990 MB)

Since GitHub cannot host this file, download it manually:

🔗 Kaggle Download Link:
https://www.kaggle.com/datasets/thanakomsn/glove6b300dtxt

After downloading, extract the file into the root of the project folder:

Question-Pair-Similarity/glove.6B.300d.txt

🧪 Training the Models

Launch Jupyter Notebook:
jupyter notebook
Open:
train_model.ipynb
Run the cells step-by-step to:
clean and preprocess text
vectorize using TF-IDF
train classical ML models
train LSTM-based Siamese networks
evaluate performance
generate similarity scores

All deep learning outputs (models, embeddings, padded sequences) will be saved automatically.


🔍 Running Similarity Checks
After training, you may use functions to compare any pair of questions and obtain a similarity score (duplicate or not) using your trained models.
