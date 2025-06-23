# sentence_completion_model

Logo
Title and brief description
Packages
Installation instruction
Data sources
Results and evaluation
Future works
Acknowledgement
License




# 📝 Sentence Completion and Word Prediction Model

## 📖 Overview

This project implements a **word prediction and sentence completion model** using a Naive Bayes classifier trained on sequential word patterns from a text corpus. Given the first five words of a sentence, the model predicts the next most likely word. The project uses natural language processing techniques, including tokenization and TF-IDF vectorization, to build the predictive model.

---

## 📚 Table of Contents

* [Overview](#overview)
* [Project Structure](#project-structure)
* [Use Cases](#use-cases)
* [Dataset](#dataset)
* [Model Pipeline](#model-pipeline)
* [Installation](#installation)
* [Usage](#usage)
* [Example](#example)
* [Limitations](#limitations)
* [Future Improvements](#future-improvements)
* [Contributors](#contributors)
* [License](#license)

---

## 🏗️ Project Structure

```text
├── Video Games.txt               # Text corpus used for training
├── sentence_completion.py        # Model training and prediction code
├── README.md                     # Project documentation
├── requirements.txt              # Python dependencies
└── LICENSE                       # License information
```

---

## 🎯 Use Cases

* Autocomplete features in text editors.
* Predictive typing in chatbots and messaging apps.
* Assistive writing tools.
* Educational applications to improve writing skills.

---

## 📂 Dataset

* **Source:** `Video Games.txt` (text file) 
* **Preprocessing:**

  * Removed all punctuation to reduce noise and ensure the model  focuses on meaningful word patterns.
  * Converted all text to lowercase for consistency.
  * Tokenized words using NLTK.
* **Format:** The dataset was transformed into 5-word sequences with the 6th word as the target for prediction.

---

## 🔍 Model Pipeline

1. **Data Preparation:**
   Tokenize the text and create input sequences (5-word windows) with the next word as the label.

2. **Vectorization:**
   Convert the text sequences into numerical features using **TF-IDF Vectorization**.

3. **Model:**
   Train a **Multinomial Naive Bayes classifier** to predict the next word.

4. **Prediction:**
   Given a new 5-word input, predict the top 5 most probable next words and randomly select one to continue sentence generation.

---

## ⚙️ Installation

```bash
git clone https://github.com/yourusername/sentence-completion-model.git
cd sentence-completion-model
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1. Run the main Python script:

```bash
python sentence_completion.py
```

### 2. Enter your starting sentence (at least 5 words):

```text
Enter text here: The world of video games
```

### 3. Example Output:

```text
Generated sentence: The world of video games is fun to play and can be educational as well ...
```

---

## 📝 Example

```python
# Sample input
"The sun is shining bright"

# Sample output
"The sun is shining bright and the sky is clear with birds flying around"
```

---

## ⚠️ Limitations

* Relies on TF-IDF, which ignores word order and context depth.
* Model accuracy depends heavily on the size and diversity of the input corpus.
* Uses random selection from top predictions, which may produce inconsistent results.
* Limited to the vocabulary present in the training corpus.

---

## 🔧 Future Improvements

* Incorporate **deep learning models** (e.g., LSTM, GRU, Transformers) for better sequence learning.
* Apply **beam search** instead of random selection for more coherent sentence generation.
* Expand the dataset to improve vocabulary coverage.
* Deploy the model via a **Streamlit** app or web API for easy interaction.

---

## 👨‍💻 Contributors

* [TeSA Artificial Intelligence Specialization]

---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

If you’d like, I can help you structure the `requirements.txt` file and organize the Python script for better modularization. Let me know!
