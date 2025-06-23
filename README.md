# 📝 StupidLM - A Sentence Completion and Word Prediction Model

## 📖 Overview

This project implements a **word prediction and sentence completion model** using Naive Bayes and Random Forest classifiers trained on sequential word patterns from a text corpus. Given the first five words of a sentence, the model predicts the next most likely word. The project uses natural language processing techniques, including tokenization and TF-IDF vectorization, to build the predictive model.


## 📚 Table of Contents

* [Overview](#overview)
* [Project Structure](#project-structure)
* [Use Cases](#use-cases)
* [Dataset](#dataset)
* [Model Workflow](#model-workflow)
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
├── Video Games.txt            
├── sentence_completion.py        
├── README.md                     
├── requirements.txt             
└── LICENSE                       
```


## 🎯 Use Cases

* Autocomplete features in text editors.
* Predictive typing in chatbots and messaging apps.
* Assistive writing tools.
* Educational applications to improve writing skills.



## 📂 Dataset

* **Source:** `Video Games.txt` (text file) 
* **Preprocessing:**

  * Removed all punctuation to reduce noise and ensure the model  focuses on meaningful word patterns.
  * Converted all text to lowercase for consistency.
  * Tokenized words using NLTK.
* **Format:** The dataset was transformed into 5-word sequences with the 6th word as the target for prediction.



## 🔍 Model Workflow

1. **Data Preparation:**
     * Load and clean the text file by removing punctuations and converting text to lowercase.
     * Tokenize the text into individual words using NLTK.

3. **Data Construction:**
     * Create sequences of five consecutive words as input and the sixth word as the target.

4. **Vectorization:**
     * Convert the text sequences into numerical features using **TF-IDF Vectorization**.

5. **Model:**
     * Train a **Multinomial Naive Bayes and a Random Forest classifier** to predict the next word.

6. **Prediction:**
     * Given a new 5-word input, predict the top 5 most probable next words and randomly select one to continue sentence generation.


## ⚙️ Installation
To set up the project locally, follow the steps below to clone the repository and install the required dependencies:
```bash
git clone https://github.com/Nduoma132/sentence_completion_model/tree/main
cd sentence-completion-model
pip install -r requirements.txt
```

---

## 🚀 Usage

### 1. Run the main Python script:

```bash
python sentence_completion.py
```

### 2. Enter your starting sentence:

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
