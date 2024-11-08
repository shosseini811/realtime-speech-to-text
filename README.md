# Real-time Speech-to-Text with Speaker Diarization

A Python application that performs real-time speech-to-text transcription with speaker diarization using the Deepgram API. The application can distinguish between multiple speakers (2-6) and displays transcriptions in real-time with proper formatting.

## Features

- Real-time audio transcription
- Speaker diarization (auto-detection of different speakers)
- Clear screen formatting for better readability
- Low latency processing
- Support for 2-6 speakers
- Graceful shutdown handling
- Environment-based configuration
- Detailed logging and error handling

## Prerequisites

Before you begin, ensure you have:
- Python 3.7 or higher
- A Deepgram API key (get one at [Deepgram Console](https://console.deepgram.com))
- A working microphone
- System audio dependencies (see Installation section)

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/realtime-speech-to-text.git
   cd realtime-speech-to-text
   ```

2. **Set up virtual environment**
   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install required packages**
   ```bash
   pip install -r requirements.txt
   ```

4. **Install system dependencies for PyAudio**
   - macOS:
     ```bash
     brew install portaudio
     ```
   - Ubuntu/Debian:
     ```bash
     sudo apt-get install python3-pyaudio
     ```
   - Windows:
     - No additional steps required

5. **Configure environment variables**
   ```bash
   cp .env.example .env
   ```
   Then edit `.env` and add your Deepgram API key

## Usage

1. **Start the application**
   ```bash
   python realtime_transcription.py
   ```

2. **During operation**
   - Speak naturally into your microphone
   - The application will automatically:
     - Detect different speakers
     - Transcribe speech in real-time
     - Format and display transcriptions with speaker labels

3. **Stop the application**
   - Press `Ctrl+C` to gracefully shutdown
   - The application will clean up resources and exit

## Configuration

### Environment Variables
- `DEEPGRAM_API_KEY`: Your Deepgram API key (required)
- `LOG_LEVEL`: Logging level (optional, defaults to INFO)

### Deepgram Settings
The application uses the following Deepgram configuration:
- Model: Nova-2
- Language: English (US)
- Features enabled:
  - Smart formatting
  - Punctuation
  - Speaker diarization
- Speaker settings:
  - Minimum speakers: 2
  - Maximum speakers: 6

## Troubleshooting

### Common Issues

1. **No audio input detected**
   - Check if your microphone is properly connected
   - Verify microphone permissions
   - Test microphone in system settings

2. **API Key errors**
   - Ensure `.env` file exists
   - Verify API key is correctly copied
   - Check Deepgram console for key status

3. **Audio dependencies**
   - Reinstall PyAudio
   - Verify system audio dependencies
   - Check system audio settings

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Deepgram](https://deepgram.com) for their excellent speech-to-text API
- All contributors and users of this project

## Contact

Sohail Hosseini - [@yourusername](https://twitter.com/yourusername)

Project Link: [https://github.com/yourusername/realtime-speech-to-text](https://github.com/yourusername/realtime-speech-to-text)