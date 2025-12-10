#  Mini Search Engine (C++)

A lightweight, command-line search engine built from scratch in **C++** using  
**TF-IDF ranking**, **word normalization**, **stemming**, and **multi-document indexing**.

This project demonstrates how real search engines process text, index documents, and rank results based on relevance.

---

##  Features

### 1. Multi-File Document Indexing
- Reads multiple `.txt` files.
- Cleans text (removes punctuation, converts to lowercase).
- Performs stemming (`playing → play`, `stories → story`, etc.).
- Builds a global **term-frequency index**.

### 2. Single Word Search
- Searches for a **single keyword** across all documents.
- Computes **TF-IDF score** for each document.
- Ranks results from most relevant → least relevant.

### 3. Multi Word Search (AND logic)
- Supports searching for multiple words.
- Only returns documents containing **all** the words.
- Ranks results using **combined TF-IDF score**.

### 4. Command Line Interface
Simple prompt-based interface:
Enter your search query (or 'exit'):

---

## How It Works

### Text Processing
Each line is:
1. Cleaned → non-alphanumeric removed  
2. Lowercased  
3. Tokenized  
4. Stemmed  
5. Counted into a frequency map

### TF-IDF Calculation
For each word in each document:
TF = (count of word in doc) / (total words in doc)
IDF = log(N / df)
Score = TF * IDF
Where:
- `N` = total number of documents  
- `df` = number of documents containing the word  

This ensures common words get lower score, rare but important words get higher.

---

## Project Structure
MiniSearchEngine/
│
├── main.cpp # Source code
├── file1.txt
├── file2.txt
├── file3.txt
├── ... more files
└── README.md


---

## How to Run

1. Compile using g++:
g++ main.cpp -o search

2. Run:
./search

3. Enter queries (or exit):
Artificial intelligence 
banana 
Data quantum


---

## 🔮 Future Improvements 

- OR logic search  
- Phrase search (“machine learning”)  
- Better stemming  
- Export results  
- Inverted index using maps or trie  

---




