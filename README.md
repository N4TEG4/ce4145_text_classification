# CE4145 Text Classification Coursework Project

This repository contains the implementation for the **CE4145 Natural Language Processing coursework**.  
The project focuses on **sentiment classification** using the *Sentiment Labelled Sentences* dataset from the UCI Machine Learning Repository.

---

## Project Structure

ce4145_project/
│
├── data/
│ ├── amazon_cells_labelled.txt
│ ├── imdb_labelled.txt
│ └── yelp_labelled.txt
│
├── CE4145_Text_Classification.ipynb ← main notebook for coursework
├── requirements.txt ← package dependencies
└── README.md


### Implemented Pipelines

1. **Word-Level TF–IDF + Multinomial Naïve Bayes (MNB)**  
   - Classic probabilistic text classifier.  
   - Represents each document as a sparse vector of word TF–IDF features.  
   - Well-suited for small, clean datasets.

2. **Character-Level TF–IDF + Linear Support Vector Machine (SVM)**  
   - Represents documents as character n-gram TF–IDF features.  
   - Captures subword patterns, useful for stylistic or misspelling variations.  
   - Strong linear baseline for text classification.

Both models are evaluated and compared using **accuracy** and **weighted F1 score** on validation and test splits.

---

## Dataset

**Dataset source:** [UCI Sentiment Labelled Sentences](https://archive.ics.uci.edu/ml/datasets/sentiment+labelled+sentences)

Each file contains 1000 short sentences labelled with:  
- `1` → Positive sentiment  
- `0` → Negative sentiment  

The dataset is preloaded from the `data/` directory:

data/
├── amazon_cells_labelled.txt
├── imdb_labelled.txt
└── yelp_labelled.txt

---

## Setup Instructions

### Create a virtual environment
```cmd
py -3.11 -m venv .venv
.venv\Scripts\activate

pip install -r requirements.txt

jupyter notebook

CE4145_Text_Classification.ipynb



