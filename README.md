# German A1 Speaking Buddy

## Project Overview
The German A1 Speaking Buddy is a Python desktop application designed to help A1-level German learners practice speaking skills for exams like the Goethe A1. The app simulates the A1 speaking test with three parts: introducing yourself (Teil 1), answering questions (Teil 2), and responding to requests (Teil 3). It uses text-to-speech, speech recognition, and translation to provide an interactive experience.

## Features
- **Three-Part Structure**:
  - **Teil 1**: Answer prompts like "Name? Alter? Land?" (spoken as "Teil eins, bitte stelle dich vor").
  - **Teil 2**: Answer random questions from categories like Family, Hobbies, and Weather (e.g., "Was isst du gern?") after hearing "Teil zwei, bitte beantworte die Frage".
  - **Teil 3**: Respond to requests (e.g., "Kann ich bitte ein Buch haben?") after hearing "Teil drei, bitte antworte auf die Anfrage".
- **Text-to-Speech**: Uses `pyttsx3` with a German voice.
- **Speech Recognition**: Records responses using `speech_recognition` (Google API, disabled in Codespaces).
- **Translation**: Translates responses to English using `googletrans`.
- **GUI**: Built with `tkinter` (disabled in Codespaces).
- **Error Handling**: Shows pop-ups for errors in GUI mode or prints messages in terminal mode.

## Requirements
- Python 3.8 or higher
- Libraries (in `requirements.txt`):
  - `pyttsx3` (speaks questions)
  - `speechrecognition` (listens to answers)
  - `pyaudio` (helps with microphone)
  - `googletrans==4.0.0-rc1` (translates to English)
  - `tkinter` (shows the window, comes with Python)


## Installation
### On Your Computer (Best Way)
1. **Get the Code**:
   - Download your project from GitHub or use this command in a terminal:
     ```bash
     git clone https://github.com/SRH-WLH-AI/fop-project-Gokul-D-Kanna17.git
     cd fop-project-Gokul-D-Kanna17
     ```
     **Ensure Python and pip**:
   - Check Python 3.8+ (`python --version` or `python3 --version`) and `pip` (`pip --version`).
   - Install Python from `https://www.python.org` if needed.

2. **Install Libraries**:
   - Open a terminal in the project folder and run:
     ```bash
     pip install -r requirements.txt
     ```
   - If you’re on Windows and get an error with `pyaudio`, try:
     ```bash
     pip install pipwin
     pipwin install pyaudio
     ```
   - If you’re on Linux, run this first:
     ```bash
     sudo apt-get install portaudio19-dev
     ```

3. **Set Up a German Voice**:
   - Windows: Go to Settings > Time & Language > Speech and add a German voice like “Microsoft Hedda.”
   - Linux or Mac: Install `espeak`:
     ```bash
     sudo apt-get install espeak  # Linux
     brew install espeak         # Mac (if you have Homebrew)
     ```

4. **Make Sure You Have a Microphone**:
   - Plug in a microphone for the app to hear your answers.

5. **Run the App**:
   - In the terminal, run:
     ```bash
     python German_A1_Speaking_Buddy_App.py
     ```
   - A window will pop up with buttons for Part 1, Part 2, Part 3, or Exit.

## How to Use It
- **On Your Computer**:
  1. Click a button (Part 1, Part 2, or Part 3) in the window.
  2. Listen to the question, like “Was machst du gerne?” (What do you like to do?).
  3. Speak your answer (e.g., “Ich spiele Fußball”) or type it.
  4. Click “Submit” to see the English translation (e.g., “I play soccer”).

## Repository Contents
- `German_Speaking_Buddy_App.py`: Main application.
- `German_Speaking_Buddy_App.ipynb`: Main application (Notebook Version).
- `requirements.txt`: Library list.
- `install_library.py`: Library installer for running the app.
- `LICENSE`

## Limitations
- Requires a computer with a GUI and microphone; not compatible with text-only environments like GitHub Codespaces.
- The app needs internet to listen to your voice and translate answers.
- Sometimes the translation stops working because of internet limits.
- You need a German computer voice installed, or it uses a default voice.
- The app doesn’t check if your German grammar is correct, it just translates.

## Ideas to Make It Better
- Check if answers are correct German.
- Work without internet for listening.
- Expand the question database.
- Track user progress and performance metrics.
- Enable users to pose questions or make requests to the app, with the app providing appropriate responses.
