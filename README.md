# Word2Vec Embeddings & Vector Arithmetic Analysis

## Project Overview
This project focuses on Natural Language Processing (NLP) word embeddings using Python and Gensim. It demonstrates how pretrained word vectors capture semantic meanings, word similarities, and vector mathematics (analogy solving) using Google's Word2Vec model.

## Model & Dataset Information
- **Pretrained Model:** `word2vec-google-news-300`
- **Vector Dimension:** 300 dimensions
- **Vocabulary Size:** ~3 Million words trained on ~3 Billion words from Google News

## Technologies Used
- Python
- Jupyter Notebook / Google Colab
- Gensim (`gensim.downloader`, `KeyedVectors`)
- NumPy

## Project Workflow

1. Install and import Gensim library.
2. Load pretrained `word2vec-google-news-300` embeddings via `gensim.downloader`.
3. Extract and inspect 300-dimensional word vectors (e.g., `'king'`, `'cricket'`).
4. Perform semantic similarity search using `most_similar()`.
5. Calculate pairwise cosine similarity between concepts using `similarity()`.
6. Implement vector arithmetic to solve semantic analogies:
   $$v_{\text{result}} = v_{\text{king}} - v_{\text{man}} + v_{\text{woman}}$$

## Key Analysis & Results

- **Vector Shape:** Each word is converted into a 300-dimensional continuous vector space.
- **Word Similarity:**
  - `wv.most_similar('cricket')` $\rightarrow$ `cricketing`, `cricketers`, `Test_cricket`
  - `wv.most_similar('happy')` $\rightarrow$ `glad`, `pleased`, `ecstatic`
- **Semantic Distance:**
  - Similarity between `'hockey'` and `'sports'` $\approx 0.5354$
- **Vector Arithmetic:**
  - $v_{\text{king}} - v_{\text{man}} + v_{\text{woman}} \approx v_{\text{queen}}$ (Cosine Similarity: $0.7300$)

## Libraries Installation

Install the required libraries using:

```bash
pip install gensim numpy
```

## How to Run the Project

1. Download or clone this repository.
2. Keep the Jupyter Notebook in your project folder.
3. Install the required libraries (`gensim`, `numpy`).
4. Open Jupyter Notebook or Google Colab.
5. Open `Word2vec_Practical_Implementation_(Spam Project).ipynb`.
6. Run all cells step by step. *(Note: Downloading the pretrained Word2Vec model requires ~1.66 GB of data).*

## Project Structure

```text
Word2Vec-Embeddings-Analysis/
│
├── Word2vec_Practical_Implementation_(Spam Project).ipynb
└── README.md
```

## Conclusion

This project illustrates the power of word embeddings in modern Natural Language Processing. By transforming words into high-dimensional numerical vectors, machine learning models can understand contextual relationships, semantic similarity, and word analogies.

## Author

Priya Kale