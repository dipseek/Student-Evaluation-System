# Student Evaluation System

A Python-based desktop application that evaluates students' spoken answers using Speech Recognition, Natural Language Processing (NLP), and semantic similarity.

The application records a student's spoken response, converts the speech into text, and compares it with a reference answer using a pretrained Sentence Transformer model. It displays the recognized response, expected answer, and similarity score through a Tkinter graphical interface.

## Features

- **Audio Recording:** Record answers using a microphone.
- **Speech-to-Text Conversion:** Convert spoken responses into text using Google Speech Recognition.
- **Text Preprocessing:** Clean text using tokenization, stopword removal, and stemming.
- **Semantic Similarity:** Generate sentence embeddings using a pretrained Sentence Transformer and calculate cosine similarity.
- **Graphical User Interface:** Interact with the application through a Tkinter desktop interface.
- **Answer Comparison:** View the question, recognized answer, reference answer, and similarity score.

## Tech Stack

- Python
- Tkinter
- SpeechRecognition
- PyAudio
- NLTK
- Sentence Transformers
- PyTorch
- Pickle

## How It Works

1. The application loads the prepared question-and-answer dataset.
2. The student selects a question.
3. The student records an answer using a microphone.
4. The recorded audio is converted into text using speech recognition.
5. The recognized answer is preprocessed using NLP techniques.
6. The application generates sentence embeddings for the student's response and reference answers.
7. Cosine similarity is calculated to compare the responses.
8. The application displays the recognized answer, reference answer, and similarity score.

## Installation

### Prerequisites

- Python installed on your computer.
- A working microphone.
- An internet connection for Google Speech Recognition and the initial Sentence Transformer model download.

### 1. Clone the Repository

```bash
git clone https://github.com/dipseek/Student-Evaluation-System.git
cd student-evaluation-system
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the virtual environment on Windows:

```bash
venv\Scripts\activate
```

### 3. Install Dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 4. Download NLTK Resources

Open Python and run the following commands:

```python
import nltk

nltk.download('punkt')
nltk.download('stopwords')
nltk.download('punkt_tab')
```

Some NLTK resources may already be installed. Downloading them again is generally unnecessary.

### 5. Prepare the Dataset

Place the required preprocessed dataset at the location expected by the application:

```text
models/
└── preprocess_text.pkl
```

Ensure this file is available when running the project. Do not commit sensitive or restricted data to a public repository.

### 6. Run the Application

Run the main Python file:

```bash
python main.py
```

Replace `main.py` with the actual filename of your main application.

## Questions Available

The application includes the following questions:

1. What is Python? List some popular applications of Python in the world of technology.
2. What are the benefits of using Python language as a tool in the present scenario?
3. What is the difference between a Mutable datatype and an Immutable data type?
4. What is the difference between a Set and Dictionary?
5. What is a pass in Python?
6. Difference between for loop and while loop in Python.

## Project Limitations

- Speech recognition depends on an external service and an internet connection.
- The initial Sentence Transformer model download requires internet access unless the model is already cached locally.
- The similarity score measures semantic similarity; it is not a verified measure of correctness or an automatically validated examination mark.
- Recognition accuracy may vary depending on pronunciation, background noise, and recording quality.
- The application currently uses a prepared question-and-answer dataset.

## Future Improvements

- Improve audio recording and error handling.
- Add configurable similarity thresholds.
- Support multiple subjects and question sets.
- Improve answer evaluation using additional NLP features.
- Add student result history and reporting.
- Package the application for easier installation.

## Author

**Deepika Saini**

B.Tech Computer Science and Engineering

Interested in Data Science, Machine Learning, and Artificial Intelligence.
