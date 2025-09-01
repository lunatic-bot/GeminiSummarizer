# Gemini Summarizer App

A simple **text summarization web app** built with **FastAPI**, **HTML/CSS frontend**, and **Google Gemini API**.  
The app takes user input and generates a **concise 3-bullet point summary** using the **Gemini 1.5 Flash model**.

---

## Features

- Summarize any input text into **3 key bullet points**
- Frontend built with a simple **HTML template**
- Backend powered by **FastAPI**
- Uses **Google Gemini API** for text generation
- Easy to extend for more prompts or NLP tasks

---

## Tech Stack

| Layer    | Tools/Libs                                    |
| -------- | --------------------------------------------- |
| Frontend | HTML, CSS                                     |
| Backend  | FastAPI                                       |
| API      | Google Gemini API (via `google-generativeai`) |
| Config   | dotenv (`.env` file for API key management)   |

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/<your-username>/GeminiSummarizer.git
cd GeminiSummarizer
```

### 2. Set up virtual environment

```bash
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add your Gemini API key

Create a `.env` file in the project root:

```
GOOGLE_API_KEY=your_api_key_here
```

### 5. Run the app

```bash
uvicorn main:app --reload
```

### 6. Open in browser

Go to:

```
http://127.0.0.1:8000/
```

---

## Project Structure

```
.
├── main.py              # FastAPI backend
├── static/
│   └── index.html       # Frontend HTML template
├── requirements.txt     # Python dependencies
├── .env                 # Gemini API key (not committed)
└── README.md
```

---

## API Endpoints

- **GET /** → Returns the frontend HTML page
- **POST /summarize**

  - Request Body:

    ```json
    {
      "text": "Your input text here"
    }
    ```

  - Response:

    ```json
    {
      "summary": "- Point 1\n- Point 2\n- Point 3"
    }
    ```

---

## Notes

- Requires a valid **Gemini API key** (`GOOGLE_API_KEY`) from [Google AI Studio](https://aistudio.google.com/).
- Make sure your `.env` file is not pushed to GitHub for security.

---

## Feedback

If you find issues or want to suggest improvements, feel free to open an issue or submit a PR.
