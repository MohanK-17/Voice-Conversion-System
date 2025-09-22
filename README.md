# Voice Recording, Transcription, and Speech Synthesis Notebook

This repository provides an **end-to-end workflow** for capturing audio, transcribing it, and synthesizing speech with **voice cloning** capabilities in a Google Colab environment. It integrates Faster-Whisper for transcription and SpeechT5 with HifiGan for text-to-speech synthesis.

---

## Features

- 🎤 **Browser-based Audio Recording**: Capture audio directly from your microphone within Colab.
- 🔄 **Automatic Format Conversion**: Convert recorded WebM audio to WAV format seamlessly.
- 📝 **Transcription**: Transcribe recordings using the Faster-Whisper ASR model, including segment timestamps.
- 🗣️ **Voice Cloning**: Generate a speaker embedding from a reference audio file to synthesize speech in your voice.
- 🔊 **Text-to-Speech Synthesis**: Convert text to speech using SpeechT5 and HifiGan vocoder.
- 🎧 **Audio Playback**: Listen to both original recordings and synthesized speech directly in the notebook.
- 📊 **Waveform Visualization**: Plot amplitude waveforms of recorded and synthesized audio.
- 📈 **Evaluation Metrics**: Explore hypothetical ASR (WER) and TTS (MOS, Cosine Similarity) metrics.

---

## Setup and Usage

1. **Open the Notebook**: Launch this notebook in Google Colab.
2. **Install Dependencies**: Run the setup cell to install required libraries.
3. **Record Your Voice**:
    - Click the "Press to start recording" button.
    - Speak clearly and stop the recording.
    - The notebook saves the recording and transcribes it automatically.
4. **Upload Reference Audio**:
    - Upload a short audio file of your voice (3–5 seconds) for voice cloning.
5. **Generate Speaker Embedding**:
    - Run the cells to generate a speaker embedding from the uploaded reference audio.
6. **Synthesize Cloned Speech**:
    - Use the transcribed text and speaker embedding to generate speech in your own voice.
7. **Visualize Waveforms**:
    - View amplitude plots for recorded and synthesized audio.
8. **Explore Metrics**:
    - Run visualization cells to see example ASR and TTS metrics.

---


---

## Dependencies

The notebook uses the following Python libraries:

- `gradio`
- `soundfile`
- `torch`
- `torchaudio`
- `huggingface_hub`
- `ruaccent`
- `datasets`
- `transformers`
- `faster-whisper`
- `ffmpeg-python`
- `coqui-tts`
- `speechbrain`
- `accelerate`

---

## Customization

- **Whisper Model**: Change `model_size` (default: `medium.en`) to use different Faster-Whisper models (`small.en`, `large-v2`, etc.).
- **Reference Audio**: Use a clean reference clip (3–5 seconds) for better voice cloning.
- **Text-to-Speech**: Modify the `transcribed_text` variable to synthesize arbitrary text in your cloned voice.

---

## Acknowledgements

- [Faster-Whisper](https://github.com/guillaumekln/faster-whisper) – Efficient ASR transcription.
- [Hugging Face Transformers](https://huggingface.co/transformers/) – SpeechT5 and HifiGan models.
- [SpeechBrain](https://speechbrain.github.io/) – Speaker embedding models.
- [FFmpeg](https://ffmpeg.org/) – Audio format conversion.

---

This notebook is a comprehensive starting point for experimenting with **voice recording, speech-to-text, and text-to-speech with voice cloning** in Colab.


