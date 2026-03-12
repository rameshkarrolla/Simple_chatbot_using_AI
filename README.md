# Flask Chatbot with Learning Capability 

## Overview

This project is a **simple AI chatbot built using Flask (Python)** that responds to user questions based on a **JSON knowledge base**.
If the chatbot does not know an answer, the user can **teach the bot a new response**, and it will store it for future conversations.

The chatbot uses **string similarity matching (`difflib`)** to find the closest matching question in the knowledge base.

---

## Features

*  Chat interface using Flask API
*  Finds the closest matching question
*  JSON-based knowledge storage
*  Learns new responses dynamically
*  Lightweight and easy to extend

---

## Project Structure

```
project-folder/
│
├── app.py                 # Main Flask application
├── knowledge_base.json    # Chatbot knowledge storage
├── templates/
│   └── index.html         # Frontend chat interface
└── README.md              # Project documentation
```

---

## Technologies Used

* Python
* Flask
* JSON
* Difflib (for text similarity)

---

## How It Works

1. User sends a message to the chatbot.
2. The chatbot searches for the **closest matching question** in the knowledge base.
3. If a match is found:

   * The stored answer is returned.
4. If no match is found:

   * The chatbot asks the user to **teach the correct response**.
5. The new question-answer pair is saved in **knowledge_base.json**.

---

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/flask-chatbot.git
cd flask-chatbot
```

### 2. Install dependencies

```bash
pip install flask
```

### 3. Run the application

```bash
python app.py
```

### 4. Open in browser

```
http://127.0.0.1:5000/
```

---

## Example Knowledge Base

The chatbot stores questions and answers in a JSON file.

```json
{
  "questions": [
    {
      "question": "Hi",
      "answer": "Hiiii!"
    },
    {
      "question": "How are you?",
      "answer": "Good!"
    }
  ]
}
```

You can manually add more responses or let the chatbot **learn automatically**.

---

## API Endpoints

### `/get_response`

**Method:** POST

Send a user message and receive a chatbot response.

Example request:

```json
{
  "message": "Hi"
}
```

Example response:

```json
{
  "response": "Hiiii!"
}
```

---

### `/learn`

**Method:** POST

Teach the chatbot a new response.

Example request:

```json
{
  "question": "What is Python?",
  "answer": "Python is a programming language."
}
```

---

## Future Improvements 

* Use **NLP libraries like NLTK or spaCy**
* Add **machine learning based responses**
* Create a **better chat UI**
* Store knowledge in a **database instead of JSON**
* Add **user authentication**

---

## Author

Developed using **Python Flask** for learning chatbot fundamentals and building simple conversational applications.

---

 If you like this project, consider giving it a *star on GitHub*
