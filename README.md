# Text Mining with TF-IDF

Python implementation of text mining using Count Vectorization and TF-IDF to extract features from text documents.

## Dataset
3 sports-related text documents (basketball, soccer, swimming)

## Requirements
```bash
pip install pandas numpy scikit-learn nltk
```

## Usage
```python
from sklearn.feature_extraction.text import CountVectorizer, TfidfVectorizer

# Count Vectorization
count_vec = CountVectorizer(stop_words="english")
doc_matrix = count_vec.fit_transform(documents)

# TF-IDF Vectorization  
tfidf_vec = TfidfVectorizer(stop_words="english")
tfidf_matrix = tfidf_vec.fit_transform(documents)
```

## Results

**Vocabulary**: 9 unique terms after stopword removal
- `basketball`, `game`, `good`, `health`, `love`, `play`, `popular`, `soccer`, `swimming`

**TF-IDF Scores**:
- Document-specific terms: **basketball, soccer, swimming** (2.099)
- Common term: **game** (1.000) - appears in all documents

## Applications
- Document similarity analysis
- Text classification preprocessing  
- Keyword extraction
- Information retrieval systems
