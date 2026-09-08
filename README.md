# 2025-29_AdityaGupta_25scs1003001506_3rdsem_2CSE19

Your official documents confirm Aditya Gupta, Artificial Intelligence Intern, Codec Technologies Pvt. Ltd., and 30/07/2026–30/08/2026.

You can copy-paste the following directly into your README.md:

# 2025-29_AdityaGupta_25SCS1003001506
# Artificial Intelligence Internship

## AICTE & ICAC Approved Internship Program | Codec Technologies Pvt. Ltd.

This repository contains my internship project, documentation, presentation, and internship completion certificate for the Artificial Intelligence Internship conducted by Codec Technologies Pvt. Ltd.

The internship was a **1 Month (30 Days) AICTE & ICAC Approved Internship Program**, conducted from **30 July 2026 to 30 August 2026**, during which I worked on a **Twitter Sentiment Analysis** project using Machine Learning and Natural Language Processing techniques.

---

## 👤 Student Details

| Field | Details |
|---|---|
| **Name** | Aditya Gupta |
| **Enrollment No.** | 25SCS1003001506 |
| **Internship Domain** | Artificial Intelligence |
| **Organization** | Codec Technologies Pvt. Ltd. |
| **Duration** | 30 Days / 1 Month |
| **Start Date** | 30 July 2026 |
| **End Date** | 30 August 2026 |
| **Internship Role** | Artificial Intelligence Intern |
| **Approval** | AICTE & ICAC Approved |
| **Development Platform** | Google Colab |
| **Mode** | Pan India, Hybrid |

---

## 📌 About the Internship

The internship was conducted by **Codec Technologies Pvt. Ltd.** as a **1 Month Artificial Intelligence Internship Program**.

During the internship, I worked on a Machine Learning project focused on **Twitter Sentiment Analysis**, with the objective of automatically classifying tweets according to their sentiment.

The project involved working with a large-scale Twitter dataset, performing text data preprocessing, converting textual information into numerical machine-learning features, training a classification model, evaluating its performance, and using the trained model for sentiment prediction.

The complete project workflow was implemented using **Python in Google Colab**.

---

# 🧠 Project: Twitter Sentiment Analysis

## 📖 Overview

The project focuses on automatically determining the sentiment expressed in a tweet.

The model was trained using the **Sentiment140 dataset**, containing approximately **1.6 million tweets**. The dataset contains sentiment labels that can be transformed into two classes:

- `0` → Negative Tweet
- `1` → Positive Tweet

The complete workflow was implemented using **Python and Google Colab**.

The project uses Natural Language Processing techniques to clean and prepare tweet text before converting the text into numerical features using **TF-IDF (Term Frequency-Inverse Document Frequency)**.

A **Logistic Regression** machine-learning model is then trained to classify tweets into negative or positive sentiment categories.

---

## 🎯 Objective

The main objectives of the project are:

- To understand the fundamentals of Natural Language Processing.
- To acquire and process the Sentiment140 Twitter dataset.
- To inspect and understand a large-scale text dataset.
- To preprocess raw tweet data for machine-learning applications.
- To remove unnecessary characters and normalize textual data.
- To remove English stop words using NLTK.
- To apply Porter Stemming to reduce words to their root forms.
- To convert textual data into numerical features using TF-IDF.
- To divide the dataset into training and testing datasets.
- To train a Logistic Regression classification model.
- To evaluate the performance of the trained model.
- To save the trained machine-learning model using Pickle.
- To reload the saved model and perform sentiment predictions.

---

## 🔄 Project Workflow

```text
Sentiment140 Dataset
        ↓
Dataset Download from Kaggle
        ↓
CSV Extraction
        ↓
Data Loading using Pandas
        ↓
Data Inspection
        ↓
Target Label Transformation
        ↓
Text Preprocessing
        ↓
Lowercase Conversion
        ↓
Stop-Word Removal
        ↓
Porter Stemming
        ↓
Train-Test Split
        ↓
TF-IDF Vectorization
        ↓
Logistic Regression
        ↓
Model Training
        ↓
Accuracy Evaluation
        ↓
Model Saving using Pickle
        ↓
Model Loading
        ↓
Sentiment Prediction

```
🛠️ Technologies and Tools Used
Technology / Tool	Purpose
Python	Programming language
Google Colab	Development and execution environment
Kaggle	Dataset acquisition
Pandas	Data loading and manipulation
NumPy	Numerical operations
NLTK	Natural Language Processing
Regular Expressions	Text cleaning
PorterStemmer	Word stemming
Scikit-learn	Machine Learning
TfidfVectorizer	Text feature extraction
Logistic Regression	Sentiment classification
accuracy_score	Model evaluation
Pickle	Model saving and loading
📊 Dataset
Sentiment140

The project uses the Sentiment140 dataset, which contains approximately 1.6 million tweets.

Dataset Feature	Description
Dataset Name	Sentiment140
Approximate Records	1,600,000 tweets
Domain	Twitter / Social Media
Task	Sentiment Classification
Original Negative Label	0
Original Positive Label	4
Project Negative Label	0
Project Positive Label	1

The original positive sentiment label 4 is converted to 1 so that the project uses a binary classification format:

0 → Negative
1 → Positive
🧹 Data Preprocessing

Raw tweets contain punctuation, special characters, inconsistent capitalization, and common words. Therefore, preprocessing is performed before training the machine-learning model.

The preprocessing pipeline includes:

Regular-expression based text cleaning
Lowercase conversion
Tokenization
English stop-word removal
Porter stemming
Creation of processed tweet text
Preprocessing Workflow
Raw Tweet
   ↓
Remove Non-Alphabetic Characters
   ↓
Convert to Lowercase
   ↓
Split into Words
   ↓
Remove Stop Words
   ↓
Porter Stemming
   ↓
Processed Text
🔢 TF-IDF Feature Extraction

Machine-learning algorithms require numerical input. Since tweets are textual data, the processed tweets are converted into numerical feature vectors using TF-IDF.

The project uses Scikit-learn's:

TfidfVectorizer()

The vectorizer is fitted on the training data and then used to transform the testing data.

vectorizer = TfidfVectorizer()

x_train = vectorizer.fit_transform(x_train)
x_test = vectorizer.transform(x_test)
🤖 Machine Learning Model
Logistic Regression

The project uses Logistic Regression as the classification algorithm.

model = LogisticRegression(max_iter=1000)

model.fit(x_train, y_train)

Logistic Regression is used to classify the processed tweets into two sentiment categories:

0 → Negative Tweet
1 → Positive Tweet
📚 Train-Test Split

The dataset is divided into training and testing portions using Scikit-learn's train_test_split().

x_train, x_test, y_train, y_test = train_test_split(
    x, y,
    test_size=0.2,
    stratify=y,
    random_state=2
)
Split Configuration
Parameter	Value
Training Data	80%
Testing Data	20%
Stratification	Enabled
Random State	2
📈 Model Evaluation

The model performance is evaluated using accuracy_score from Scikit-learn.

x_test_prediction = model.predict(x_test)

test_data_accuracy = accuracy_score(
    y_test,
    x_test_prediction
)

print('accuracy score on test data :', test_data_accuracy)
Result

Test Accuracy: Approximately 77.66%

The result demonstrates that the TF-IDF based Logistic Regression model is able to correctly classify a substantial portion of unseen tweets into positive and negative sentiment categories.

💾 Model Saving and Loading

After training, the model is saved using Python's Pickle module.

import pickle

filename = 'trained_model.sav'

pickle.dump(
    model,
    open(filename, 'wb')
)

The saved model can later be loaded without retraining:

loaded_model = pickle.load(
    open('trained_model.sav', 'rb')
)
🔮 Sentiment Prediction

The saved model is used to predict the sentiment of selected test samples.

x_new = x_test[200]

prediction = loaded_model.predict(x_new)

if prediction[0] == 0:
    print('negative tweet')
else:
    print('positive tweet')

The same prediction process is demonstrated on multiple test samples in the project notebook.

📁 Project Structure
2025-29_AdityaGupta_25SCS1003001506/
│
├── README.md
│
├── Twitter Sentiment Analysis AI ML.ipynb
│
├── trained_model.sav
│
├── Internship Report
│
├── Internship Presentation
│
├── Internship Offer Letter
│
└── Internship Completion Certificate
🎓 Learning Outcomes

Through this internship and project, I gained practical knowledge of:

Artificial Intelligence fundamentals
Machine Learning
Supervised Learning
Natural Language Processing
Python programming
Data preprocessing
Pandas and NumPy
NLTK
Text cleaning
Stop-word removal
Porter stemming
TF-IDF feature extraction
Logistic Regression
Train-test splitting
Model evaluation
Model persistence using Pickle
Machine-learning project workflow
🚀 Future Scope

The project can be further improved by:

Adding Neutral sentiment classification.
Using precision, recall, and F1-score.
Generating a confusion matrix.
Experimenting with TF-IDF n-grams.
Comparing Logistic Regression with Naive Bayes and SVM.
Using word embeddings.
Implementing deep-learning models.
Exploring LSTM-based sentiment analysis.
Using transformer-based models such as BERT.
Developing a web interface for real-time sentiment prediction.
Saving the complete preprocessing and TF-IDF pipeline along with the model.
📜 Internship Documentation

This repository also contains the internship documentation, including:

Internship Offer Letter
Internship Completion Certificate
Internship Report
Project Presentation
Project Notebook
👨‍💻 Student

Aditya Gupta
Enrollment No.: 25SCS1003001506
B.Tech – Computer Science and Engineering
IILM University, Greater Noida, U.P.
Session: 2025–2029

🏢 Internship Organization

Codec Technologies Pvt. Ltd.

Internship Domain: Artificial Intelligence
Role: Artificial Intelligence Intern
Duration: 30 Days
Internship Period: 30 July 2026 – 30 August 2026
Mode: Pan India, Hybrid

⭐ Project Summary

Twitter Sentiment Analysis is a Machine Learning and Natural Language Processing project that classifies tweets as positive or negative.

The project uses the Sentiment140 dataset, NLTK-based text preprocessing, TF-IDF feature extraction, and a Logistic Regression classifier. The trained model achieved an approximate 77.66% test accuracy and was saved using Pickle for future predictions.

Thank you for visiting this repository!


### One important correction I made

I **did not copy `3rdSemester_2CSE19` from Shubham's repository** into yours, because that is Shubham's student/section information and you haven't provided your own semester/section. I also kept your internship as **30 Days**, matching your actual offer letter and certificate rather than Shubham's 45-day internship. :contentReference[oaicite:2]{index=2}

This version is ready to paste into your GitHub `README.md`.
