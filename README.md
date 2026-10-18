# ITNPA4-B34
Project 1

This project classifies research abstracts as ai or classical using a TF-IDF + machine-learning pipeline (Questions 1–2, with a Streamlit app and HTML for deployment in deployment).

Q1 loads research_abstracts.json, drops duplicate abstracts, cleans the text (lowercase, strip URLs and non-letters, remove stop-words, lemmatize), splits it into train/test sets, converts it to numbers with a TF-IDF vectorizer, and trains a baseline Naive Bayes model. Q2 then trains several more models (Logistic Regression, Linear SVM, Random Forest, Gradient Boosting), compares them on test accuracy and Macro F1, improves one by balancing the classes through resampling, and saves the best-performing model and the fitted vectorizer as best_model.pkl and vectorizer.pkl. To use it: put app.py, best_model.pkl, vectorizer.pkl and requirements.txt in one folder

open a terminal there (not a notebook cell), run pip install -r requirements.txt, then streamlit run app.py. A browser page opens where you paste a research abstract, click Classify Abstract, and it replies with whether the abstract is ai or classical. Then there is a Notebook version that uses HTML widgets and still works the same way as the streamlit version of the web-interface but doesn't need external terminals.
