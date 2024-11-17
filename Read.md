Situationships Data Analysis and Sentiment Processing
This repository contains the Python code and methodology used for analyzing comments related to the phenomenon of situationships. The analysis involves preprocessing textual data, performing topic modeling, sentiment analysis, and extracting insights based on word frequencies. The project uses advanced natural language processing (NLP) techniques and leverages tools like SpaCy, Gensim, and NLTK.

Repository Contents
1. Code Files
The primary script/code performs the following tasks:
Text Preprocessing:
Tokenization, lemmatization, and removal of stop words.
POS filtering to focus on nouns.
N-gram Construction:
Builds bigrams and trigrams for better context capture.
Sentiment Analysis:
Analyzes the sentiment of comments using RoBERTa (cardiffnlp/twitter-roberta-base-sentiment).
Topic Modeling:
Constructs LDA topic models to uncover hidden themes in the text.
Word Frequency Analysis:
Identifies and filters frequently occurring words for high-negative and high-positive comments.
2. Dataset
journal_final_reddit.xlsx: Original dataset of comments (ensure it is anonymized before sharing or processing).
3. Output Files
situationships_preprocessed_data.xlsx: Dataset with preprocessed text and added columns for further analysis.
sentiment_analysis_results.xlsx: Contains sentiment analysis results, including sentiment labels and scores for each comment.
Steps to Reproduce
Prerequisites
Ensure you have Python 3.8 or above installed, along with the following libraries:

pandas
spacy
gensim
transformers
nltk
openpyxl
seaborn
matplotlib
Install all dependencies by running:

bash
Copy code
pip install -r requirements.txt
Process Workflow
File Upload:

The dataset (journal_final_reddit.xlsx) is uploaded and read using Pandas.
Text Preprocessing:

Removes stop words, lemmatizes text, and constructs n-grams using SpaCy and Gensim.
Outputs: situationships_preprocessed_data.xlsx
Topic Modeling:

Applies LDA modeling using Gensim.
Extracts and displays key topics with coherence scores.
Sentiment Analysis:

Uses a pre-trained RoBERTa model to analyze sentiments.
Outputs sentiment labels (Positive, Neutral, Negative) and scores.
Visualizations:
Sentiment label distribution (count plot).
Sentiment score distribution by label (box plot).
Outputs: sentiment_analysis_results.xlsx
Word Frequency Analysis:

Identifies the top words associated with high-positive and high-negative comments.
Filters out additional custom stop words.
Key Outputs
Statistics
Descriptive statistics of the dataset (e.g., comment length, total word count).
Sentiment analysis results:
Sentiment label distribution.
Sentiment score statistics grouped by label.
Visualizations
Distribution of sentiment labels (bar plot).
Sentiment score distribution by label (box plot).
Topic Modeling
Coherence score: Measures the quality of topics.
Top 10 topics: Each with the most representative words.
Frequent Words
Top words for high-positive/neutral comments.
Top words for high-negative comments.
Usage
Run the Script:

Execute the code in a Jupyter Notebook or Colab environment.
Upload the journal_final_reddit.xlsx dataset during execution.
Save Results:

Sentiment analysis results are saved as an Excel file (sentiment_analysis_results.xlsx).
Preprocessed dataset is saved as situationships_preprocessed_data.xlsx.
Customization
Thresholds:

Adjust thresholds for sentiment scores in the code (e.g., threshold = 0.9).
Stop Words:

Add/remove words from the additional_stop_words set to refine word frequency analysis.
Number of Topics:

Change the number of topics for LDA modeling (default: num_topics = 10).