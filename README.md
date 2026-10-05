# Information Retrieval: Practical Work (TPs)

Lab sessions for the Information Retrieval module, from text preprocessing and term weighting to retrieval models. The final project that builds on these labs is in a separate repository: [Information-Retrival-Project](https://github.com/sarahmoussaoui/Information-Retrival-Project).

## Repository structure

```
.
├── Collection/                       # Test collection
├── Documents/                        # Sample documents
├── LAB0+1/                           # Lab 0 and 1
├── LAB2/                             # Lab 2
├── LAB3/                             # Lab 3
├── LAB4/                             # Lab 4
├── lab2_language_models_results.txt  # Output of the Lab 2 language-model experiments
├── notes.txt                         # Working notes
└── README.md
```

## Core concepts

### TF (Term Frequency)

How often a term appears in a document.

```
TF(t, d) = (occurrences of t in d) / (total terms in d)
```

Example: in "the cat sat on the mat", TF("cat") = 1/6 ≈ 0.1667.

### IDF (Inverse Document Frequency)

How rare a term is across the corpus.

```
IDF(t) = log(N / df_t)
```

where `N` is the number of documents and `df_t` the number of documents containing `t`. Common words ("the", "and") get a low IDF, rare words a high one.

### TF-IDF

```
TF-IDF(t, d) = TF(t, d) × IDF(t)
```

High when a term is frequent in a document but rare in the collection, which makes it a good keyword indicator.

## Getting started

```bash
git clone https://github.com/sarahmoussaoui/Information-Retrival-Practical-Work.git
cd Information-Retrival-Practical-Work

python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
```

Install the packages the labs import (for example `numpy`, `scipy`, `scikit-learn`, `nltk`), then run the scripts or notebooks of the lab you want from its folder.

