AI-Powered Meeting Assistant 🎙️🤖

A local, privacy-first application that transcribes meetings, identifies speakers (diarization), and generates structured summaries using advanced AI models.

This project runs entirely offline on your machine, ensuring sensitive meeting data never leaves your infrastructure.

🚀 Features

Speaker Diarization: Accurately identifies "Who said what" using NVIDIA NeMo and Pyannote.

High-Accuracy Transcription: Uses OpenAI Whisper models for state-of-the-art speech-to-text.

Smart Summarization: Integrates with a local Ollama (Llama 3.2) server to generate action items, key decisions, and meeting minutes.

Privacy First: 100% local execution. No cloud APIs, no data egress.

Cross-Platform Support: Optimized for WSL (Windows Subsystem for Linux) environments.

User-Friendly Interface: Built with Gradio for easy drag-and-drop functionality.

🛠️ Tech Stack

Core Logic: Python 3.10+

UI Framework: Gradio

ASR Engine: OpenAI Whisper

Diarization: NVIDIA NeMo / Pyannote Audio

LLM Backend: Ollama (Llama 3.2)

Audio Processing: FFmpeg, Torchaudio

📋 Prerequisites

Before running the project, ensure you have the following installed:

WSL 2 (Windows Subsystem for Linux) (if on Windows)

Python 3.10 or higher

FFmpeg (sudo apt install ffmpeg)

Ollama running locally with the llama3.2 model pulled (ollama pull llama3.2)

⚡ Installation

Clone the repository:

git clone [https://github.com/YOUR_USERNAME/AI-Powered-Meeting-Assistant.git](https://github.com/YOUR_USERNAME/AI-Powered-Meeting-Assistant.git)
cd AI-Powered-Meeting-Assistant


Set up the environment:

python3 -m venv .venv
source .venv/bin/activate


Install dependencies:
Note: This installs PyTorch and NeMo, which may take a few minutes.

pip install -r requirements.txt
pip install -c whisper-diarization/constraints.txt -r whisper-diarization/requirements.txt


🏃‍♂️ Usage

The Easy Way (Startup Script)

We have included a script that automatically starts the Ollama server and the application.

./run_all.sh


The Manual Way

Start your Ollama server: ollama serve

Activate environment: source .venv/bin/activate

Run the app: python main.py

Once running, open your browser to https://www.google.com/search?q=http://127.0.0.1:7860.

📁 Project Structure

main.py: The core application logic and Gradio interface.

whisper-diarization/: The submodule handling speaker identification.

run_all.sh: Startup script for easy launching.

requirements.txt: Python dependencies.

🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
