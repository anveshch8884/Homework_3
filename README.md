NLP Pipeline Using NLTK - Assignment H3
This project demonstrates the construction of a basic Natural Language Processing (NLP) pipeline using the NLTK (Natural Language Toolkit) library. It forms part of an academic assignment to explore key steps involved in text preprocessing and linguistic analysis.

📌 Objective
To implement and understand the foundational building blocks of an NLP pipeline:

Breaking text into smaller components

Cleaning and transforming text

Understanding syntactic and semantic elements of language

🗂️ Notebook Overview
The notebook H3.ipynb performs the following NLP operations:

1. 🔡 Input Text
A sample paragraph is hardcoded into the notebook.

This paragraph is used as the base input for all subsequent processing steps.

2. ✂️ Tokenization
Goal: Divide text into smaller units—sentences and words.

Sentence Tokenization:

Uses nltk.sent_tokenize() to split the paragraph into individual sentences.

Word Tokenization:

Uses nltk.word_tokenize() to split the text into individual words (tokens), including punctuation.

✅ Output: Lists of sentences and words from the input paragraph.

3. 🧹 Stop Words Removal
Goal: Remove common English words (e.g., “the”, “is”, “in”) that do not add much meaning in context.

Utilizes nltk.corpus.stopwords to filter out stopwords from tokenized words.

✅ Output: Cleaned list of words after removing stopwords.

4. 🌱 Stemming
Goal: Reduce words to their root forms by chopping off suffixes.

Uses PorterStemmer from NLTK.

Example: "playing" → "play", "flies" → "fli"

✅ Output: A stemmed version of the tokenized sentence.

5. 📖 Lemmatization
Goal: Convert words to their base dictionary form (lemma) using context-aware rules.

Uses WordNetLemmatizer.

Unlike stemming, lemmatization considers the actual meaning of words.

Example: "better" → "good" (depending on POS tagging)

✅ Output: Lemmatized version of the sentence.

6. 🏷️ Part-of-Speech (POS) Tagging
Goal: Tag each word in a sentence with its grammatical role (e.g., noun, verb, adjective).

Uses nltk.pos_tag() on tokenized words.

Helps understand sentence structure and context.

✅ Output: List of tuples: (word, POS_tag)

7. 🧑🏽‍💼 Named Entity Recognition (NER)
Goal: Identify named entities in the text such as:

People

Locations

Organizations

Dates

Combines POS tagging with nltk.ne_chunk() to identify chunks labeled with entity types.

✅ Output: Parsed tree showing named entities from the text.

🛠️ Setup & Installation
Make sure Python 3.x and pip are installed. Then install nltk:

bash
pip install nltk
Download the necessary NLTK resources:

import nltk
nltk.download('punkt')
nltk.download('stopwords')
nltk.download('wordnet')
nltk.download('averaged_perceptron_tagger')
nltk.download('maxent_ne_chunker')
nltk.download('words')
▶️ How to Run
Clone the repository or download the H3.ipynb file.

Open it in Jupyter Notebook, Google Colab, or VS Code.

Run each cell step by step.

Observe how raw text is transformed at each NLP stage.

📚 Learning Outcomes
By completing this notebook, you will:

Understand how raw text is transformed into structured data

Learn the difference between stemming and lemmatization

Grasp how POS tagging and NER contribute to deeper language understanding

Gain experience using the nltk library
