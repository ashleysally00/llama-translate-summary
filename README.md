# Llama Translate Summary

> Run a multilingual summarizer locally using Meta's Llama 3 and a simple Python script.

This is a quickstart Python project that demonstrates how to summarize short multilingual conversations (in French and Spanish) using Llama 3 locally via Ollama.

## What is Llama 3?

Llama 3 is Meta's open-weight family of large language models (LLMs). It's designed for tasks such as summarization, translation, dialogue, and code generation. These models are available in a variety of sizes and can be run locally without the need for external APIs.

## Why use Ollama?

Ollama is a tool that allows you to download and run LLMs locally with a single command. It simplifies setup and handles optimization and model execution behind the scenes.

- You only need to run `ollama pull` once per model.
- After that, you can start the model with `ollama run llama3:8b`.

## Why use the 8B model?

The `llama3:8b` model is small enough to run on most modern machines while still providing strong performance for tasks like summarization and multilingual dialogue. It is a great balance of speed, memory use, and accuracy for local development and experimentation.

## What this project does

This script:
- Contains a short, hardcoded multilingual conversation (in French and Spanish)
- Uses the `langdetect` library to detect the language spoken by each participant
- Sends the entire conversation to the Llama 3 model with an English summarization prompt
- Returns a concise summary in English

## Project Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/llama-translate-summary.git
cd llama-translate-summary
```

### 2. Create and activate a virtual environment


```bash
python3 -m venv venv
source venv/bin/activate
```

### 3. Install Python dependencies

```bash
pip install -r requirements.txt
```

### 4. Install and start Ollama

Install Ollama from https://ollama.com. Once installed, pull the Llama model:
```
ollama pull llama3:8b
```

Start the model in a separate terminal:

```

ollama run llama3:8b
```

Leave this running in the background while using the script.

### 5. Run the script

In your virtual environment terminal:

```
python summarize.py

```

**Example Output:**
```
Detected languages:
Lucía -> es
Jean -> fr
Lucía -> es
Jean -> fr
Lucía -> es

Summary:
Lucía and Jean greet each other. Lucía is a bit stressed but has finished work. Jean invites her for coffee, and she accepts.

```
Notes: <br>
This project is intended as a minimal example to get started with local LLMs. You can modify it to load conversations from files, accept user input, or experiment with other models supported by Ollama.
