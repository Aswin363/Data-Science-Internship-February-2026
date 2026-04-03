# NLP Task 4 – Fine-Tuning BERT on IMDB Dataset

##  Overview
This project is part of my Data Science Internship (February 2026), where I implemented a text classification model by fine-tuning a pre-trained BERT model on the IMDB movie reviews dataset.

The goal of this project is to understand how transformer-based models like BERT can be used for sentiment analysis tasks.

---

##  Objective
- Fine-tune a pre-trained BERT model for sentiment classification  
- Perform text preprocessing and tokenization  
- Train and evaluate the model using multiple metrics  
- Compare different fine-tuning strategies  

---

## 🛠 Tools & Technologies
- Python  
- PyTorch  
- Hugging Face Transformers  
- Scikit-learn  
- Matplotlib & Seaborn  

---

## 📊 Dataset
- Dataset: IMDB Movie Reviews (Kaggle)  
- Total Records: 50,000  
- Classes: Positive (1), Negative (0)  

---

## 🔄 Pipeline Flow

Raw Data  
↓  
Text Cleaning & Preprocessing  
↓  
Tokenization (BERT Tokenizer)  
↓  
Train / Validation / Test Split  
↓  
Model Training (Fine-Tuning)  
↓  
Evaluation  
↓  
Experiment Comparison  

---

## 🧹 Data Preprocessing
- Removed HTML tags and URLs  
- Converted text to lowercase  
- Removed special characters  
- Removed empty rows  

---

## 📊 Data Analysis
- Visualized class distribution  
- Analyzed review length distribution  
- Verified balanced dataset  

---

## 🔤 Tokenization
- Used `bert-base-uncased` tokenizer  
- Applied padding and truncation  
- Maximum sequence length: 128  

---

## 🧠 Model Architecture
- Model: BERT (bert-base-uncased)  
- Type: Sequence Classification  
- Output: Binary classification (Positive / Negative)  

---

## ⚙️ Training Details
- Optimizer: AdamW  
- Learning Rate: 2e-5  
- Batch Size: 16  
- Scheduler: Linear Warmup  
- Gradient Clipping applied  

---

## 📈 Evaluation Metrics
- Accuracy  
- Precision  
- Recall  
- F1 Score  
- Confusion Matrix  
- Classification Report  

---

## 🧪 Experiments

### 🔹 Experiment 1: Frozen BERT
- All BERT layers frozen  
- Only classifier layer trained  
- Faster but lower performance  

### 🔹 Experiment 2: Fine-Tuning Last 2 Layers
- Last 2 encoder layers unfrozen  
- Better performance and adaptability  

---

## 📊 Results

| Experiment | Performance |
|----------|------------|
| Frozen BERT | Lower Accuracy & F1 |
| Last 2 Layers | Improved Performance |

👉 Fine-tuning the last two layers provided better results compared to freezing all layers.

---

## 📌 Analysis
- Frozen BERT cannot adapt well to new data  
- Fine-tuning improves contextual understanding  
- Partial fine-tuning gives a balance between speed and accuracy  

---

## ⚠️ Note
A subset of the dataset was used to reduce training time due to hardware limitations.

---

## 🏁 Conclusion
BERT is highly effective for NLP classification tasks. Fine-tuning the last layers significantly improves performance compared to freezing the model. Increasing dataset size and training epochs can further enhance the results.

---

## 🚀 Future Improvements
- Use DistilBERT or RoBERTa  
- Increase epochs and dataset size  
- Apply early stopping  
- Hyperparameter tuning  

---


## 🙏 Acknowledgment
Thanks to Innomatics Research Labs, my trainer, and my mentor for their continuous support and guidance.

---

## 📌 Author
Your Name
