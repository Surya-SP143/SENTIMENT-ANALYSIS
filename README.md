# SENTIMENT-ANALYSIS <br>
COMPANY : CODTECH IT SOLUTIONS PVT.LTD <br>
NAME : SURYA DAS MAHANTA <br>
INTERN ID : CTIS8871 <br>
DOMAIN : DATA ANALYTICS <br>
DURATION : 4 WEEKS <br>
MENTOR : NEELA SANTHOSH KUMAR

#  Task 4: Sentiment Analysis on Textual Data using Spark NLP

### 📌 Project Overview
This project focuses on building a scalable **Natural Language Processing (NLP)** pipeline to classify the sentiment of movie reviews as either **Positive** or **Negative**. Using the **IMDB Dataset of 50K Movie Reviews** sourced from Kaggle, the entire processing and model training workflow was executed on the cloud-based **Databricks** platform using **Apache Spark**.

###  Tech Stack & Concepts
* **Platform:** Databricks
* **Language:** Python (PySpark)
* **Engine:** Apache Spark (Distributed Computing for Big Data)
* **Libraries:** `pyspark.ml.feature` (Tokenizer, StopWordsRemover, HashingTF, IDF), `pyspark.ml.classification` (LogisticRegression)

###  Pipeline Architecture & Implementation
The project follows a standard machine learning engineering pipeline for unstructured text data:

1. **Data Ingestion & Labeling:** Imported the IMDB CSV file into Databricks Volumes. Converted string sentiments (`positive` / `negative`) into binary numeric labels (`1.0` / `0.0`).
2. **Text Pre-processing (NLP Pipeline):**
   * **Tokenization:** Fragmented raw review text sentences into individual word tokens.
   * **Stop-Words Removal:** Cleaned the text by stripping out common unhelpful words (e.g., "the", "is", "and").
   * **Feature Extraction (TF-IDF):** Computed Term Frequency-Inverse Document Frequency to map words into mathematical vectors based on their importance.
3. **Model Training:** Split the dataset into **80% Training** and **20% Testing** allocations. Trained a distributed **Logistic Regression Classifier** optimized for binary classification.
4. **Evaluation:** Evaluated model performance utilizing the Binary Classification Evaluator (Area Under ROC) and visualized performance metrics using a Matplotlib/Seaborn **Confusion Matrix Heatmap**.

###  Performance & Insights
* **Model Accuracy (ROC Score):** [Insert your final accuracy score here, e.g., 0.88]
* **Key Observations:** The pipeline proved highly efficient at isolating sentiment-bearing keywords (e.g., "masterpiece", "waste"). Distributed computing via Spark ensured rapid tokenization and feature mapping across thousands of heavy text records without latency.
