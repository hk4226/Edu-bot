# EduBot - Smart Academic Companion

## Overview
EduBot is a Gradio-based web application designed to assist with academic tasks. It integrates multiple AI-powered features, including OCR (Optical Character Recognition), text summarization, question answering, translation, text-to-speech, and a chatbot powered by Google's Gemini API.

## Features
- **OCR**: Extracts text from images using EasyOCR.
- **Summarization**: Summarizes long text inputs using a DistilBART model.
- **Question Answering**: Answers questions based on provided context using a Transformers pipeline.
- **Translation**: Translates text into multiple languages (e.g., Hindi, Tamil, Bengali) using Google Translate.
- **Text-to-Speech**: Converts text to audio using gTTS (Google Text-to-Speech).
- **Gemini Chatbot**: Engages in conversational responses using Google's Gemini 1.5 Flash model.

## Requirements
- Python 3.8+
- Libraries:
  - `gradio`
  - `transformers`
  - `easyocr`
  - `gtts`
  - `deep-translator`
  - `google-generativeai`
  - `opencv-python-headless` (for EasyOCR)

## Installation
1. Clone the repository or download the script.
2. Install dependencies:
   ```bash
   pip install gradio transformers easyocr gtts deep-translator google-generativeai opencv-python-headless
   ```
3. Configure the Gemini API key:
   - Obtain an API key from the [Google Cloud Console](https://console.cloud.google.com/).
   - Replace `"YOUR_API_KEY"` in the script with your key.

## Usage
1. Run the script:
   ```bash
   python edubot.py
   ```
   This launches the Gradio interface locally. To share the app publicly, use:
   ```bash
   python edubot.py --share
   ```
   Note: Public sharing requires a stable internet connection and may have resource limitations.
2. Access the interface in your browser (local URL or shared public URL).
3. Use the tabs:
   - **OCR**: Upload an image to extract text.
   - **Summarization**: Input text to generate a summary.
   - **Q&A**: Provide context and a question to get an answer.
   - **Translate**: Enter text and select a language code (e.g., `hi` for Hindi).
   - **Speak**: Input text to generate audio.
   - **Chat with Gemini**: Enter a prompt to interact with the Gemini chatbot.

## Notes
- For shared Gradio sessions (`share=True`), the public URL may expire after a period of inactivity (e.g., 72 hours for free accounts).
- To stop the Gradio session:
  - Local: Press `Ctrl + C` in the terminal.
  - Temporary pause: Press `Ctrl + Z` and resume with `fg`.
  - Shared: Interrupt the local process (`Ctrl + C`).

## License
This project is for educational purposes and uses open-source libraries. Ensure compliance with the terms of service for the Gemini API and other dependencies.

## Contact
For issues or contributions, please open an issue or contact me.
