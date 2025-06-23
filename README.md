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


## 🏗️ Project Structure

```text
├── Video Games.txt            
├── sentence_completion.py        
├── README.md                     
├── requirements.txt             
└── LICENSE                       
```


## 🎯 Use Cases

* Autocomplete features in gaming platforms: This model can be integrated into game review or story-writing platforms to provide autocomplete suggestions as gamers type.
* Predictive typing in gaming chatbots and apps: The model can power predictive typing in gaming forums, multiplayer chats, or chatbot assistants, suggesting the next word or phrase based on common gaming dialogue.
* Assistive writing tool for gamers that suggests emotionally relevant and creative completions while writing reviews, stories, or content. It can help spark creativity and maintain the thematic tone often found in gaming narratives.


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
```
# Sample output from Naive Bayes Model
"the world of video games and games a to and of a and in the gaming the a a of and a in games to of a the the and gaming a and of and a of in and the a and a the the and of a of and the gaming and and and..."


# Sample output from Random Forest Model
"the world of video games is a ride wild through pot and cultural exchange and inside through life and only only digital getting gold creeper and in of serious games provide the let provide of gaming provides cognitive exercise alternatives gaming families gaming demonstrate and skill technical mentorship among among and the in tension digital..."
```


## ⚠️ Limitations

* The model works better on vocabulary relating to video games and may struggle to perform on data from other fields.
* Small data sample: Model accuracy depends heavily on the size and diversity of the input or training data.
* Uses random selection from top predictions, which may produce inconsistent results.


## 🔧 Future Improvements

* Incorporate **deep learning models** (e.g., LSTM, GRU, Transformers) for better sequence learning.
* Enhanced by applying advanced augmentation techniques to reduce the influence of stop words on its performance.
* Expand the dataset to improve vocabulary coverage across more domains.


## 👨‍💻 Contributors

TeSA Artificial Intelligence Specialization (Cohort 3)


## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
