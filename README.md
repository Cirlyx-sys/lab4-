# lab4

Lab 4 – Text Feature Engineering on Databricks

This lab applies text feature engineering to the Goodreads review dataset stored in Azure Data Lake (ADLS). The notebook performs the following steps:

Connects to ADLS using the storage account key.

Loads the curated dataset: gold/features_v1.

Splits the data into train/validation/test (70/15/15).

Cleans and normalizes review text (lowercase, remove punctuation, remove URLs, remove digits).

Extracts numerical features:

review_length_words

review_length_chars

Adds sentiment features using NLTK VADER:

sentiment_pos, sentiment_neu, sentiment_neg, sentiment_compound

Adds lexical features:

avg_word_length

lexical_diversity

Combines all features + metadata (review_id, book_id, rating).

Saves the final training dataset to:
gold/features_v2/train_simple_features.

Due to cluster restrictions (Spark Connect blocking Spark ML constructors), TF-IDF and BERT embeddings were not used. Instead, the lab uses pure PySpark + VADER as permitted by the environment and instructor instructions.
