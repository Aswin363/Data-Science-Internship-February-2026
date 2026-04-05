# Fine-Tuning DistilBERT for POS Tagging and Chunking

## Project Overview

This project focuses on **token classification using transformer models**. We fine-tune **DistilBERT** to perform:

* Part-of-Speech (POS) Tagging
* Chunking (Phrase Detection)

Token classification assigns labels to each word in a sentence, helping machines understand both **grammar** and **sentence structure**.

---

## Objective

* Build a token classification system using DistilBERT
* Perform POS tagging and chunking
* Handle tokenization and label alignment
* Evaluate model performance using sequence-based metrics

---

## Dataset Used

* **Dataset:** CoNLL-2000
* **Source:** NLTK corpus

### Dataset Contains:

* Tokens (words)
* POS Tags (NN, VB, JJ, etc.)
* Chunk Tags (B-NP, I-NP, B-VP, etc.)

---

## Technologies Used

* Python
* Hugging Face Transformers
* PyTorch
* NLTK
* SeqEval (for evaluation)

---

## Pipeline Flow

```
Raw Data → Tokenization → Label Alignment → Model Training → Evaluation → Inference → Comparison
```

---

## Key Concepts

* Token Classification
* POS Tagging (word-level task)
* Chunking (phrase-level task)
* Transformer Models (DistilBERT)
* Label Alignment using -100

---

## Model Implementation

* Model: `distilbert-base-uncased`
* Used: `AutoModelForTokenClassification`
* Separate models for:

  * POS Tagging
  * Chunking

---

## Training Details

* Learning Rate: `2e-5`
* Batch Size: `4`
* Epochs: `1`
* Optimizer: AdamW

---

## Evaluation Metrics

* Precision
* Recall
* F1 Score

👉 POS Tagging achieved better performance compared to Chunking due to its simpler nature.

---

## Inference Example

**Input:**
`John works at Google in California`

**Output:**

* POS Tags → Noun, Verb, etc.
* Chunk Tags → NP, VP

---

## Comparison

| Feature    | POS Tagging | Chunking     |
| ---------- | ----------- | ------------ |
| Level      | Word-level  | Phrase-level |
| Focus      | Grammar     | Structure    |
| Complexity | Easy        | Moderate     |

---

## Challenges Faced

* Handling subword tokenization
* Label alignment with tokens
* Missing labels in dataset

---

##  Key Learnings

* Transformers improve NLP performance using context
* Proper preprocessing is critical
* Label alignment is essential for token classification

---

## Conclusion

DistilBERT is highly effective for token classification tasks.
POS tagging is simpler and more accurate, while chunking is more complex due to phrase-level understanding.

This project demonstrates how transformer models can be applied to real-world NLP problems.

---

## Submission Details

* 📁 Notebook: `.ipynb` file
* 🔗 GitHub Repository: (Add your link here)
* 📢 LinkedIn Post: (Add your link here)

---

##  Acknowledgment

Thanks to **Innomatics Research Labs** for providing this learning opportunity and guidance throughout the internship.

---

## Hashtags

#NLP #ArtificialIntelligence #MachineLearning #DataScience #DeepLearning #BERT
