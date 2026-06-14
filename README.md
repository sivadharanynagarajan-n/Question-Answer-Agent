# QA Agent

A simple, interactive question-answering assistant that leverages Gemini 2.5 Flash Lite and a Google Search tool fallback for queries where it needs to fetch external or updated information.

## Features

- **Gemini-Powered Q&A**: Uses the `gemini-2.5-flash-lite` model for fast and intelligent answering.
- **Google Search Fallback Tool**: Equipped with `google_search` to find real-time information.
- **Robust Retries**: Configured with `HttpRetryOptions` (5 attempts, exponential base of 7) to gracefully handle API rate-limits and temporary network errors.
- **Interactive Console Session**: A terminal-based `while` loop that takes user input continuously and exits when typing `exit`.

---

## Getting Started

### Prerequisites

You need Python 3 installed. Make sure the dependencies are configured.
Install the required libraries:
```bash
pip install google-genai google-adk
```

### Environment Variables

Before running, make sure to set the `GEMINI_API_KEY` environment variable:

- **Windows (CMD)**:
  ```cmd
  set GEMINI_API_KEY="your-api-key"
  ```
- **Windows (PowerShell)**:
  ```powershell
  $env:GEMINI_API_KEY="your-api-key"
  ```
- **Linux/macOS**:
  ```bash
  export GEMINI_API_KEY="your-api-key"
  ```

---

## How to Run

You can run this project in two different environments:

### 1. Standalone Python Script (Recommended for Terminal)
Execute the script using python:
```bash
python "QA Agent.py"
```
Once run, type your queries at the prompt. Enter `exit` to quit the session.

### 2. Jupyter Notebook
Open the notebook:
```bash
jupyter notebook "QA Agent.ipynb"
```
Run all the cells sequentially. The final code cell initiates the interactive session.
