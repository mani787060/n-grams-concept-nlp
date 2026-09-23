# N-Grams Concept in NLP

## Overview

This project explores the concept of **N-grams** in Natural Language Processing (NLP). N-grams are sequences of consecutive words or tokens used to represent relationships between words in text.

The notebook uses a small custom dataset to understand how text can be divided into different types of N-grams and how increasing the value of `N` changes the representation of a sentence.

---

## Objective

The main objectives of this project are to:

* Understand the concept of N-grams.
* Learn how text can be represented using consecutive word sequences.
* Understand **Unigrams, Bigrams, and Trigrams**.
* Observe how the value of `N` affects text representation.
* Understand the importance of N-grams in NLP and text-based machine learning.

---

## Dataset

The notebook uses the following custom dataset:

```python
df = pd.DataFrame({
    'text': [
        'people watch campusx',
        'campusx watch campusx',
        'people write comment',
        'campusx write comment'
    ],
    'output': [1, 1, 0, 0]
})
```

### Dataset Columns

| Column   | Description                           |
| -------- | ------------------------------------- |
| `text`   | Input text/document                   |
| `output` | Output label associated with the text |

The dataset is intentionally small to make the N-gram generation process easy to understand.

---

## What are N-Grams?

An **N-gram** is a sequence of `N` consecutive words or tokens extracted from a text.

The value of `N` determines how many consecutive words are grouped together.

For example:

```text
people watch campusx
```

### Unigram (N = 1)

```text
people
watch
campusx
```

### Bigram (N = 2)

```text
people watch
watch campusx
```

### Trigram (N = 3)

```text
people watch campusx
```

---

## Types of N-Grams

### 1. Unigram

A unigram contains a single word.

```text
people
watch
campusx
```

It captures individual word information but does not capture relationships between neighboring words.

### 2. Bigram

A bigram contains two consecutive words.

```text
people watch
watch campusx
```

Bigrams provide some information about word-to-word relationships.

### 3. Trigram

A trigram contains three consecutive words.

```text
people watch campusx
```

Trigrams can capture more local context than unigrams and bigrams.

---

## General N-Gram Workflow

```text
Raw Text
   ↓
Tokenization
   ↓
Select N
   ↓
Generate N-Grams
   ↓
Represent Text
   ↓
NLP / Machine Learning Task
```

---

## Why N-Grams Are Useful

N-grams provide more contextual information than treating every word independently.

For example:

```text
machine learning
```

contains more meaningful local context as a bigram than the individual words:

```text
machine
learning
```

Similarly, larger N-grams can capture longer local word patterns.

---

## N-Grams and Machine Learning

N-grams can be used as features for traditional NLP machine learning models.

A typical workflow is:

```text
Text
  ↓
Preprocessing
  ↓
N-Gram Generation
  ↓
Vectorization
  ↓
Feature Matrix
  ↓
Machine Learning Model
```

N-gram features can be combined with techniques such as **Bag of Words** or **TF-IDF** to represent text numerically.

---

## Advantages

* Simple to understand and implement.
* Captures local word relationships.
* More informative than individual words in many cases.
* Can be used with traditional machine learning algorithms.
* Useful for text classification and other NLP tasks.

---

## Limitations

* Larger values of `N` can significantly increase the number of features.
* Many possible N-grams may never occur in the dataset.
* Can create sparse feature matrices.
* Does not understand deep semantic meaning.
* Usually captures only local context.
* The vocabulary can grow rapidly as `N` increases.

---

## Key Learnings

Through this project, the following concepts are explored:

* Understanding N-grams in NLP.
* Generating Unigrams, Bigrams, and Trigrams.
* Understanding how the value of `N` changes text representation.
* Capturing local word relationships.
* Understanding the connection between N-grams and text vectorization.
* Recognizing the advantages and limitations of N-gram-based representations.

---

## Applications

N-grams can be used in:

* Text classification
* Sentiment analysis
* Spam detection
* Language modeling
* Search systems
* Autocomplete systems
* Text prediction
* Natural Language Processing pipelines

---

## Technologies

* **Python**
* **Pandas**
* **Natural Language Processing (NLP)**
* **N-Grams**

---

## Future Improvements

This project can be extended by:

* Applying N-grams to a larger real-world dataset.
* Comparing Unigram, Bigram, and Trigram representations.
* Combining N-grams with TF-IDF.
* Using N-gram features for text classification.
* Exploring higher-order N-grams.
* Comparing traditional N-gram representations with modern word embeddings.

---

## Conclusion

N-grams are a fundamental concept in NLP that helps represent relationships between consecutive words or tokens. **Unigrams** capture individual words, while **Bigrams** and **Trigrams** provide increasing amounts of local context.

Understanding N-grams provides an important foundation for learning traditional NLP feature extraction techniques and more advanced language representation methods.
