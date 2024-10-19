# Vietnamese Sentiment Analysis using PhoBERT and Logistic Regression

This project demonstrates sentiment analysis on Vietnamese text using PhoBERT for feature extraction and Logistic Regression for classification.

## Dataset

The project utilizes the "Vietnamese Sentiment Analyst" dataset from Kaggle: 

The dataset contains customer reviews from Shopee, labeled as positive, negative, or neutral.


## Methodology

1. **Data Preprocessing:**
    - The dataset is loaded and cleaned by removing rows with missing values.
    - Labels are converted to numerical values: 
        - POS: 1
        - NEG: -1
        - NEU: 0
2. **Feature Extraction:**
    - PhoBERT, a pre-trained language model for Vietnamese, is used to extract text embeddings.
    - The `extract_embedding_batch` function tokenizes the text and extracts embeddings using PhoBERT.
3. **Model Training:**
    - Logistic Regression is employed as the classification model.
    - The model is trained on the extracted embeddings and corresponding labels.
4. **Evaluation:**
    - The model's performance is evaluated on a test set using accuracy and classification report metrics.
5. **Prediction:**
    - The trained model is saved and can be loaded for predicting sentiment on new text samples.
    - The model predicts the sentiment label (Positive, Negative, or Neutral) for a given input.


## Usage

1. **Install Dependencies:**
   ```
   pip install kaggle
   pip install torch transformers scikit-learn

   ```
3. **Download Dataset:**
    Download the "Vietnamese Sentiment Analyst" dataset from Kaggle: 
4. **Run Notebook:**
    Execute the provided Jupyter Notebook to train the model and make predictions.


## Results

- The model achieved an accuracy of 76 % on the test set.
- Detailed classification report is included in the notebook.
- **Tokenizer Optimization:** The tokenizer process has been optimized by utilizing CUDA, resulting in faster execution time.

## Conclusion

- This project demonstrates the effective use of PhoBERT and Logistic Regression for Vietnamese sentiment analysis.
- The trained model can be used for various applications such as analyzing customer feedback, social media monitoring, and market research.
