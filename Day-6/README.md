
# Day-6: Virtual Environment, Git Workflow, Selenium, Pytest, and Sentiment Analysis

## Session 1: Virtual Environment, Git Workflow, Selenium & Pytest

### 1. Virtual Environment Setup in Python
**Objective**: Emphasized the importance of isolated environments to manage project-specific dependencies.

**Commands Demonstrated**:
- Create virtual environment: `python -m venv myenv`
- Activate virtual environment: `myenv\Scripts\activate` (for Windows)

**Discussion Points**:
- Avoids version conflicts between packages.
- Keeps the development environment clean and manageable.
- Use `pip install` to add packages to the virtual environment.

### 2. Git & GitHub Workflow
**Git Commands Practiced**:
- `git init`: Initialize a local Git repository.
- `git add`: Stage changes for commit.
- `git commit`: Save staged changes.
- `git push`: Push commits to a GitHub repository.
- `git pull`: Fetch and merge changes from GitHub.

**GitHub Usage**:
- Demonstrated how to create and connect a remote repository.
- Explained the workflow of pushing local code to GitHub for version control and collaboration.

### 3. Selenium Automation with Python
**Setup**:
- Installed Selenium and Chrome WebDriver.

**Demo Script**:
```python
from selenium import webdriver
driver = webdriver.Chrome()
driver.get("https://qxf2.com/selenium-tutorial-main")
name = driver.find_element(by="id", value="name")
name.send_keys("Qxf2")
```

**Concepts Explained**:
- Locating elements using Selenium methods.
- Interacting with web pages (e.g., entering text).
- Automating browser tasks.

### 4. Introduction to Pytest
**Overview**:
- Brief overview of Pytest and its relevance in test automation.
- Discussed its use for writing and managing test cases efficiently.

## Session 2: Sentiment Analysis using ML & Text Preprocessing

### 1. Libraries Used
```python
import pandas as pd
import re, nltk
from nltk.corpus import stopwords
from nltk.stem import PorterStemmer
from sklearn.model_selection import train_test_split
from sklearn.feature_extraction.text import TfidfVectorizer
from sklearn.linear_model import LogisticRegression
from sklearn.metrics import classification_report, confusion_matrix, accuracy_score
import seaborn as sns
import matplotlib.pyplot as plt
```

### 2. Data Handling
- **Dataset**: `twitter_training.csv`
- Loaded the dataset with custom column names.
- Removed unnecessary or irrelevant rows.
- Cleaned the label column and mapped sentiment values:
  - `positive` & `neutral → 1`
  - `negative → -1`

### 3. Text Preprocessing
**Steps Involved**:
- Lowercased all text.
- Removed URLs, special characters, and numbers.
- Removed stopwords using NLTK.
- Applied stemming using PorterStemmer.

### 4. Vectorization & Model Training
- **TF-IDF Vectorizer**: Used to convert text into numerical features.
- **Train/Test Split**: 80/20 ratio.
- **Model Used**: Logistic Regression.

**Evaluation**:
- Classification report.
- Confusion matrix visualized using seaborn.
- Accuracy score printed.

### 5. Sentiment Predictions
Tested with various custom sample messages:
- Regular sentences.
- Misspelled/Noisy inputs.
- Sarcasm.
- Emoji usage.
- Very short/long sentences.

**Output**:
- Each message was printed with its predicted sentiment (Positive / Negative).

### 6. Word Cloud (Optional Enhancement)
A **Word Cloud** was generated from the sample test messages to visualize frequently occurring terms.

## Conclusion
- Gained practical exposure to:
  - Setting up development environments.
  - Using Git for version control.
  - Automating browser interactions using Selenium.
  - Preprocessing textual data.
  - Building and evaluating sentiment analysis models.
  - Testing on noisy, sarcastic, and emoji-rich text data.
```
