# 🔍 TF-IDF Ranked Retrieval System

A Python-based Information Retrieval (IR) system that processes a document collection, calculates **TF-IDF weights**, and ranks documents based on their relevance to a user's search query using **Cosine Similarity** and **Jaccard Similarity**.

## 📖 Overview
This project implements a search engine from scratch without using high-level IR libraries (like Whoosh or ElasticSearch). It demonstrates the core mathematical concepts of text retrieval:
1.  **Preprocessing:** Reading documents and building a **Bag of Words (BoW)**.
2.  **Indexing:** Constructing **Frequency Vectors** and **TF-IDF Vectors** for all documents.
3.  **Ranking:** Calculating similarity scores between the query and documents to return the top results.

## 🚀 Features
* **Bag of Words Model:** dynamically creates a vocabulary from the document corpus.
* **TF-IDF Calculation:**
    * *Term Frequency (TF):* Log-normalized frequency ($1 + \log(tf)$).
    * *Inverse Document Frequency (IDF):* Standard log inverse frequency ($\log(N/df)$).
* **Dual Similarity Metrics:**
    * **Cosine Similarity:** Measures the angle between the query vector and document vectors (best for ranked retrieval).
    * **Jaccard Similarity:** Measures the intersection over union of unique terms (set-based similarity).
* **Dynamic Search:** Accepts user input and ranks the top 10 matching documents.

## 🛠️ Technologies
* **Python 3.x**
* **Libraries:** `os`, `math`, `collections` (Standard Python libraries only).

## 📂 Dataset Structure
The system expects a main folder containing subfolders for different categories. By default, the code looks for:
* **Root Path:** `.../Desktop/Collection`
* **Categories:** `Gaza`, `Sport`, `Economy`

*You must update the `path` variable in the code to point to your local dataset.*

## ⚙️ How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Aseel-Alshishani/IR-Ranked-Retrieval.git](https://github.com/Aseel-Alshishani/IR-Ranked-Retrieval.git)
    ```
2.  **Prepare your data:**
    Ensure you have a folder with text files organized by category.
3.  **Update the path:**
    Open the script and change the `path` variable to your document folder location:
    ```python
    path = r'C:\Your\Local\Path\To\Collection'
    folders = ['Gaza', 'Sport', 'Economy'] # Update folder names if necessary
    ```
4.  **Run the script:**
    ```bash
    python ir_system.py
    ```
5.  **Search:**
    Enter a query when prompted (e.g., `sport`, `economy crisis`, etc.).

## 📊 Example Output

```text
Enter your search query: sport

The similarity between query and documents based on Cos similarity is:
Doc id          Similarity
39 Sport.txt    0.11
28 Sport.txt    0.10
46 Sport.txt    0.10
...

The similarity between query and documents based on Jaccard similarity is:
Doc id          Similarity
31 Sport.txt    0.01
...vv
