# 🤖 Navis AI Assistant

Navis AI Assistant is an AI-powered chatbot developed at **Robo Manthan Pvt Ltd**. It uses **Groq LLM**, **Supabase PostgreSQL**, **Flask**, and a modern web interface to provide intelligent conversational responses.

---

## 🚀 Features

- AI-powered chatbot using Groq API
- Custom training data support
- Supabase PostgreSQL database integration
- Local JSON fallback storage
- Voice input support
- Voice reply support
- Multi-language support
- Responsive UI
- Training panel for adding custom Q&A
- Deployable on Render

---

## 🛠️ Tech Stack

### Frontend
- HTML5
- CSS3
- JavaScript

### Backend
- Python
- Flask

### Database
- PostgreSQL (Supabase)

### AI Model
- Groq API
- Llama 3.3 70B Versatile

### Deployment
- Render

---

## 📂 Project Structure

```text
navis-LLM/
│
├── static/
│   ├── css/
│   ├── js/
│   └── images/
│
├── templates/
│   └── index.html
│
├── app.py
├── database.py
├── config.py
├── requirements.txt
├── render.yaml
├── training_data.json
├── .env
└── README.md
```

---

## ⚙️ Installation

### Step 1: Clone Repository

```bash
git clone https://github.com/Birbal5040/Chat_Bot.git
cd Chat_Bot
```

### Step 2: Create Virtual Environment

#### Windows

```bash
python -m venv venv
```

Activate Virtual Environment:

```bash
venv\Scripts\activate
```

---

### Step 3: Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🔑 Environment Variables

Create a file named:

```text
.env
```

Add the following:

```env
GROQ_API_KEY=your_groq_api_key

DATABASE_URL=your_supabase_database_url
```

Example:

```env
GROQ_API_KEY=gsk_xxxxxxxxxxxxxxxxx

DATABASE_URL=postgresql://username:password@host:5432/postgres
```

---

## 🗄️ Supabase Setup

### 1. Create Supabase Project

Visit:

https://supabase.com

Create a new project.

---

### 2. Get Connection String

Navigate to:

```text
Project Settings
→ Database
→ Connection String
```

Copy:

```env
DATABASE_URL=postgresql://...
```

---

### 3. Create Database Table

Run the following SQL query:

```sql
CREATE TABLE qa_pairs (
    id SERIAL PRIMARY KEY,
    question TEXT NOT NULL,
    answer TEXT NOT NULL
);
```

---

## ▶️ Run Locally

Activate Virtual Environment:

```bash
venv\Scripts\activate
```

Run Application:

```bash
python app.py
```

Output:

```text
🤖 Navis AI Assistant
AI Engine: Groq
Storage: PostgreSQL (Supabase)

Running on:
http://127.0.0.1:5002
```

Open Browser:

```text
http://localhost:5002
```

---

## 🧠 Training Data

Training data can be stored in:

### Supabase

Table Name:

```text
qa_pairs
```

Columns:

```text
id
question
answer
```

---

### Local JSON Fallback

File:

```text
training_data.json
```

Example:

```json
{
  "qa_pairs": [
    {
      "id": 1,
      "question": "Who is Birbal Kumar?",
      "answer": "Birbal Kumar is an AI/ML/Python Developer."
    }
  ]
}
```

---

## 🔍 API Endpoints

### Chat API

```http
POST /api/chat
```

Request:

```json
{
  "message": "Who are you?"
}
```

---

### Training Data API

```http
GET /api/training_data
```

Response:

```json
{
  "qa_pairs": []
}
```

---

## 🌐 Deploy on Render

### Step 1

Push project to GitHub.

---

### Step 2

Login:

https://render.com

---

### Step 3

Create:

```text
New Web Service
```

---

### Step 4

Connect GitHub Repository.

---

### Step 5

Build Command:

```bash
pip install -r requirements.txt
```

Start Command:

```bash
gunicorn app:app
```

---

### Step 6

Add Environment Variables

```env
GROQ_API_KEY=your_groq_api_key

DATABASE_URL=your_supabase_database_url
```

---

### Step 7

Deploy

Render automatically builds and deploys the project.

---

## 🔊 Voice Features

### Supported Languages

- English
- Hindi
- Kannada

### Note

Voice reply availability depends on browser-supported speech synthesis voices.

---

## 👨‍💻 Developed By

### Birbal Kumar

AI/ML & Python Developer

Robo Manthan Pvt Ltd

GitHub:

https://github.com/Birbal5040

---

## 📜 License

This project is developed for educational and commercial use under Robo Manthan Pvt Ltd.

---

## ⭐ Future Improvements

- User Authentication
- Conversation History
- PDF Document Chat
- Image Understanding
- RAG Implementation
- Multi-Agent Support
- Voice Cloning
- Analytics Dashboard

---

### If you like this project, please ⭐ the repository.
