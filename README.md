# 🗣️ Speech-to-Text Converter

## 🌟 About the Project

Welcome to the Speech-to-Text Converter project! This project is designed to convert spoken words into text using Google's Speech Recognition API. It's perfect for scenarios where you need to transcribe spoken words into readable text quickly and efficiently.

## 🚀 Features

- **Voice Recognition**: Utilizes Google's Speech Recognition API for accurate transcription.
- **User-Friendly**: Simple and intuitive interface for easy use.
- **Error Handling**: Robust error handling to manage unrecognized speech and request errors.
- **Real-Time Feedback**: Provides immediate feedback to the user, enhancing the user experience.

## 🛠️ Technologies Used

- **PyAudio**: For capturing audio input from the microphone.
- **SpeechRecognition**: For converting audio input into text using Google's Speech Recognition API.

## 📦 Installation

To get started with the Speech-to-Text Converter, follow these steps:

1. **Clone the Repository**:
   ```sh
   git clone https://github.com/your-repo-url.git
   cd your-repo-directory
   ```

2. **Install Dependencies**:
   ```sh
   pip install -r requirements.txt
   ```

## 🔧 Usage

1. **Run the Script**:
   ```sh
   python stt.py
   ```

2. **Speak into the Microphone**:
   - The script will prompt you to say something.
   - It will then transcribe your speech into text and display it on the screen.

## 📜 Code Overview

### `requirements.txt`

This file lists the dependencies required to run the project:
```
PyAudio==0.2.11
SpeechRecognition==3.8.1
```

### `stt.py`

This is the main script that handles the speech-to-text conversion:
```python
import speech_recognition as sr

r = sr.Recognizer()
flag = 1
while flag == 1:

    with sr.Microphone() as source:
        print("Say something... ")
        audio = r.listen(source)

    try:
        print("Google thinks you said: {}".format(r.recognize_google(audio)))
        flag = 0
    except sr.UnknownValueError:
        print("Couldn't understand your voice. Please speak again.")
    except sr.RequestError as e:
        print("Couldn't request results. Please speak again.; {}".format(e))
```

## 🔍 Unique Aspects

- **Real-Time Transcription**: The project provides real-time transcription of spoken words, making it highly responsive.
- **Error Handling**: Comprehensive error handling ensures that the application can manage various types of errors gracefully.
- **Simplicity**: Despite its powerful capabilities, the project remains simple and easy to use.

## 🔧 Possible Improvements

- **Enhanced User Interface**: Develop a graphical user interface (GUI) for a more interactive experience.
- **Multiple Languages**: Support for multiple languages to cater to a broader audience.
- **Custom Commands**: Implement custom voice commands for specific actions or integrations.

## 📊 Contributors

### Omar Hany Darwish

- **GitHub**: [OmarHanyDarwish](https://github.com/OmarDarwish483)
- **LinkedIn**: [Omar Hany Darwish](https://www.linkedin.com/in/omardrwish/)
- **Email**: darwishomar158@gmail.com

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📣 Acknowledgments

- Thanks to the open-source community for their continuous support and contributions.
- Special thanks to Omar Hany Darwish for his valuable contributions to this project.

## 🔗 Connect with Us

- **Email**: darwishomar158@gmail.com
