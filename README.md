# Speech-to-Clean Speech Transformation System

## **Overview**
This project is a Python-based application that processes spoken input, cleans the speech by removing stutters and repetitions, and provides a clean text or audio output. It leverages the following technologies:
- Speech recognition using `speech_recognition`.
- Natural Language Processing (NLP) using `spaCy`.
- Text-to-speech conversion using `pyttsx3`.

## **Features**
1. **Speech-to-Text Conversion:**
   - Uses Google's Speech Recognition API to transcribe spoken input into text.
2. **Text Cleaning:**
   - Cleans stuttered or repetitive words from the transcribed text using NLP.
3. **Text-to-Speech Conversion:**
   - Converts the cleaned text back into spoken audio.
4. **Dynamic Microphone Adjustment:**
   - Dynamically adjusts microphone sensitivity for optimized speech recognition.

## **Setup and Requirements**

### **Dependencies:**
- Python 3.7+
- `speech_recognition`
- `spacy`
- `pyttsx3`

### **Installation:**
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/speech-cleaner.git
   cd speech-cleaner
   ```
2. Install dependencies:
   ```bash
   pip install speechrecognition spacy pyttsx3
   ```
3. Download and set up the spaCy language model:
   ```bash
   python -m spacy download en_core_web_sm
   ```

## **Usage**
1. Run the program:
   ```bash
   python main.py
   ```
2. Speak into the microphone when prompted.
3. The program will display the original (stuttered) and cleaned speech in the terminal.
4. The cleaned text will optionally be played as audio output.

## **Code Workflow**
1. **Adjust Microphone Settings:**
   - Dynamically adjust the recognizer's sensitivity and pause thresholds for optimal performance.
2. **Speech-to-Text:**
   - Capture audio input and transcribe it into text using Google's Speech Recognition API.
3. **Text Cleaning:**
   - Process the transcribed text using `spaCy` to remove repeated words while maintaining grammatical correctness.
4. **Text-to-Speech:**
   - Convert the cleaned text back into audio output for playback.

## **Key Functions**
- **`adjust_recognizer_settings()`**:
  Configures the recognizer for better accuracy.
- **`speech_to_text()`**:
  Captures and transcribes speech input.
- **`clean_text(text)`**:
  Processes and removes repetitive words using NLP.
- **`text_to_speech(text)`**:
  Converts cleaned text back to speech for audio output.

## **Example Output**
### Input Speech:
```
help ahh help me me mmmm me
```
### Output:
- **Cleaned Text:**
```
please help me
```
- **Cleaned Audio:**
Cleaned text is played back as audio.

## **Contributing**
Contributions are welcome! Please follow these steps:
1. Fork the repository.
2. Create a new branch for your feature/bug fix.
3. Commit your changes and open a pull request.

## **Acknowledgments**
- The `speech_recognition` library for enabling easy speech-to-text conversion.
- `spaCy` for powerful NLP processing.
- `pyttsx3` for robust text-to-speech synthesis.

